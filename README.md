
                        <!DOCTYPE html>
                        <html lang="en">
                        <head>
                            <meta charset="UTF-8">
                            <meta name="viewport" content="width=device-width, initial-scale=1.0">
              <style>
                body {
                  background-color: white; /* Ensure the iframe has a white background */
                }

                :root {
  --primary: #8a2be2;
  --primary-dark: #6a1cb0;
  --secondary: #ff6b6b;
  --dark: #0f0f1b;
  --darker: #0a0a14;
  --text: #e0e0ff;
  --text-secondary: #a0a0c0;
  --success: #4ade80;
  --error: #f87171;
  --card-bg: rgba(25, 25, 45, 0.7);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: linear-gradient(135deg, var(--darker), var(--dark));
  color: var(--text);
  font-family: 'Segoe UI', system-ui, sans-serif;
  min-height: 100vh;
  line-height: 1.6;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Header */
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
  border-bottom: 1px solid rgba(138, 43, 226, 0.3);
}

.logo {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo h1 {
  font-size: 1.8rem;
  background: linear-gradient(90deg, var(--primary), var(--secondary));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.network-badge {
  background: var(--primary);
  color: white;
  padding: 4px 10px;
  border-radius: 20px;
  font-size: 0.8rem;
  margin-left: 10px;
}

.btn {
  background: var(--primary);
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 600;
  transition: all 0.3s ease;
  border: 2px solid var(--primary);
}

.btn:hover {
  background: transparent;
  color: var(--primary);
}

.btn-primary {
  background: var(--primary);
  color: white;
}

.btn-primary:hover {
  background: var(--primary-dark);
  transform: translateY(-2px);
}

.btn-secondary {
  background: var(--secondary);
  color: white;
}

.btn-secondary:hover {
  background: #ff5252;
  transform: translateY(-2px);
}

.btn:disabled {
  opacity: 0.5;
  cursor: not-allowed;
  transform: none;
}

.hidden {
  display: none !important;
}

/* Hero */
.hero {
  text-align: center;
  padding: 60px 0;
}

.hero h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  line-height: 1.2;
}

.highlight {
  color: var(--secondary);
  position: relative;
}

.highlight::after {
  content: '';
  position: absolute;
  bottom: 5px;
  left: 0;
  width: 100%;
  height: 8px;
  background: rgba(255, 107, 107, 0.3);
  z-index: -1;
}

.hero p {
  color: var(--text-secondary);
  max-width: 600px;
  margin: 0 auto 40px;
  font-size: 1.1rem;
}

.rabbit-animation {
  display: flex;
  justify-content: center;
  margin: 30px 0;
}

.rabbit-jumping {
  font-size: 4rem;
  animation: hop 2s infinite;
}

@keyframes hop {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-30px); }
}

/* Dashboard */
.dashboard {
  padding: 40px 0;
}

.card {
  background: var(--card-bg);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(138, 43, 226, 0.3);
  border-radius: 16px;
  padding: 30px;
  margin: 0 auto;
  max-width: 800px;
}

.card h3 {
  text-align: center;
  margin-bottom: 30px;
  color: var(--secondary);
  font-size: 1.5rem;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 20px;
  margin-bottom: 30px;
}

.stat {
  text-align: center;
  padding: 20px;
  background: rgba(30, 30, 50, 0.5);
  border-radius: 12px;
  border: 1px solid rgba(138, 43, 226, 0.2);
}

.stat-value {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 8px;
  color: white;
}

.stat-value.success {
  color: var(--success);
}

.stat-value.error {
  color: var(--error);
}

.actions {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

/* Wisdom Section */
.wisdom-section {
  padding: 60px 0;
}

.wisdom-card {
  background: rgba(25, 25, 45, 0.8);
  border: 2px solid var(--secondary);
  border-radius: 16px;
  padding: 40px;
  text-align: center;
  max-width: 700px;
  margin: 0 auto;
}

.wisdom-card h3 {
  font-size: 1.8rem;
  margin-bottom: 20px;
  color: var(--secondary);
  font-style: italic;
}

.twitter-link {
  display: inline-block;
  background: var(--secondary);
  color: white;
  padding: 12px 24px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  margin-top: 20px;
  transition: all 0.3s ease;
}

.twitter-link:hover {
  background: #ff5252;
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(255, 107, 107, 0.3);
}

/* Footer */
footer {
  text-align: center;
  padding: 40px 0;
  color: var(--text-secondary);
  border-top: 1px solid rgba(138, 43, 226, 0.3);
  margin-top: 40px;
}

#contract-address {
  color: var(--primary);
  font-family: monospace;
}

.footer-links {
  margin-top: 15px;
}

.footer-links a {
  color: var(--primary);
  text-decoration: none;
  margin: 0 15px;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: var(--secondary);
}

/* Modal */
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  background: var(--darker);
  padding: 30px;
  border-radius: 16px;
  border: 1px solid var(--error);
  max-width: 500px;
  width: 90%;
  text-align: center;
}

.modal-content h3 {
  color: var(--error);
  margin-bottom: 15px;
}

.modal-content p {
  margin-bottom: 20px;
  color: var(--text);
}

.modal-content button {
  background: var(--error);
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  cursor: pointer;
}

/* Responsive */
@media (max-width: 768px) {
  .hero h2 {
    font-size: 2rem;
  }
  
  .actions {
    flex-direction: column;
    align-items: center;
  }
  
  .btn {
    width: 100%;
    max-width: 300px;
  }
  
  .stats-grid {
    grid-template-columns: 1fr;
  }
}


              </style>
                        </head>
                        <body>
                            <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>White Rabbit DApp | AssetHub Westend</title>
  <link rel="stylesheet" href="style.css" />
  <script src="https://cdn.ethers.io/lib/ethers-5.7.2.umd.min.js"></script>
</head>
<body>
  <div class="container">
    <!-- Header -->
    <header>
      <div class="logo">
        <span class="rabbit">🐇</span>
        <h1>White Rabbit</h1>
      </div>
      <div id="wallet-status">
        <button id="connect-btn" class="btn">Connect Wallet</button>
        <div id="account-info" class="hidden">
          <span id="address-display"></span>
          <span id="network-badge" class="network-badge">AssetHub Westend</span>
        </div>
      </div>
    </header>

    <!-- Hero -->
    <section class="hero">
      <div class="hero-content">
        <h2>Follow the Rabbit into the <span class="highlight">Narrative</span></h2>
        <p>Deployed on Polkadot AssetHub Westend. Burn HOP tokens to reveal the truth.</p>
        
        <div class="rabbit-animation">
          <div class="rabbit-jumping">🐇</div>
        </div>
      </div>
    </section>

    <!-- Dashboard -->
    <section id="dashboard" class="dashboard hidden">
      <div class="card">
        <h3>Your Status</h3>
        <div class="stats-grid">
          <div class="stat">
            <div class="stat-value" id="hop-balance">0.00</div>
            <div class="stat-label">HOP Balance</div>
          </div>
          <div class="stat">
            <div class="stat-value" id="hopped-status">❌</div>
            <div class="stat-label">Hopped</div>
          </div>
          <div class="stat">
            <div class="stat-value" id="wisdom-status">❌</div>
            <div class="stat-label">Wisdom Claimed</div>
          </div>
        </div>

        <div class="actions">
          <button id="hop-btn" class="btn btn-primary" disabled>
            Execute Hop()
          </button>
          <button id="claim-btn" class="btn btn-secondary" disabled>
            Claim Wisdom
          </button>
        </div>
      </div>
    </section>

    <!-- Wisdom Reveal -->
    <section id="wisdom-section" class="wisdom-section hidden">
      <div class="wisdom-card">
        <h3>"The scarcity is real. The narrative is realer."</h3>
        <a href="https://x.com/thewhiterabbitM" target="_blank" class="twitter-link">
          Follow @thewhiterabbitM →
        </a>
      </div>
    </section>

    <!-- Footer -->
    <footer>
      <p>Interacting with contract: <span id="contract-address">0x087E...1Ad9</span></p>
      <div class="footer-links">
        <a href="https://assethub-westend.subscan.io" target="_blank">Block Explorer</a>
        <a href="https://x.com/thewhiterabbitM" target="_blank">Twitter</a>
      </div>
    </footer>

    <!-- Error Modal -->
    <div id="error-modal" class="modal hidden">
      <div class="modal-content">
        <h3>Error</h3>
        <p id="error-message"></p>
        <button id="close-error">Close</button>
      </div>
    </div>
  </div>

  <script src="main.js"></script>
</body>
</html>



              <script>
                              // Config
const CONTRACT_ADDRESS = "0x087Ea7C436cd9689C9aad64E5B76C6C1C3771Ad9";
const CONTRACT_ABI = [
  "function balanceOf(address) view returns (uint256)",
  "function hop()",
  "function claimWisdom()",
  "function hasHopped(address) view returns (bool)",
  "function hasClaimed(address) view returns (bool)"
];

// DOM Elements
const connectBtn = document.getElementById('connect-btn');
const accountInfo = document.getElementById('account-info');
const addressDisplay = document.getElementById('address-display');
const dashboard = document.getElementById('dashboard');
const hopBalance = document.getElementById('hop-balance');
const hoppedStatus = document.getElementById('hopped-status');
const wisdomStatus = document.getElementById('wisdom-status');
const hopBtn = document.getElementById('hop-btn');
const claimBtn = document.getElementById('claim-btn');
const wisdomSection = document.getElementById('wisdom-section');
const errorModal = document.getElementById('error-modal');
const errorMessage = document.getElementById('error-message');
const closeError = document.getElementById('close-error');
const contractAddressEl = document.getElementById('contract-address');

// Shorten contract address display
contractAddressEl.textContent = `${CONTRACT_ADDRESS.slice(0, 6)}...${CONTRACT_ADDRESS.slice(-4)}`;

// State
let provider = null;
let signer = null;
let contract = null;
let currentAccount = null;

// Initialize
async function init() {
  // Try auto-connect if already authorized
  await autoConnect();
  
  // Event listeners
  connectBtn.addEventListener('click', connectWallet);
  hopBtn.addEventListener('click', executeHop);
  claimBtn.addEventListener('click', claimWisdom);
  closeError.addEventListener('click', () => errorModal.classList.add('hidden'));
  
  // Handle account/network changes
  if (window.ethereum) {
    window.ethereum.on('accountsChanged', () => {
      currentAccount = null;
      location.reload();
    });
    window.ethereum.on('chainChanged', () => {
      location.reload();
    });
  }
}

// Auto-connect if already authorized
async function autoConnect() {
  if (!window.ethereum) return;
  
  try {
    const accounts = await window.ethereum.request({ method: 'eth_accounts' });
    if (accounts.length > 0) {
      await setupWallet(accounts[0]);
    }
  } catch (err) {
    console.log('Auto-connect failed:', err);
  }
}

// Connect wallet
async function connectWallet() {
  if (!window.ethereum) {
    showError('MetaMask not detected. Please install it to proceed.');
    return;
  }
  
  try {
    const accounts = await window.ethereum.request({ method: 'eth_requestAccounts' });
    if (accounts.length === 0) {
      showError('No accounts found. Please create an account in MetaMask.');
      return;
    }
    
    await setupWallet(accounts[0]);
  } catch (err) {
    if (err.code !== 4001) {
      showError('Connection failed. Please ensure you are on AssetHub Westend network.');
    }
  }
}

// Setup wallet connection
async function setupWallet(account) {
  currentAccount = account;
  addressDisplay.textContent = `${account.slice(0, 6)}...${account.slice(-4)}`;
  connectBtn.classList.add('hidden');
  accountInfo.classList.remove('hidden');
  dashboard.classList.remove('hidden');
  
  // Initialize ethers
  provider = new ethers.providers.Web3Provider(window.ethereum);
  signer = provider.getSigner();
  contract = new ethers.Contract(CONTRACT_ADDRESS, CONTRACT_ABI, signer);
  
  // Load data
  await refreshData();
}

// Refresh on-chain data
async function refreshData() {
  if (!contract || !currentAccount) return;
  
  try {
    const [balance, hasHopped, hasClaimed] = await Promise.all([
      contract.balanceOf(currentAccount),
      contract.hasHopped(currentAccount),
      contract.hasClaimed(currentAccount)
    ]);
    
    // Update UI
    hopBalance.textContent = ethers.utils.formatUnits(balance, 18);
    hoppedStatus.textContent = hasHopped ? '✅' : '❌';
    hoppedStatus.className = `stat-value ${hasHopped ? 'success' : 'error'}`;
    
    wisdomStatus.textContent = hasClaimed ? '✅' : '❌';
    wisdomStatus.className = `stat-value ${hasClaimed ? 'success' : 'error'}`;
    
    // Update button states
    hopBtn.disabled = hasHopped;
    claimBtn.disabled = !hasHopped || hasClaimed;
    
    // Show wisdom section if claimed
    if (hasClaimed) {
      wisdomSection.classList.remove('hidden');
    }
  } catch (err) {
    console.error('Refresh error:', err);
    showError('Failed to load data. Please ensure you are on AssetHub Westend network.');
  }
}

// Execute hop
async function executeHop() {
  if (!contract) return;
  
  try {
    const tx = await contract.hop();
    await tx.wait();
    await refreshData();
  } catch (err) {
    if (err.code !== 4001) {
      showError('Hop failed. Please check your gas balance or network connection.');
    }
  }
}

// Claim wisdom
async function claimWisdom() {
  if (!contract) return;
  
  try {
    const tx = await contract.claimWisdom();
    await tx.wait();
    wisdomSection.classList.remove('hidden');
    await refreshData();
  } catch (err) {
    if (err.code !== 4001) {
      showError('Claim failed. You need at least 1 HOP token to claim wisdom.');
    }
  }
}

// Show error modal
function showError(message) {
  errorMessage.textContent = message;
  errorModal.classList.remove('hidden');
}

// Start the app
document.addEventListener('DOMContentLoaded', init);


              </script>
                        </body>
                        </html>
                    
