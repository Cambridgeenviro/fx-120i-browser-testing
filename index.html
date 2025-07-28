<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>FX-120i Browser Interface</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body { 
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
      padding: 20px; 
      background: #f8f9fa; 
      color: #212529; 
      display: flex; 
      transition: all 0.3s ease;
    }
    .main { flex: 3; padding-right: 20px; }
    .sidebar { 
      flex: 1; 
      background: #fff; 
      border-left: 2px solid #dee2e6; 
      padding: 20px; 
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    
    button { 
      margin: 5px; 
      padding: 12px 20px; 
      border: none;
      border-radius: 6px;
      background: #007bff;
      color: white;
      cursor: pointer;
      font-size: 14px;
      transition: all 0.2s ease;
    }
    button:hover { background: #0056b3; transform: translateY(-1px); }
    button:active { transform: translateY(0); }
    button:disabled { background: #6c757d; cursor: not-allowed; }
    
    input, select { 
      margin: 5px; 
      padding: 10px; 
      border: 1px solid #ced4da;
      border-radius: 4px;
      font-size: 14px;
    }
    input:focus, select:focus {
      outline: none;
      border-color: #007bff;
      box-shadow: 0 0 0 2px rgba(0,123,255,0.25);
    }
    
    #log, #consoleOutput { 
      width: 100%; 
      max-height: 200px; 
      overflow-y: auto; 
      background: #fff; 
      border: 1px solid #dee2e6; 
      padding: 15px; 
      margin-top: 10px; 
      border-radius: 6px;
      font-family: 'Courier New', monospace;
      font-size: 12px;
    }
    
    table { 
      border-collapse: collapse; 
      width: 100%; 
      margin-top: 15px; 
      background: #fff; 
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    th, td { 
      border: 1px solid #dee2e6; 
      padding: 12px; 
      text-align: left; 
    }
    th { 
      background: #f8f9fa; 
      font-weight: 600;
      color: #495057;
    }
    
    #weightDisplay { 
      font-size: 3em; 
      margin: 20px 0; 
      font-weight: bold;
      color: #28a745;
      text-align: center;
      background: #fff;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      border: 3px solid #e9ecef;
    }
    
    #chartContainer { 
      width: 100%; 
      max-width: 800px; 
      margin-top: 20px; 
      background: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    
    #status {
      padding: 8px 16px;
      border-radius: 20px;
      font-weight: 500;
      display: inline-block;
      margin: 10px 0;
    }
    .status-connected { background: #d4edda; color: #155724; }
    .status-disconnected { background: #f8d7da; color: #721c24; }

    /* Responsive Layout */
    @media (max-width: 900px) {
      body { flex-direction: column; }
      .main, .sidebar { flex: 1 1 100%; max-width: 100%; }
      .sidebar { margin-top: 20px; padding-left: 0; border-left: none; border-top: 2px solid #dee2e6; }
    }

    /* Grouping */
    fieldset {
      border: 2px solid #dee2e6;
      margin: 15px 0;
      padding: 20px;
      border-radius: 8px;
      background: #fff;
    }
    legend {
      font-weight: 600;
      padding: 0 10px;
      color: #495057;
      font-size: 16px;
    }

    /* Toast Notification */
    .toast {
      position: fixed;
      bottom: 30px;
      right: 30px;
      background: #28a745;
      color: white;
      padding: 15px 25px;
      border-radius: 8px;
      display: none;
      z-index: 1000;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
      animation: slideIn 0.3s ease;
    }

    /* Collapsible fieldset */
    .collapsible-legend {
      cursor: pointer;
      user-select: none;
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
    }
    .collapsible-legend:hover {
      color: #007bff;
    }
    .collapse-icon {
      transition: transform 0.3s ease;
      font-size: 0.8em;
      margin-left: 10px;
    }
    .collapsed .collapse-icon {
      transform: rotate(-90deg);
    }
    .fieldset-content {
      overflow: hidden;
      transition: max-height 0.3s ease, opacity 0.3s ease;
      max-height: 500px;
      opacity: 1;
    }
    .collapsed .fieldset-content {
      max-height: 0;
      opacity: 0;
    }
    
    @keyframes slideIn {
      from { transform: translateX(100%); opacity: 0; }
      to { transform: translateX(0); opacity: 1; }
    }

    .company-header {
      background: linear-gradient(135deg, #007bff, #0056b3);
      color: white;
      padding: 15px;
      border-radius: 8px;
      margin-bottom: 20px;
      text-align: center;
    }
    .company-header h1 { margin: 0; font-size: 1.8em; }
    .company-header .subtitle { opacity: 0.9; margin-top: 5px; }
  </style>
</head>
<body>
  <div class="toast" id="toast">Command sent successfully</div>
  
  <div class="main">
    <div class="company-header">
      <h1>FX-120i Browser Interface</h1>
      <div class="subtitle">Cambridge Environmental Products Inc.</div>
    </div>
    
    <div style="text-align: center; margin-bottom: 20px;">
      <button id="connect">🔌 Connect to Balance</button>
      <div style="margin: 10px 0;">
        <label>Baud Rate: 
          <select id="baudRate">
            <option value="1200">1200</option>
            <option value="2400">2400</option>
            <option value="4800">4800</option>
            <option value="9600" selected>9600</option>
            <option value="19200">19200</option>
            <option value="38400">38400</option>
          </select>
        </label>
      </div>
      <div id="status" class="status-disconnected">Status: Disconnected</div>
    </div>
    
    <div id="weightDisplay">--.-- g</div>

    <fieldset>
      <legend>⚖️ Balance Controls</legend>
      <button id="read">📖 Read Weight (Q)</button>
      <button id="zero">🔄 Zero Balance (Z)</button>
      <button id="tare">⚖️ Tare (T)</button>
      <label style="margin-left: 20px;">
        <input type="checkbox" id="autoPoll"> 
        🔄 Auto-Poll Every Second
      </label>
    </fieldset>

    <fieldset>
      <legend>📊 Data Logging</legend>
      <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px; margin-bottom: 15px;">
        <label>👤 Operator: <input id="operatorName" type="text" placeholder="Enter operator name"></label>
        <label>🧪 Sample ID: <input id="sampleId" type="text" placeholder="Sample identifier"></label>
        <label>⚖️ Threshold: <input id="threshold" type="number" step="0.01" value="0.01"> g</label>
        <label>📏 Units:
          <select id="unitSelect">
            <option value="1">Grams (g)</option>
            <option value="1">Pieces (PCS)</option>
            <option value="1">Percent (%)</option>
            <option value="0.035274">Ounces (OZ)</option>
            <option value="0.00220462">Pounds (lb)</option>
            <option value="0.032151">Troy Ounces (ozt)</option>
            <option value="5">Carats (ct)</option>
            <option value="0.2667">Mommes (mom)</option>
            <option value="0.6430">Pennyweights (dwt)</option>
            <option value="15.4324">Grains (GN)</option>
            <option value="0.0267">Taels (tl)</option>
            <option value="0.0857">Tolas (tol)</option>
            <option value="0.2">Mesgals (mes)</option>
            <option value="1000">Milligrams (MLT)</option>
          </select>
        </label>
      </div>
      <div style="text-align: center;">
        <label style="margin-right: 20px;">
          <input type="checkbox" id="logEnabled"> 
          ✅ Enable Data Logging
        </label>
        <button id="export">📥 Export CSV</button>
        <button id="print">🖨️ Print Report</button>
        <button id="clear">🗑️ Clear All Data</button>
      </div>
    </fieldset>

    <table id="logTable">
      <thead>
        <tr>
          <th>⏰ Timestamp</th>
          <th>⚖️ Weight</th>
          <th>🧪 Sample ID</th>
          <th>👤 Operator</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>

    <div id="chartContainer">
      <canvas id="weightChart"></canvas>
    </div>

    <fieldset id="commandConsole">
      <legend class="collapsible-legend" onclick="toggleCollapse('commandConsole')">
        💻 Command Console
        <span class="collapse-icon">▼</span>
      </legend>
      <div class="fieldset-content">
        <div style="display: flex; gap: 10px; margin-bottom: 10px;">
          <input type="text" id="commandInput" placeholder="Enter RS-232 command (e.g., Q, Z, T)" style="flex: 1;" />
          <button id="sendCommand">📤 Send Command</button>
        </div>
        <pre id="consoleOutput" placeholder="Command responses will appear here..."></pre>
      </div>
    </fieldset>
  </div>
  
  <div class="sidebar">
    <h3>📞 Contact Information</h3>
    <p><strong>Cambridge Environmental Products Inc.</strong></p>
    <p>
      📧 <a href="mailto:sales@cambridgeenviro.com">sales@cambridgeenviro.com</a><br>
      ☎️ Toll-Free: <a href="tel:18005353751">1-800-535-3751</a><br>
      ☎️ Local: <a href="tel:15194737356">519-473-7356</a><br>
      🏢 <a href="https://www.google.com/maps?q=225+Enterprise+Drive,+Komoka,+ON+N0L+1R0" target="_blank">225 Enterprise Drive, Komoka, ON N0L 1R0</a>
    </p>
    
    <iframe src="https://maps.google.com/maps?q=225%20Enterprise%20Drive%2C%20Komoka%20ON%20N0L%201R0&amp;output=embed" 
            width="100%" height="200" style="border:0; border-radius: 6px;" 
            allowfullscreen="" loading="lazy"></iframe>
    
    <hr style="margin: 20px 0;">
    
    <h3>📝 Support Request</h3>
    <form action="mailto:info@ceproducts.ca" method="POST" enctype="text/plain">
      <label for="supportName">Name:</label><br>
      <input type="text" id="supportName" name="Name" required style="width: calc(100% - 10px); margin-bottom: 10px;"><br>
      
      <label for="supportEmail">Email:</label><br>
      <input type="email" id="supportEmail" name="Email" required style="width: calc(100% - 10px); margin-bottom: 10px;"><br>
      
      <label for="supportMessage">Message:</label><br>
      <textarea id="supportMessage" name="Message" rows="4" required 
                style="width: calc(100% - 10px); margin-bottom: 10px; resize: vertical;"></textarea><br>
      
      <button type="submit" style="width: 100%; background: #28a745;">📧 Send Message</button>
    </form>
    
    <hr style="margin: 20px 0;">
    
    <h3>📚 Resources</h3>
    <ul style="list-style: none; padding: 0;">
      <li style="margin-bottom: 8px;">
        <a href="https://cdn.shopify.com/s/files/1/2006/8997/files/FZ-i_FX-i_Manual.pdf?14788397102087296248" 
           target="_blank" style="text-decoration: none;">
          📘 User Manual (PDF)
        </a>
      </li>
      <li style="margin-bottom: 8px;">
        <a href="https://cdn.shopify.com/s/files/1/2006/8997/files/FZ-i_FX-i_Series_Literature.pdf?14788397102087296248" 
           target="_blank" style="text-decoration: none;">
          📄 Product Brochure
        </a>
      </li>
    </ul>
    
    <hr style="margin: 20px 0;">
    
    <h3>📈 Session Statistics</h3>
    <div style="background: #f8f9fa; padding: 15px; border-radius: 6px;">
      <p><strong>📊 Average:</strong> <span id="avgValue">--</span></p>
      <p><strong>📏 Std Deviation:</strong> <span id="stdDevValue">--</span></p>
      <p><strong>📋 Total Readings:</strong> <span id="totalReadings">0</span></p>
      <button id="showStats" style="width: 100%; background: #17a2b8;">🔄 Update Statistics</button>
    </div>
  </div>

  <script>
    let port, reader, writer, textBuffer = '';
    let chart, chartData = [], chartLabels = [], weights = [];
    let autoPollInterval;

    function showToast(message, type = 'success') {
      const toast = document.getElementById('toast');
      toast.textContent = message;
      toast.style.background = type === 'success' ? '#28a745' : '#dc3545';
      toast.style.display = 'block';
      setTimeout(() => { 
        toast.style.display = 'none'; 
      }, 3000);
    }

    function updateStatus(connected) {
      const status = document.getElementById('status');
      if (connected) {
        status.textContent = 'Status: Connected ✅';
        status.className = 'status-connected';
        document.getElementById('connect').textContent = '🔌 Disconnect';
      } else {
        status.textContent = 'Status: Disconnected ❌';
        status.className = 'status-disconnected';
        document.getElementById('connect').textContent = '🔌 Connect to Balance';
      }
    }

    document.getElementById('connect').addEventListener('click', async () => {
      try {
        if (port && port.readable) {
          // Disconnect
          if (reader) {
            await reader.cancel();
            reader.releaseLock();
          }
          if (writer) {
            writer.releaseLock();
          }
          await port.close();
          port = null;
          updateStatus(false);
          clearInterval(autoPollInterval);
          document.getElementById('autoPoll').checked = false;
          showToast('Disconnected from balance');
          return;
        }

        // Connect
        if (!navigator.serial) {
          throw new Error('Web Serial API not supported in this browser');
        }

        port = await navigator.serial.requestPort();
        const baudRate = parseInt(document.getElementById('baudRate').value);
        await port.open({ 
          baudRate: baudRate,
          dataBits: 8,
          stopBits: 1,
          parity: 'none',
          flowControl: 'none'
        });
        
        writer = port.writable.getWriter();
        reader = port.readable.getReader();
        updateStatus(true);
        setupChart();
        listenToPort();
        showToast('Successfully connected to FX-120i balance!');
      } catch (err) {
        showToast('Connection failed: ' + err.message, 'error');
        console.error('Connection error:', err);
      }
    });

    async function sendCommand(cmd) {
      if (!writer) {
        showToast('Not connected to balance', 'error');
        return;
      }
      try {
        const encoder = new TextEncoder();
        await writer.write(encoder.encode(cmd + '\r\n'));
        showToast(`Command sent: ${cmd}`);
        
        // Add to console output
        const console = document.getElementById('consoleOutput');
        console.textContent += `> ${cmd}\n`;
        console.scrollTop = console.scrollHeight;
      } catch (err) {
        showToast('Failed to send command: ' + err.message, 'error');
      }
    }

    // Control buttons
    document.getElementById('read').onclick = () => sendCommand('Q');
    document.getElementById('zero').onclick = () => sendCommand('Z');
    document.getElementById('tare').onclick = () => sendCommand('T');

    document.getElementById('showStats').onclick = () => {
      if (weights.length === 0) {
        showToast('No weight data available', 'error');
        return;
      }
      
      const avg = weights.reduce((a,b) => a + b, 0) / weights.length;
      const stdDev = calculateStdDev(weights);
      
      document.getElementById('avgValue').textContent = avg.toFixed(4);
      document.getElementById('stdDevValue').textContent = stdDev.toFixed(4);
      document.getElementById('totalReadings').textContent = weights.length;
      
      showToast('Statistics updated');
    };

    document.getElementById('autoPoll').addEventListener('change', (e) => {
      if (e.target.checked) {
        if (!port || !port.readable) {
          showToast('Connect to balance first', 'error');
          e.target.checked = false;
          return;
        }
        autoPollInterval = setInterval(() => sendCommand('Q'), 1000);
        showToast('Auto-polling started');
      } else {
        clearInterval(autoPollInterval);
        showToast('Auto-polling stopped');
      }
    });

    document.getElementById('sendCommand').onclick = () => {
      const cmd = document.getElementById('commandInput').value.trim();
      if (cmd) {
        sendCommand(cmd);
        document.getElementById('commandInput').value = '';
      }
    };

    // Enter key support for command input
    document.getElementById('commandInput').addEventListener('keypress', (e) => {
      if (e.key === 'Enter') {
        document.getElementById('sendCommand').click();
      }
    });

    async function listenToPort() {
      const decoder = new TextDecoder();
      try {
        while (port && port.readable) {
          const { value, done } = await reader.read();
          if (done) break;
          
          const chunk = decoder.decode(value);
          textBuffer += chunk;
          
          // Update console output
          const console = document.getElementById('consoleOutput');
          console.textContent += chunk;
          console.scrollTop = console.scrollHeight;
          
          // Process complete lines
          let lines = textBuffer.split('\n');
          textBuffer = lines.pop() || '';
          
          for (let line of lines) {
            const clean = line.trim();
            const match = clean.match(/[-+]?\s*\d*\.?\d+\s*g/);
            if (match) {
              const numeric = match[0].replace('g', '').trim();
              handleWeight(numeric);
            }
          }
        }
      } catch (error) {
        console.error('Port reading error:', error);
        updateStatus(false);
        showToast('Connection lost. Attempting to reconnect...', 'error');
        
        // Auto-reconnect attempt
        setTimeout(() => {
          if (port && !port.readable) {
            document.getElementById('connect').click();
          }
        }, 3000);
      }
    }

    function handleWeight(weight) {
      const weightNum = parseFloat(weight);
      if (isNaN(weightNum)) return;
      
      const multiplier = parseFloat(document.getElementById('unitSelect').value);
      const adjustedWeight = (weightNum * multiplier).toFixed(4);
      const threshold = parseFloat(document.getElementById('threshold').value) || 0;
      const sampleId = document.getElementById('sampleId').value || 'N/A';
      const operator = document.getElementById('operatorName').value || 'N/A';
      const unitText = document.getElementById('unitSelect').options[document.getElementById('unitSelect').selectedIndex].text.match(/\((.*?)\)/)[1];

      // Update main display
      document.getElementById('weightDisplay').textContent = `${adjustedWeight} ${unitText}`;

      // Log if enabled and above threshold
      if (document.getElementById('logEnabled').checked && Math.abs(weightNum) >= threshold) {
        const time = new Date().toLocaleString();
        const logRow = document.createElement('tr');
        logRow.innerHTML = `
          <td>${time}</td>
          <td>${adjustedWeight} ${unitText}</td>
          <td>${sampleId}</td>
          <td>${operator}</td>
        `;
        document.querySelector('#logTable tbody').appendChild(logRow);
        
        // Update chart data
        const timeLabel = new Date().toLocaleTimeString();
        chartData.push(parseFloat(adjustedWeight));
        chartLabels.push(timeLabel);
        weights.push(parseFloat(adjustedWeight));
        
        // Keep only last 50 points for performance
        if (chartData.length > 50) {
          chartData.shift();
          chartLabels.shift();
        }
        
        if (chart) {
          chart.update('none'); // No animation for better performance
        }
        
        // Auto-scroll table
        const tableContainer = document.getElementById('logTable').parentElement;
        tableContainer.scrollTop = tableContainer.scrollHeight;
      }
    }

    function setupChart() {
      const ctx = document.getElementById('weightChart').getContext('2d');
      if (chart) {
        chart.destroy();
      }
      
      chart = new Chart(ctx, {
        type: 'line',
        data: {
          labels: chartLabels,
          datasets: [{
            label: 'Weight Over Time',
            data: chartData,
            borderColor: '#007bff',
            backgroundColor: 'rgba(0, 123, 255, 0.1)',
            borderWidth: 2,
            fill: true,
            tension: 0.4,
            pointRadius: 3,
            pointHoverRadius: 6
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          scales: {
            y: { 
              beginAtZero: false,
              title: { display: true, text: 'Weight' }
            },
            x: { 
              display: true, 
              title: { display: true, text: 'Time' }
            }
          },
          plugins: {
            legend: {
              display: true,
              position: 'top'
            }
          },
          animation: {
            duration: 0 // Disable animations for real-time data
          }
        }
      });
    }

    document.getElementById('clear').onclick = () => {
      if (confirm('Are you sure you want to clear all logged data?')) {
        document.querySelector('#logTable tbody').innerHTML = '';
        chartData.length = 0;
        chartLabels.length = 0;
        weights.length = 0;
        
        if (chart) {
          chart.update();
        }
        
        document.getElementById('avgValue').textContent = '--';
        document.getElementById('stdDevValue').textContent = '--';
        document.getElementById('totalReadings').textContent = '0';
        
        showToast('All data cleared');
      }
    };

    document.getElementById('export').onclick = () => {
      const rows = [['Timestamp', 'Weight', 'Sample ID', 'Operator']];
      document.querySelectorAll('#logTable tbody tr').forEach(tr => {
        const cols = [...tr.querySelectorAll('td')].map(td => td.textContent.trim());
        rows.push(cols);
      });
      
      if (rows.length === 1) {
        showToast('No data to export', 'error');
        return;
      }
      
      const csv = rows.map(r => r.map(cell => `"${cell}"`).join(',')).join('\n');
      const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = `fx120i_log_${new Date().toISOString().split('T')[0]}.csv`;
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
      URL.revokeObjectURL(url);
      
      showToast(`Exported ${rows.length - 1} readings to CSV`);
    };

    document.getElementById('print').onclick = () => {
      if (weights.length === 0) {
        showToast('No data to print', 'error');
        return;
      }
      
      const avg = (weights.reduce((a,b) => a + b, 0) / weights.length).toFixed(4);
      const stdDev = calculateStdDev(weights).toFixed(4);
      const operator = document.getElementById('operatorName').value || 'N/A';
      const unitText = document.getElementById('unitSelect').options[document.getElementById('unitSelect').selectedIndex].text.match(/\((.*?)\)/)[1];
      
      const printWindow = window.open('', '', 'width=800,height=600');
      printWindow.document.write(`
        <html>
          <head>
            <title>FX-120i Log Summary</title>
            <style>
              body { font-family: Arial, sans-serif; margin: 20px; }
              table { border-collapse: collapse; width: 100%; }
              th, td { border: 1px solid #ddd; padding: 8px; text-align: left; }
              th { background-color: #f2f2f2; }
              .header { text-align: center; margin-bottom: 30px; }
              .stats { background: #f9f9f9; padding: 15px; margin: 20px 0; }
            </style>
          </head>
          <body>
            <div class="header">
              <h1>FX-120i Balance Log Summary</h1>
              <p>Cambridge Environmental Products Inc.</p>
              <p>Generated: ${new Date().toLocaleString()}</p>
            </div>
            <div class="stats">
              <h3>Session Statistics</h3>
              <p><strong>Operator:</strong> ${operator}</p>
              <p><strong>Total Readings:</strong> ${weights.length}</p>
              <p><strong>Average Weight:</strong> ${avg} ${unitText}</p>
              <p><strong>Standard Deviation:</strong> ${stdDev} ${unitText}</p>
            </div>
            ${document.getElementById('logTable').outerHTML}
          </body>
        </html>
      `);
      printWindow.document.close();
      printWindow.print();
      
      showToast('Print dialog opened');
    };

    function calculateStdDev(arr) {
      if (arr.length === 0) return 0;
      const mean = arr.reduce((a, b) => a + b, 0) / arr.length;
      const variance = arr.reduce((sum, val) => sum + Math.pow(val - mean, 2), 0) / arr.length;
      return Math.sqrt(variance);
    }

    // Initialize chart container height
    document.getElementById('chartContainer').style.height = '400px';

    // Collapsible functionality
    function toggleCollapse(fieldsetId) {
      const fieldset = document.getElementById(fieldsetId);
      fieldset.classList.toggle('collapsed');
    }
  </script>
</body>
</html>
