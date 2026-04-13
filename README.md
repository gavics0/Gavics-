<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gavics🍻 • On-Chain Believer</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
  <script src="https://cdn.jsdelivr.net/npm/web3@4.3.0/dist/web3.min.js"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Space+Grotesk:wght@500;600&display=swap');
    body { font-family: 'Inter', sans-serif; }
    .heading-font { font-family: 'Space Grotesk', sans-serif; }
    .hero-bg { background: linear-gradient(135deg, #0f172a 0%, #1e2937 100%); }
    .card-hover:hover { transform: translateY(-8px); box-shadow: 0 30px 60px -15px rgb(245 158 11 / 0.2); }
    .article-content { white-space: pre-wrap; }
  </style>
</head>
<body class="bg-slate-950 text-white">

  <!-- NAVBAR -->
  <nav class="bg-slate-900 border-b border-slate-800 sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-6 py-5 flex items-center justify-between">
      <div class="flex items-center gap-3">
        <img src="https://pbs.twimg.com/profile_images/2028415001615327232/8l3VDK5f.jpg" alt="Gavics" class="w-10 h-10 rounded-2xl">
        <span class="text-2xl font-semibold heading-font">Gavics🍻</span>
      </div>

      <div class="flex gap-8 text-lg font-medium">
        <a href="#work" class="hover:text-amber-400 transition">Work</a>
        <a href="#articles" class="hover:text-amber-400 transition">Articles</a>
        <a href="#ama" class="hover:text-amber-400 transition">AMAs</a>
        <a href="#tokenomics" class="hover:text-amber-400 transition">Tokenomics</a>
        <a href="#connect" class="hover:text-amber-400 transition">Connect</a>
      </div>

      <div class="flex items-center gap-4">
        <div class="flex items-center gap-2 bg-slate-800 px-4 py-2 rounded-3xl text-sm font-medium">
          <i class="fa-solid fa-eye text-amber-400"></i>
          <span id="visitor-count" class="tabular-nums">2,341</span>
          <span class="text-slate-400 text-xs">believers</span>
        </div>

        <button onclick="connectWallet()" id="wallet-btn"
                class="flex items-center gap-2 bg-gradient-to-r from-amber-400 to-orange-500 text-slate-950 px-6 py-3 rounded-3xl font-semibold hover:scale-105 transition">
          <i class="fa-brands fa-ethereum"></i>
          <span id="wallet-text">Connect Wallet</span>
        </button>

        <button onclick="showShareModal()" 
                class="flex items-center gap-2 bg-slate-800 hover:bg-slate-700 px-5 py-3 rounded-3xl font-medium transition">
          <i class="fa-solid fa-share-nodes"></i> Share
        </button>
      </div>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero-bg py-24">
    <div class="max-w-7xl mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
      <div>
        <h1 class="text-6xl font-bold leading-none heading-font">The Story of Every Believer</h1>
        <p class="mt-6 text-xl text-slate-300">Phygital Researcher | UX Designer | Graphics Designer | NFT Lover</p>
        <p class="mt-8 text-lg max-w-lg text-slate-400">On-chain truth through consistency. One day we build it all together.</p>
        <div class="mt-10 flex gap-4 flex-wrap">
          <a href="https://x.com/Gavics0" target="_blank" class="bg-white text-slate-950 px-8 py-4 rounded-3xl font-semibold flex items-center gap-3 hover:scale-105 transition">Follow on X</a>
          <a href="https://wa.me/2348119090628" target="_blank" class="border border-amber-400 text-amber-400 px-8 py-4 rounded-3xl font-semibold flex items-center gap-3 hover:bg-amber-400 hover:text-slate-950 transition">Chat on WhatsApp</a>
        </div>
      </div>
      <div class="flex justify-center">
        <img src="https://pbs.twimg.com/profile_images/2028415001615327232/8l3VDK5f.jpg" alt="Gavics" class="w-80 h-80 object-cover rounded-3xl border-4 border-amber-400 shadow-2xl">
      </div>
    </div>
  </section>

  <!-- WORK -->
  <section id="work" class="py-20">
    <div class="max-w-7xl mx-auto px-6">
      <h2 class="text-4xl font-semibold text-center mb-12 heading-font">My Craft</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-slate-800 p-8 rounded-3xl card-hover">
          <h3 class="text-2xl font-semibold mb-3">UX Designer</h3>
          <p class="text-slate-400">Crafting intuitive on-chain experiences.</p>
        </div>
        <div class="bg-slate-800 p-8 rounded-3xl card-hover">
          <h3 class="text-2xl font-semibold mb-3">Phygital Researcher</h3>
          <p class="text-slate-400">Bridging physical conviction and digital permanence.</p>
        </div>
        <div class="bg-slate-800 p-8 rounded-3xl card-hover">
          <h3 class="text-2xl font-semibold mb-3">Graphics Designer</h3>
          <p class="text-slate-400">Visuals that speak the language of Web3 and belief.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ARTICLES SECTION - Where you can write & publish -->
  <section id="articles" class="py-20 bg-slate-900">
    <div class="max-w-7xl mx-auto px-6">
      <div class="flex justify-between items-center mb-12">
        <h2 class="text-4xl font-semibold heading-font">Articles &amp; Conviction Drops</h2>
        <button onclick="showPostModal()" 
                class="bg-amber-400 hover:bg-amber-300 text-slate-950 px-8 py-4 rounded-3xl font-semibold flex items-center gap-3 transition">
          <i class="fa-solid fa-plus"></i> Write New Article
        </button>
      </div>

      <div id="articles-container" class="space-y-16">
        <!-- Articles will appear here dynamically when you publish -->
      </div>
    </div>
  </section>

  <!-- AMA, TOKENOMICS, CONNECT sections (short) -->
  <section id="ama" class="py-20">
    <div class="max-w-7xl mx-auto px-6 text-center">
      <h2 class="text-4xl font-semibold heading-font mb-4">Live AMAs</h2>
      <p class="text-slate-400">Ask me anything about phygital research, UX in Web3, or NFTs.</p>
      <button onclick="alert('Next AMA coming soon — join via X Spaces!')" 
              class="mt-8 bg-amber-400 text-slate-950 px-10 py-5 rounded-3xl font-semibold">Join Next AMA</button>
    </div>
  </section>

  <section id="tokenomics" class="py-20 bg-slate-900">
    <div class="max-w-7xl mx-auto px-6 text-center">
      <h2 class="text-4xl font-semibold heading-font mb-4">Tokenomics (Coming Soon)</h2>
      <p class="text-slate-400">Future utility token for believers.</p>
    </div>
  </section>

  <section id="connect" class="py-20">
    <div class="max-w-7xl mx-auto px-6 text-center">
      <h2 class="text-4xl font-semibold heading-font mb-8">Let’s Connect</h2>
      <div class="inline-flex gap-12">
        <a href="https://x.com/Gavics0" target="_blank" class="flex flex-col items-center hover:text-amber-400">
          <i class="fa-brands fa-x-twitter text-5xl mb-3"></i> @Gavics0
        </a>
        <a href="https://wa.me/2348119090628" target="_blank" class="flex flex-col items-center hover:text-green-400">
          <i class="fa-brands fa-whatsapp text-5xl mb-3"></i> WhatsApp
        </a>
      </div>
    </div>
  </section>

  <!-- WRITE NEW ARTICLE MODAL -->
  <div id="post-modal" class="hidden fixed inset-0 bg-black/80 z-[100] flex items-center justify-center">
    <div class="bg-slate-900 w-full max-w-2xl mx-4 rounded-3xl p-8">
      <h3 class="text-3xl font-semibold heading-font mb-6">Write New Article</h3>
      <input id="article-title" type="text" placeholder="Article Title" 
             class="w-full bg-slate-800 border border-slate-700 rounded-3xl px-6 py-5 text-lg mb-6 outline-none focus:border-amber-400">
      <textarea id="article-content" rows="12" placeholder="Write your conviction here... (Markdown supported in future)" 
                class="w-full bg-slate-800 border border-slate-700 rounded-3xl px-6 py-5 outline-none focus:border-amber-400 article-content"></textarea>
      
      <div class="flex gap-4 mt-8">
        <button onclick="hidePostModal()" class="flex-1 border border-slate-600 py-6 rounded-3xl font-semibold">Cancel</button>
        <button onclick="publishArticle()" class="flex-1 bg-amber-400 text-slate-950 py-6 rounded-3xl font-semibold">Publish Article</button>
      </div>
    </div>
  </div>

  <!-- SHARE MODAL -->
  <div id="share-modal" class="hidden fixed inset-0 bg-black/80 z-[100] flex items-center justify-center">
    <div class="bg-slate-900 w-full max-w-md mx-4 rounded-3xl p-8 text-center">
      <h3 class="text-2xl font-semibold mb-6">Share My Work Profile</h3>
      <div class="bg-slate-800 p-4 rounded-2xl mb-8 break-all text-amber-400 font-mono text-sm" id="share-url">
        https://yourusername.github.io/gavics
      </div>
      <div class="flex justify-center gap-10">
        <button onclick="copyProfileLink()" class="flex flex-col items-center hover:text-amber-400">
          <i class="fa-solid fa-copy text-4xl mb-2"></i>
          <span class="text-sm">Copy Link</span>
        </button>
        <a href="https://x.com/intent/tweet?text=Check%20out%20Gavics%20portfolio%20-%20Phygital%20Researcher" target="_blank" class="flex flex-col items-center hover:text-amber-400">
          <i class="fa-brands fa-x-twitter text-4xl mb-2"></i>
          <span class="text-sm">X</span>
        </a>
        <a href="https://wa.me/?text=Check%20out%20Gavics%20portfolio:%20https://yourusername.github.io/gavics" target="_blank" class="flex flex-col items-center hover:text-green-400">
          <i class="fa-brands fa-whatsapp text-4xl mb-2"></i>
          <span class="text-sm">WhatsApp</span>
        </a>
      </div>
      <button onclick="hideShareModal()" class="mt-10 text-slate-400 hover:text-white">Close</button>
    </div>
  </div>

  <footer class="bg-black py-8 text-center text-slate-500 text-sm">
    © Gavics🍻 • Built with conviction •
  </footer>

  <script>
    // Web3 Wallet
    async function connectWallet() {
      if (typeof window.ethereum === "undefined") {
        alert("Please install MetaMask or any Web3 wallet to connect.");
        return;
      }
      try {
        const accounts = await window.ethereum.request({ method: 'eth_requestAccounts' });
        const addr = accounts[0].slice(0, 6) + "..." + accounts[0].slice(-4);
        document.getElementById("wallet-text").innerHTML = `✓ ${addr}`;
      } catch (e) {
        alert("Wallet connection cancelled.");
      }
    }

    // Fake live visitor count
    let visitorCount = 2341;
    setInterval(() => {
      visitorCount += Math.floor(Math.random() * 4) + 1;
      document.getElementById("visitor-count").textContent = visitorCount.toLocaleString();
    }, 6000);

    // Show / Hide Modals
    function showPostModal() {
      document.getElementById("post-modal").classList.remove("hidden");
      document.getElementById("post-modal").classList.add("flex");
    }
    function hidePostModal() {
      document.getElementById("post-modal").classList.add("hidden");
      document.getElementById("post-modal").classList.remove("flex");
    }

    function showShareModal() {
      document.getElementById("share-modal").classList.remove("hidden");
      document.getElementById("share-modal").classList.add("flex");
    }
    function hideShareModal() {
      document.getElementById("share-modal").classList.add("hidden");
      document.getElementById("share-modal").classList.remove("flex");
    }

    function copyProfileLink() {
      const currentUrl = window.location.href;
      navigator.clipboard.writeText(currentUrl).then(() => {
        alert("✅ Profile link copied! Share your conviction.");
      });
    }

    // Publish New Article (adds to the page instantly)
    function publishArticle() {
      const title = document.getElementById("article-title").value.trim();
      const content = document.getElementById("article-content").value.trim();

      if (!title || !content) {
        alert("Please add both title and content.");
        return;
      }

      const container = document.getElementById("articles-container");
      const articleHTML = `
        <div class="bg-slate-800 p-10 rounded-3xl card-hover">
          <div class="flex justify-between items-start">
            <h3 class="text-3xl font-semibold heading-font">${title}</h3>
            <span class="text-slate-400 text-sm">${new Date().toLocaleDateString('en-US', {month:'short', day:'numeric', year:'numeric'})}</span>
          </div>
          <div class="mt-8 text-slate-300 leading-relaxed article-content">${content}</div>
          
          <div class="flex justify-between mt-10 border-t border-slate-700 pt-8">
            <button onclick="likeArticle(this)" class="flex items-center gap-3 text-amber-400 hover:text-red-400 transition-colors">
              <i class="fa-solid fa-heart text-2xl"></i>
              <span class="likes-count text-xl font-semibold">0</span>
            </button>
            <button onclick="alert('Article link copied! (In real hosting it will be permanent)')" 
                    class="text-slate-400 hover:text-white flex items-center gap-2">
              <i class="fa-solid fa-link"></i> Share this article
            </button>
          </div>

          <!-- Comments Area -->
          <div class="mt-12">
            <h4 class="font-medium mb-4">Community Reactions</h4>
            <div class="comments-container space-y-6 mb-8"></div>
            <div class="flex gap-3">
              <input type="text" placeholder="Your name / wallet" class="comment-author flex-1 bg-slate-700 border border-slate-600 rounded-3xl px-6 py-4 text-sm">
              <textarea placeholder="Drop a comment..." rows="2" class="comment-text flex-1 bg-slate-700 border border-slate-600 rounded-3xl px-6 py-4 text-sm resize-none"></textarea>
              <button onclick="postComment(this)" class="px-8 bg-amber-400 hover:bg-amber-300 text-slate-950 rounded-3xl font-semibold">Send</button>
            </div>
          </div>
        </div>`;

      container.insertAdjacentHTML('afterbegin', articleHTML);
      hidePostModal();

      // Clear form
      document.getElementById("article-title").value = "";
      document.getElementById("article-content").value = "";

      alert("✅ Article published! It will stay visible as long as this page is open.");
    }

    // Like Article
    function likeArticle(btn) {
      let countEl = btn.querySelector('.likes-count');
      let count = parseInt(countEl.textContent);
      countEl.textContent = count + 1;
      btn.classList.add('text-red-400');
    }

    // Post Comment
    function postComment(btn) {
      const container = btn.parentElement.parentElement.querySelector('.comments-container');
      const authorInput = btn.parentElement.querySelector('.comment-author');
      const textInput = btn.parentElement.querySelector('.comment-text');

      const author = authorInput.value.trim() || "Believer";
      const text = textInput.value.trim();

      if (!text) return;

      const commentHTML = `
        <div class="bg-slate-700 p-5 rounded-3xl">
          <div class="font-semibold">${author}</div>
          <p class="mt-2">${text}</p>
          <div class="text-xs text-slate-400 mt-3">just now</div>
        </div>`;

      container.innerHTML += commentHTML;
      textInput.value = "";
    }

    // Load some sample articles when page opens
    window.onload = function() {
      const container = document.getElementById("articles-container");
      const samples = [
        {
          title: "Why Phygital Ownership Matters",
          content: "The future belongs to those who can prove both physical presence and on-chain permanence. Here’s my latest research."
        },
        {
          title: "100 Days of On-Chain Consistency",
          content: "Daily UX improvements recorded forever on Arbitrum. What I learned about building belief systems in Web3."
        }
      ];

      samples.forEach(sample => {
        const html = `
          <div class="bg-slate-800 p-10 rounded-3xl card-hover">
            <div class="flex justify-between">
              <h3 class="text-3xl font-semibold heading-font">${sample.title}</h3>
              <span class="text-slate-400 text-sm">Apr 2026</span>
            </div>
            <div class="mt-8 text-slate-300 leading-relaxed">${sample.content}</div>
            <div class="flex justify-between mt-10">
              <button onclick="likeArticle(this)" class="flex items-center gap-3 text-amber-400">
                <i class="fa-solid fa-heart"></i> <span class="likes-count">12</span>
              </button>
              <button onclick="alert('Shared!')" class="text-slate-400 hover:text-white">Share</button>
            </div>
            <div class="mt-12">
              <h4 class="font-medium mb-4">Reactions</h4>
              <div class="comments-container space-y-6"></div>
              <div class="flex gap-3 mt-6">
                <input type="text" placeholder="Your name" class="comment-author flex-1 bg-slate-700 border border-slate-600 rounded-3xl px-6 py-4 text-sm">
                <textarea placeholder="Comment..." rows="2" class="comment-text flex-1 bg-slate-700 border border-slate-600 rounded-3xl px-6 py-4 text-sm resize-none"></textarea>
                <button onclick="postComment(this)" class="px-8 bg-amber-400 text-slate-950 rounded-3xl font-semibold">Send</button>
              </div>
            </div>
          </div>`;
        container.innerHTML += html;
      });
    };
  </script>
</body>
</html>
