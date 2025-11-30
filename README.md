<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>RAMS HALO BANDO - Internet Service Provider</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Helvetica', 'Arial', sans-serif;
      background: linear-gradient(-45deg, #f97316, #ea580c, #fbbf24, #f59e0b);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .container {
      max-width: 600px;
      width: 100%;
      background: white;
      border-radius: 24px;
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
      overflow: hidden;
    }

    .header {
      background: linear-gradient(135deg, #f97316 0%, #fbbf24 100%);
      padding: 40px 30px;
      text-align: center;
      color: white;
    }

    .logo {
      width: 60px;
      height: 60px;
      background: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 16px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }

    .logo svg {
      width: 30px;
      height: 30px;
      stroke: #f97316;
      stroke-width: 2;
      fill: none;
    }

    .header h1 {
      font-size: 28px;
      font-weight: 700;
      margin-bottom: 4px;
      letter-spacing: 0.5px;
    }

    .header p {
      font-size: 16px;
      opacity: 0.9;
      font-weight: 500;
    }

    .form-container {
      padding: 32px;
    }

    .form-group {
      margin-bottom: 24px;
    }

    .form-group label {
      display: flex;
      align-items: center;
      gap: 8px;
      font-weight: 600;
      color: #374151;
      margin-bottom: 8px;
      font-size: 15px;
    }

    .form-group label svg {
      width: 18px;
      height: 18px;
      stroke: #f97316;
      stroke-width: 2;
      fill: none;
    }

    .form-group input,
    .form-group select {
      width: 100%;
      padding: 12px 14px;
      border: 2px solid #e5e7eb;
      border-radius: 10px;
      font-size: 15px;
      transition: all 0.3s ease;
      font-family: inherit;
    }

    .form-group input:focus,
    .form-group select:focus {
      outline: none;
      border-color: #f97316;
      box-shadow: 0 0 0 3px rgba(249, 115, 22, 0.1);
    }

    .form-group small {
      display: block;
      margin-top: 6px;
      color: #9ca3af;
      font-size: 13px;
    }

    .cost-box {
      background: linear-gradient(135deg, #fef3c7 0%, #fef08a 100%);
      border: 2px solid #fcd34d;
      border-radius: 12px;
      padding: 20px;
      margin-bottom: 24px;
    }

    .cost-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 12px;
    }

    .cost-row:last-child {
      margin-bottom: 0;
    }

    .cost-label {
      color: #6b7280;
      font-weight: 500;
      font-size: 14px;
    }

    .cost-value {
      font-weight: 700;
      color: #b45309;
      font-size: 18px;
    }

    .cost-value.total {
      font-size: 24px;
      color: #d97706;
    }

    button {
      width: 100%;
      padding: 16px;
      background: linear-gradient(135deg, #f97316 0%, #fbbf24 100%);
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 12px rgba(249, 115, 22, 0.2);
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(249, 115, 22, 0.3);
    }

    button:active {
      transform: translateY(0);
    }

    button:disabled {
      opacity: 0.6;
      cursor: not-allowed;
    }

    .form-note {
      text-align: center;
      color: #9ca3af;
      font-size: 13px;
      margin-top: 16px;
    }

    .footer {
      text-align: center;
      padding: 16px;
      color: rgba(255, 255, 255, 0.8);
      font-size: 12px;
      margin-top: 16px;
    }

    @media (max-width: 480px) {
      .form-container {
        padding: 24px;
      }

      .header {
        padding: 32px 20px;
      }

      .header h1 {
        font-size: 24px;
      }

      .cost-box {
        padding: 16px;
      }
    }
  </style>
</head>
<body>
  <div>
    <div class="container">
      <div class="header">
        <div class="logo">
          <svg viewBox="0 0 24 24">
            <path d="M12 2c5.5 0 10 4.5 10 10s-4.5 10-10 10S2 17.5 2 12 6.5 2 12 2m0 2c-4.4 0-8 3.6-8 8s3.6 8 8 8 8-3.6 8-8-3.6-8-8-8m3.5 5c.8 0 1.5.7 1.5 1.5s-.7 1.5-1.5 1.5-1.5-.7-1.5-1.5.7-1.5 1.5-1.5m-7 0c.8 0 1.5.7 1.5 1.5s-.7 1.5-1.5 1.5-1.5-.7-1.5-1.5.7-1.5 1.5-1.5m3.5 6c1.7 0 3.2-1 4-2.5h-8c.8 1.5 2.3 2.5 4 2.5z"/>
          </svg>
        </div>
        <h1>RAMS HALO BANDO</h1>
        <p>Internet Service Provider</p>
      </div>

      <div class="form-container">
        <h2 style="text-align: center; margin-bottom: 28px; color: #1f2937; font-size: 22px;">Order Your Internet Service</h2>

        <form id="orderForm">
          <div class="form-group">
            <label>
              <svg viewBox="0 0 24 24">
                <path d="M12 12c2.2 0 4-1.8 4-4s-1.8-4-4-4-4 1.8-4 4 1.8 4 4 4m0 2c-2.7 0-8 1.3-8 4v2h16v-2c0-2.7-5.3-4-8-4z"/>
              </svg>
              Your Name
            </label>
            <input type="text" id="customerName" placeholder="John Doe" required>
          </div>

          <div class="form-group">
            <label>
              <svg viewBox="0 0 24 24">
                <path d="M17 10.5V7c0 .55-.45 1-1 1H4c-.55 0-1-.45-1-1v10c0 .55.45 1 1 1h12c.55 0 1-.45 1-1v-3.5l4 4v-11l-4 4z"/>
              </svg>
              Your Phone Number
            </label>
            <input type="tel" id="customerPhone" placeholder="2557XXXXXXXX" required>
            <small>Include country code (e.g., 2557XXXXXXXX)</small>
          </div>

          <div class="form-group">
            <label>
              <svg viewBox="0 0 24 24">
                <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2m-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
              </svg>
              Select Data Package
            </label>
            <select id="gbAmount">
              <option value="10">10 GB - Tsh 10,000</option>
              <option value="20">20 GB - Tsh 20,000</option>
              <option value="30">30 GB - Tsh 30,000</option>
              <option value="40">40 GB - Tsh 40,000</option>
              <option value="50">50 GB - Tsh 50,000</option>
              <option value="60">60 GB - Tsh 60,000</option>
              <option value="70">70 GB - Tsh 70,000</option>
              <option value="80">80 GB - Tsh 80,000</option>
              <option value="90">90 GB - Tsh 90,000</option>
              <option value="100">100 GB - Tsh 100,000</option>
            </select>
          </div>

          <div class="cost-box">
            <div class="cost-row">
              <span class="cost-label">Selected Package:</span>
              <span class="cost-value"><span id="gbDisplay">10</span> GB</span>
            </div>
            <div class="cost-row">
              <span class="cost-label">Total Cost:</span>
              <span class="cost-value total" id="costDisplay">Tsh 10,000</span>
            </div>
          </div>

          <button type="submit">Place Order via WhatsApp</button>
          <p class="form-note">Clicking the button will open WhatsApp to send your order</p>
        </form>
      </div>
    </div>

    <div class="footer">
      <p>© 2025 RAMS HALO BANDO. All rights reserved.</p>
    </div>
  </div>

  <script>
    const PRICE_PER_GB = 1000;
    const gbSelect = document.getElementById('gbAmount');
    const gbDisplay = document.getElementById('gbDisplay');
    const costDisplay = document.getElementById('costDisplay');
    const orderForm = document.getElementById('orderForm');

    function formatCurrency(amount) {
      return 'Tsh ' + amount.toLocaleString();
    }

    function updateCost() {
      const gb = Number(gbSelect.value);
      gbDisplay.textContent = gb;
      costDisplay.textContent = formatCurrency(gb * PRICE_PER_GB);
    }

    gbSelect.addEventListener('change', updateCost);

    orderForm.addEventListener('submit', function(e) {
      e.preventDefault();

      const name = document.getElementById('customerName').value.trim();
      const phone = document.getElementById('customerPhone').value.trim();
      const gb = Number(gbSelect.value);
      const cost = gb * PRICE_PER_GB;

      if (!name || !phone) {
        alert('Please enter your name and phone number.');
        return;
      }

      const orderDetails = `SERVICE: INTERNET\nAMOUNT OF GB: ${gb}\nTOTAL COST: ${formatCurrency(cost)}\nNAME: ${name}\nPHONE: ${phone}\nDATE: ${new Date().toLocaleString()}`;

      const cleanPhone = phone.replace(/\D/g, '');
      const encodedText = encodeURIComponent(orderDetails);
      const whatsappUrl = cleanPhone.length >= 9
        ? `https://wa.me/${cleanPhone}?text=${encodedText}`
        : `https://web.whatsapp.com/send?text=${encodedText}`;

      window.open(whatsappUrl, '_blank');
    });
  </script>
</body>
</html>
