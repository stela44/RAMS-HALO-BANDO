<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>RAMS HALO BANDO CLIENT SITE</title>
  <style>
    body{
      font-family:Inter,system-ui,Segoe UI,Roboto,Helvetica,Arial;
      max-width:900px;
      margin:28px auto;
      padding:18px;
      color:#fff;
      font-size:18px;
      background: linear-gradient(-45deg, #FAA533, #ff7b00, #ffb84d, #ff914d);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
    }
    @keyframes gradientBG {
      0% {background-position:0% 50%}
      50% {background-position:100% 50%}
      100% {background-position:0% 50%}
    }
    h1{font-size:28px;margin-bottom:10px;color:#fff}
    h2{font-size:32px;margin-bottom:20px;color:#fff;text-align:center}
    label{display:block;margin-top:12px;font-weight:600;color:#fff;font-size:18px}
    input,select,button{
      padding:12px 14px;
      margin-top:6px;
      border:1px solid #FAA533;
      border-radius:6px;
      font-size:18px;
    }
    button{
      background:#FAA533;
      color:#fff;
      cursor:pointer;
      font-size:18px;
    }
    button:hover{
      opacity:0.9;
    }
    .controls{margin-top:14px;display:flex;gap:10px;justify-content:center}
  </style>
</head>
<body>
  <h2>RAMS HALO BANDO CLIENT SITE</h2>
  <h1>Order Your INTERNET Service</h1>
  <p class="muted">Fill in your details below. Clicking <strong>Place Order</strong> will open WhatsApp to send your order directly.</p>

  <form id="orderForm">
    <label>Your Name</label>
    <input id="customerName" type="text" placeholder="John Doe" required />

    <label>Your Phone (include country code, e.g., 2557XXXXXXXX)</label>
    <input id="customerPhone" type="tel" placeholder="2557XXXXXXXX" required />

    <label>Service</label>
    <input id="service" type="text" value="INTERNET" readonly />

    <label>Amount of GB (10 to 100)</label>
    <select id="gbAmount"></select>

    <label>Total Cost</label>
    <input id="cost" type="text" readonly />

    <div class="controls">
      <button type="submit">Place Order via WhatsApp</button>
    </div>
  </form>

  <script>
    const PRICE_PER_GB = 1000;
    const gbSelect = document.getElementById('gbAmount');
    for(let g = 10; g <= 100; g += 10){
      const opt = document.createElement('option');
      opt.value = g; opt.textContent = g + ' GB';
      gbSelect.appendChild(opt);
    }

    const costInput = document.getElementById('cost');
    function formatTsh(n){ return 'Tsh ' + String(n).replace(/\B(?=(\d{3})+(?!\d))/g, ','); }
    function updateCost(){
      const gb = Number(gbSelect.value || 10);
      costInput.value = formatTsh(gb * PRICE_PER_GB);
    }
    gbSelect.addEventListener('change', updateCost);
    updateCost();

    function openWhatsAppForOrder(order){
      const phone = order.phone.replace(/\D/g,'');
      const text = `SERVICE: ${order.service}\nAMOUNT OF GB: ${order.gb}\nTOTAL COST: ${order.cost}\nNAME: ${order.name}\nPHONE: ${order.phone}\nDATE: ${order.date}`;
      const encoded = encodeURIComponent(text);
      const url = phone.length >= 9 ? `https://wa.me/${phone}?text=${encoded}` : `https://web.whatsapp.com/send?text=${encoded}`;
      window.open(url, '_blank');
    }

    document.getElementById('orderForm').addEventListener('submit', function(e){
      e.preventDefault();
      const name = document.getElementById('customerName').value.trim();
      const phone = document.getElementById('customerPhone').value.trim();
      const service = document.getElementById('service').value.trim();
      const gb = Number(document.getElementById('gbAmount').value);
      const cost = gb * PRICE_PER_GB;
      if(!name || !phone){ alert('Please enter your name and phone number.'); return; }
      const order = { date: new Date().toLocaleString(), name, phone, service, gb, cost };
      openWhatsAppForOrder(order);
      alert('WhatsApp opened to send your order.');
    });
  </script>
</body>
</html>
