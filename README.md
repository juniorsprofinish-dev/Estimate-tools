<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Junior's Pro Finish, LLC - Drywall Estimator</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }

    body {
      background-color: #f4f6f8;
      color: #333;
      padding: 20px;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
    }

    .header-card, .section-card, .summary-card {
      background: #ffffff;
      border-radius: 8px;
      padding: 24px;
      margin-bottom: 20px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    }

    h1 {
      color: #2c3e50;
      font-size: 24px;
      margin-bottom: 4px;
    }

    h2 {
      color: #7f8c8d;
      font-size: 14px;
      letter-spacing: 1px;
      margin-bottom: 20px;
    }

    h3 {
      font-size: 16px;
      color: #34495e;
      margin-bottom: 16px;
    }

    .grid-4 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 16px;
    }

    .field-group {
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    label {
      font-size: 12px;
      font-weight: 600;
      color: #7f8c8d;
      text-transform: uppercase;
    }

    input[type="text"],
    input[type="number"],
    input[type="date"] {
      padding: 10px 12px;
      border: 1px solid #dcdfe6;
      border-radius: 6px;
      font-size: 14px;
      outline: none;
      transition: border-color 0.2s;
      width: 100%;
    }

    input:focus {
      border-color: #3498db;
    }

    .rate-summary {
      background-color: #fff8ec;
      border-left: 4px solid #f39c12;
      padding: 12px 16px;
      border-radius: 4px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .highlight-price {
      font-size: 20px;
      font-weight: bold;
      color: #d35400;
    }

    .toolbar {
      display: flex;
      gap: 10px;
      margin-bottom: 16px;
    }

    .btn {
      padding: 10px 16px;
      border: none;
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
      font-size: 14px;
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .btn-primary { background: #e67e22; color: white; }
    .btn-secondary { background: #27ae60; color: white; }
    .btn-dark { background: #34495e; color: white; }
    .btn-danger { background: #e74c3c; color: white; padding: 6px 12px; font-size: 12px; }

    /* Room Card Styling */
    .room-card {
      background: #ffffff;
      border: 1px solid #e2e8f0;
      border-radius: 8px;
      padding: 16px;
      margin-bottom: 12px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    }

    .room-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 12px;
    }

    .room-title {
      font-weight: bold;
      color: #2c3e50;
    }

    /* Controls aligned to the right side of room header */
    .room-header-controls {
      display: flex;
      align-items: center;
      gap: 16px;
    }

    .checkbox-inline {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .checkbox-inline label {
      display: flex;
      align-items: center;
      gap: 6px;
      text-transform: none;
      font-size: 14px;
      color: #2c3e50;
      cursor: pointer;
    }

    /* 4-column grid for dimension inputs */
    .room-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 12px;
    }

    @media (max-width: 600px) {
      .room-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    /* Summary Dashboard */
    .summary-card {
      background: #1a252f;
      color: white;
    }

    .summary-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 20px;
      text-align: center;
      margin-bottom: 20px;
    }

    .metric-title {
      font-size: 11px;
      color: #bdc3c7;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 6px;
    }

    .metric-value {
      font-size: 22px;
      font-weight: bold;
    }

    .total-bid {
      border-top: 1px solid #34495e;
      padding-top: 16px;
      text-align: center;
    }

    .total-bid .metric-value {
      font-size: 32px;
      color: #f39c12;
    }
  </style>
</head>
<body>

<div class="container">
  
  <!-- Header -->
  <div class="header-card">
    <h1>Junior's Pro Finish, LLC</h1>
    <h2>DRYWALL CONTRACTING ESTIMATE</h2>

    <div class="grid-4">
      <div class="field-group">
        <label>Customer Name</label>
        <input type="text" id="cust-name" value="John Doe">
      </div>
      <div class="field-group">
        <label>Phone Number</label>
        <input type="text" id="cust-phone" value="(555) 123-4567">
      </div>
      <div class="field-group">
        <label>Email Address</label>
        <input type="text" id="cust-email" value="john@example.com">
      </div>
      <div class="field-group">
        <label>Date</label>
        <input type="date" id="doc-date">
      </div>
    </div>

    <div class="field-group" style="margin-top: 16px;">
      <label>Project Site Address</label>
      <input type="text" id="cust-address" value="123 Main St, City, State, Zip">
    </div>
  </div>

  <!-- Pricing Structure -->
  <div class="section-card">
    <h3>Pricing Structure & Material Settings</h3>
    <div class="grid-4" style="align-items: center;">
      <div class="field-group">
        <label>Labor Rate ($/sq ft)</label>
        <input type="number" id="labor-rate" step="0.05" value="2.90" oninput="calculateTotals()">
      </div>
      <div class="field-group">
        <label>Material Rate ($/sq ft)</label>
        <input type="number" id="material-rate" step="0.05" value="0.65" oninput="calculateTotals()">
      </div>
      <div class="field-group">
        <label>Waste Allowance</label>
        <div style="font-weight: bold; padding: 10px 0;">+15% Included</div>
      </div>
      <div class="rate-summary">
        <div>
          <label style="display:block; margin-bottom:2px;">Combined Rate</label>
          <span class="highlight-price" id="combined-rate-display">$3.55</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Room Breakdown -->
  <div class="section-card">
    <h3>Room Dimensions & Area Breakdown</h3>
    
    <div class="toolbar">
      <button type="button" class="btn btn-primary" onclick="addRoom()">➕ Add Room</button>
      <button type="button" class="btn btn-secondary" onclick="exportCSV()">💾 Export to CSV</button>
      <button type="button" class="btn btn-dark" onclick="window.print()">🖨️ Print / Save as PDF</button>
    </div>

    <div id="rooms-container"></div>
  </div>

  <!-- Total Summary -->
  <div class="summary-card">
    <div class="summary-grid">
      <div>
        <div class="metric-title">Total Board Area</div>
        <div class="metric-value" id="total-sqft">0 sq ft</div>
      </div>
      <div>
        <div class="metric-title">Est. 4x12 Sheets (w/ waste)</div>
        <div class="metric-value" id="total-sheets">0 sheets</div>
      </div>
      <div>
        <div class="metric-title">Estimated Labor</div>
        <div class="metric-value" id="total-labor">$0.00</div>
      </div>
      <div>
        <div class="metric-title">Estimated Material</div>
        <div class="metric-value" id="total-material">$0.00</div>
      </div>
    </div>

    <div class="total-bid">
      <div class="metric-title" style="color: #ea8014;">Total Bid Estimate</div>
      <div class="metric-value" id="total-bid">$0.00</div>
    </div>
  </div>

</div>

<script>
  let roomCount = 0;

  // Set default date to today
  document.getElementById('doc-date').valueAsDate = new Date();

  function addRoom(defaultName = '') {
    roomCount++;
    const container = document.getElementById('rooms-container');
    
    const roomCard = document.createElement('div');
    roomCard.className = 'room-card';
    roomCard.id = `room-${roomCount}`;

    const initialName = (typeof defaultName === 'string') ? defaultName : '';

    roomCard.innerHTML = `
      <div class="room-header">
        <span class="room-title">Room #${roomCount}</span>
        <div class="room-header-controls">
          <div class="checkbox-inline">
            <label><input type="checkbox" class="inc-walls" checked onchange="calculateTotals()"> Walls</label>
            <label><input type="checkbox" class="inc-ceiling" checked onchange="calculateTotals()"> Ceiling</label>
          </div>
          <button type="button" class="btn btn-danger" onclick="removeRoom(${roomCount})">Remove</button>
        </div>
      </div>
      <div class="room-grid">
        <div class="field-group">
          <label>Room Name</label>
          <input type="text" class="room-name" value="${initialName}" placeholder="e.g. Living Room">
        </div>
        <div class="field-group">
          <label>Length (ft)</label>
          <input type="number" class="room-length" value="0" min="0" oninput="calculateTotals()">
        </div>
        <div class="field-group">
          <label>Width (ft)</label>
          <input type="number" class="room-width" value="0" min="0" oninput="calculateTotals()">
        </div>
        <div class="field-group">
          <label>Height (ft)</label>
          <input type="number" class="room-height" value="8" min="0" oninput="calculateTotals()">
        </div>
      </div>
    `;

    container.appendChild(roomCard);
    calculateTotals();
  }

  function removeRoom(id) {
    const card = document.getElementById(`room-${id}`);
    if (card) {
      card.remove();
      calculateTotals();
    }
  }

  function calculateTotals() {
    const laborRate = parseFloat(document.getElementById('labor-rate').value) || 0;
    const materialRate = parseFloat(document.getElementById('material-rate').value) || 0;
    const combinedRate = laborRate + materialRate;

    document.getElementById('combined-rate-display').innerText = `$${combinedRate.toFixed(2)}`;

    let totalArea = 0;
    const rooms = document.querySelectorAll('.room-card');

    rooms.forEach(room => {
      const length = parseFloat(room.querySelector('.room-length').value) || 0;
      const width = parseFloat(room.querySelector('.room-width').value) || 0;
      const height = parseFloat(room.querySelector('.room-height').value) || 0;
      const incWalls = room.querySelector('.inc-walls').checked;
      const incCeiling = room.querySelector('.inc-ceiling').checked;

      let roomSqFt = 0;

      if (incWalls) {
        roomSqFt += (2 * length * height) + (2 * width * height);
      }
      if (incCeiling) {
        roomSqFt += (length * width);
      }

      totalArea += roomSqFt;
    });

    const wasteSqFt = totalArea * 1.15;
    const sheetCount = Math.ceil(wasteSqFt / 48);

    const laborCost = totalArea * laborRate;
    const materialCost = totalArea * materialRate;
    const totalBid = laborCost + materialCost;

    document.getElementById('total-sqft').innerText = `${totalArea.toLocaleString()} sq ft`;
    document.getElementById('total-sheets').innerText = `${sheetCount} sheets`;
    document.getElementById('total-labor').innerText = `$${laborCost.toFixed(2)}`;
    document.getElementById('total-material').innerText = `$${materialCost.toFixed(2)}`;
    document.getElementById('total-bid').innerText = `$${totalBid.toFixed(2)}`;
  }

  function exportCSV() {
    let csv = "Room Name,Length (ft),Width (ft),Height (ft),Walls,Ceiling\n";
    const rooms = document.querySelectorAll('.room-card');

    rooms.forEach(room => {
      const name = room.querySelector('.room-name').value || "Unnamed Room";
      const length = room.querySelector('.room-length').value || 0;
      const width = room.querySelector('.room-width').value || 0;
      const height = room.querySelector('.room-height').value || 0;
      const walls = room.querySelector('.inc-walls').checked ? "Yes" : "No";
      const ceiling = room.querySelector('.inc-ceiling').checked ? "Yes" : "No";

      csv += `"${name}",${length},${width},${height},${walls},${ceiling}\n`;
    });

    const blob = new Blob([csv], { type: 'text/csv' });
    const url = window.URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = `Drywall_Estimate_${new Date().toISOString().slice(0,10)}.csv`;
    a.click();
  }

  // Add one initial room on load
  addRoom();
</script>

</body>
</html># Estimate-tools
