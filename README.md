<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>LOOPSNHOOKS — Handmade Crochet Gifts</title>
<meta name="description" content="Handmade crochet products for gifts — flowers, bags, and winter essentials. Order online, made in Gujarat.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,600;0,9..144,700;1,9..144,500&family=Karla:wght@400;500;600;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ivory:#F5F1E8;
    --card:#FFFDF8;
    --charcoal:#2B2620;
    --charcoal-soft:#5A5348;
    --berry:#A8455E;
    --berry-dark:#8A3750;
    --sage:#6E8570;
    --gold:#C79A46;
    --line:#DDD4C4;
    --radius:14px;
    --shadow: 0 4px 16px rgba(43,38,32,0.08);
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--ivory);
    color:var(--charcoal);
    font-family:'Karla',sans-serif;
    -webkit-font-smoothing:antialiased;
    padding-bottom:90px;
  }
  h1,h2,h3{font-family:'Fraunces',serif; margin:0;}
  .price, .tag-mono{font-family:'Space Mono',monospace;}

  /* ---------- stitched divider signature ---------- */
  .stitch-divider{
    width:100%; height:14px; margin:0 auto;
    background-image: radial-gradient(circle at 7px 7px, var(--berry) 3px, transparent 3.5px);
    background-size:22px 14px;
    background-repeat:repeat-x;
    background-position:center;
    opacity:0.55;
  }

  /* ---------- header ---------- */
  header{
    padding:34px 20px 22px;
    text-align:center;
    position:relative;
  }
  .eyebrow{
    font-family:'Space Mono',monospace;
    font-size:11px;
    letter-spacing:0.18em;
    color:var(--sage);
    text-transform:uppercase;
    margin-bottom:6px;
    display:block;
  }
  header h1{
    font-size:clamp(2rem, 8vw, 3.2rem);
    font-weight:700;
    letter-spacing:-0.01em;
    color:var(--berry-dark);
  }
  header .tagline{
    font-size:0.95rem;
    color:var(--charcoal-soft);
    letter-spacing:0.04em;
    margin-top:8px;
    font-style:italic;
    font-family:'Fraunces',serif;
  }
  .shop-meta{
    margin-top:16px;
    display:flex;
    flex-wrap:wrap;
    gap:10px 18px;
    justify-content:center;
    font-size:0.8rem;
    color:var(--charcoal-soft);
  }
  .shop-meta a{color:var(--berry-dark); text-decoration:none;}

  /* ---------- filters ---------- */
  .filters{
    display:flex;
    gap:10px;
    overflow-x:auto;
    padding:22px 20px 10px;
    -ms-overflow-style:none;
    scrollbar-width:none;
  }
  .filters::-webkit-scrollbar{display:none;}
  .filter-btn{
    flex:0 0 auto;
    padding:9px 18px;
    border-radius:999px;
    border:1.5px solid var(--line);
    background:var(--card);
    color:var(--charcoal-soft);
    font-family:'Karla',sans-serif;
    font-weight:600;
    font-size:0.8rem;
    letter-spacing:0.03em;
    cursor:pointer;
    transition:all .2s ease;
    white-space:nowrap;
  }
  .filter-btn:hover{border-color:var(--berry);}
  .filter-btn.active{
    background:var(--berry);
    border-color:var(--berry);
    color:#fff;
  }

  /* ---------- product grid ---------- */
  .grid{
    display:grid;
    grid-template-columns:repeat(2, 1fr);
    gap:16px;
    padding:14px 20px 30px;
    max-width:1100px;
    margin:0 auto;
  }
  @media(min-width:640px){ .grid{grid-template-columns:repeat(3,1fr);} }
  @media(min-width:960px){ .grid{grid-template-columns:repeat(4,1fr);} }

  .card{
    background:var(--card);
    border-radius:var(--radius);
    overflow:hidden;
    box-shadow:var(--shadow);
    display:flex;
    flex-direction:column;
    transition:transform .18s ease;
  }
  .card:hover{transform:translateY(-3px);}
  .card-img-wrap{
    aspect-ratio:1/1;
    overflow:hidden;
    background:#EFE8DA;
  }
  .card-img-wrap img{
    width:100%; height:100%; object-fit:cover; display:block;
  }
  .card-body{
    padding:12px 12px 14px;
    display:flex;
    flex-direction:column;
    gap:6px;
    flex:1;
  }
  .card-cat{
    font-size:0.65rem;
    letter-spacing:0.1em;
    color:var(--sage);
    font-weight:700;
    text-transform:uppercase;
  }
  .card-name{
    font-size:0.95rem;
    font-weight:600;
    line-height:1.25;
    font-family:'Karla',sans-serif;
  }
  .card-desc{
    font-size:0.78rem;
    color:var(--charcoal-soft);
    font-style:italic;
    font-family:'Fraunces',serif;
  }
  .card-footer{
    margin-top:auto;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:8px;
    padding-top:6px;
  }
  .card-price{
    font-size:0.95rem;
    font-weight:700;
    color:var(--berry-dark);
  }
  .add-btn{
    border:none;
    background:var(--charcoal);
    color:#fff;
    padding:8px 14px;
    border-radius:8px;
    font-size:0.75rem;
    font-weight:700;
    letter-spacing:0.03em;
    cursor:pointer;
    transition:background .18s ease, transform .12s ease;
  }
  .add-btn:hover{background:var(--berry);}
  .add-btn.added{background:var(--sage); transform:scale(0.96);}

  .empty-state{
    grid-column:1/-1;
    text-align:center;
    padding:40px 20px;
    color:var(--charcoal-soft);
    font-family:'Fraunces',serif;
    font-style:italic;
  }

  /* ---------- floating buttons ---------- */
  .floating-stack{
    position:fixed;
    right:18px;
    bottom:18px;
    display:flex;
    flex-direction:column;
    gap:12px;
    z-index:40;
  }
  .fab{
    width:58px; height:58px;
    border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    box-shadow:0 6px 18px rgba(43,38,32,0.22);
    cursor:pointer;
    border:none;
    position:relative;
    transition:transform .15s ease;
  }
  .fab:active{transform:scale(0.94);}
  .fab-cart{background:var(--berry); color:#fff;}
  .fab-wa{background:#25D366; color:#fff; text-decoration:none;}
  .fab svg{width:26px; height:26px;}
  .cart-badge{
    position:absolute;
    top:-4px; right:-4px;
    background:var(--gold);
    color:#2B2620;
    font-family:'Space Mono',monospace;
    font-size:11px;
    font-weight:700;
    min-width:20px;
    height:20px;
    border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    padding:0 4px;
    border:2px solid var(--ivory);
  }

  /* ---------- overlay / drawers ---------- */
  .overlay{
    position:fixed; inset:0;
    background:rgba(43,38,32,0.45);
    z-index:50;
    opacity:0;
    pointer-events:none;
    transition:opacity .22s ease;
  }
  .overlay.open{opacity:1; pointer-events:auto;}

  .drawer{
    position:fixed;
    right:0; top:0; bottom:0;
    width:min(420px, 100%);
    background:var(--ivory);
    z-index:60;
    transform:translateX(100%);
    transition:transform .28s ease;
    display:flex;
    flex-direction:column;
    box-shadow:-8px 0 24px rgba(0,0,0,0.15);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-header{
    padding:20px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    border-bottom:1px solid var(--line);
  }
  .drawer-header h2{font-size:1.3rem;}
  .close-btn{
    background:none; border:none; font-size:1.6rem;
    cursor:pointer; color:var(--charcoal-soft); line-height:1;
  }
  .drawer-body{
    flex:1;
    overflow-y:auto;
    padding:16px 20px;
  }
  .drawer-footer{
    padding:18px 20px 22px;
    border-top:1px solid var(--line);
    background:var(--card);
  }

  .cart-item{
    display:flex;
    gap:12px;
    padding:14px 0;
    border-bottom:1px dashed var(--line);
  }
  .cart-item img{width:64px; height:64px; object-fit:cover; border-radius:10px; flex-shrink:0;}
  .cart-item-info{flex:1; min-width:0;}
  .cart-item-name{font-weight:600; font-size:0.9rem; margin-bottom:2px;}
  .cart-item-price{font-size:0.8rem; color:var(--charcoal-soft);}
  .qty-row{
    display:flex; align-items:center; gap:10px; margin-top:8px;
  }
  .qty-btn{
    width:26px; height:26px;
    border-radius:50%;
    border:1.5px solid var(--line);
    background:var(--card);
    cursor:pointer;
    font-weight:700;
    font-size:0.9rem;
    line-height:1;
    color:var(--charcoal);
  }
  .qty-num{font-family:'Space Mono',monospace; font-size:0.85rem; min-width:16px; text-align:center;}
  .remove-link{
    background:none; border:none; color:var(--berry); font-size:0.75rem;
    text-decoration:underline; cursor:pointer; margin-left:auto;
  }
  .item-subtotal{
    font-family:'Space Mono',monospace;
    font-weight:700;
    font-size:0.85rem;
    align-self:flex-start;
    white-space:nowrap;
  }
  .cart-empty{
    text-align:center; padding:40px 10px; color:var(--charcoal-soft);
    font-family:'Fraunces',serif; font-style:italic;
  }
  .grand-total-row{
    display:flex; justify-content:space-between; align-items:baseline;
    margin-bottom:14px;
  }
  .grand-total-row span:first-child{font-size:0.85rem; color:var(--charcoal-soft); text-transform:uppercase; letter-spacing:0.05em;}
  .grand-total-row span:last-child{font-size:1.4rem; font-weight:700; color:var(--berry-dark); font-family:'Space Mono',monospace;}

  .btn-primary{
    width:100%;
    padding:14px;
    background:var(--berry);
    color:#fff;
    border:none;
    border-radius:10px;
    font-size:0.95rem;
    font-weight:700;
    letter-spacing:0.02em;
    cursor:pointer;
    transition:background .18s ease;
  }
  .btn-primary:hover{background:var(--berry-dark);}
  .btn-primary:disabled{background:#C7BCAE; cursor:not-allowed;}

  /* ---------- checkout form ---------- */
  .field{margin-bottom:14px;}
  .field label{
    display:block; font-size:0.78rem; font-weight:700;
    text-transform:uppercase; letter-spacing:0.04em;
    color:var(--charcoal-soft); margin-bottom:5px;
  }
  .field input, .field textarea{
    width:100%;
    padding:11px 12px;
    border-radius:8px;
    border:1.5px solid var(--line);
    background:var(--card);
    font-family:'Karla',sans-serif;
    font-size:0.9rem;
    color:var(--charcoal);
  }
  .field input:focus, .field textarea:focus{
    outline:2px solid var(--sage);
    outline-offset:1px;
  }
  .field textarea{resize:vertical; min-height:60px;}
  .required-mark{color:var(--berry);}
  .order-summary-box{
    background:var(--card);
    border:1px dashed var(--line);
    border-radius:10px;
    padding:12px 14px;
    margin-bottom:16px;
    font-size:0.8rem;
    color:var(--charcoal-soft);
    max-height:120px;
    overflow-y:auto;
  }
  .order-summary-box div{display:flex; justify-content:space-between; padding:2px 0;}

  .confirmation{
    text-align:center;
    padding:30px 10px;
  }
  .confirmation .check{
    width:56px; height:56px; border-radius:50%;
    background:var(--sage); color:#fff;
    display:flex; align-items:center; justify-content:center;
    margin:0 auto 16px; font-size:1.6rem;
  }
  .confirmation h3{margin-bottom:8px; font-size:1.2rem;}
  .confirmation p{color:var(--charcoal-soft); font-size:0.88rem; margin-bottom:20px;}
  .wa-inline-link{
    display:inline-flex; align-items:center; gap:8px;
    background:#25D366; color:#fff; text-decoration:none;
    padding:11px 20px; border-radius:999px; font-weight:700; font-size:0.85rem;
  }

  footer{
    text-align:center;
    padding:30px 20px 10px;
    color:var(--charcoal-soft);
    font-size:0.78rem;
  }

  .visually-hidden{
    position:absolute; width:1px; height:1px; overflow:hidden;
    clip:rect(0,0,0,0); white-space:nowrap;
  }

  @media (prefers-reduced-motion: reduce){
    *{transition:none !important; animation:none !important;}
  }
</style>
</head>
<body>

<header>
  <span class="eyebrow">Gujarat · Handmade to order</span>
  <h1>LOOPSNHOOKS</h1>
  <p class="tagline">Handmade crochet products for gifts</p>
  <div class="shop-meta">
    <span>📍 Gujarat, India</span>
    <a href="tel:+918238841842">📞 +91 82388 41842</a>
    <a href="mailto:Loopsnhooks0603@gmail.com">✉️ Loopsnhooks0603@gmail.com</a>
  </div>
</header>

<div class="stitch-divider"></div>

<nav class="filters" id="filters" aria-label="Filter products by category"></nav>

<main>
  <section class="grid" id="grid" aria-live="polite"></section>
</main>

<div class="stitch-divider"></div>

<footer>
  Made by hand in Gujarat · © 2026 LOOPSNHOOKS · Orders confirmed via WhatsApp before dispatch
</footer>

<!-- floating buttons -->
<div class="floating-stack">
  <a class="fab fab-wa" id="waFab" href="https://wa.me/918238841842" target="_blank" rel="noopener" aria-label="Chat on WhatsApp">
    <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12.04 2C6.58 2 2.13 6.45 2.13 11.91c0 1.75.46 3.43 1.32 4.92L2.05 22l5.32-1.39c1.43.78 3.03 1.19 4.66 1.19h.01c5.46 0 9.91-4.45 9.91-9.9C21.95 6.45 17.5 2 12.04 2zm0 18.1h-.01c-1.47 0-2.91-.39-4.17-1.14l-.3-.18-3.12.82.83-3.04-.2-.31a8.19 8.19 0 0 1-1.26-4.36c0-4.54 3.7-8.24 8.24-8.24 2.2 0 4.27.86 5.83 2.42a8.18 8.18 0 0 1 2.41 5.82c0 4.54-3.7 8.21-8.25 8.21zm4.52-6.16c-.25-.12-1.47-.72-1.7-.81-.23-.08-.39-.12-.56.13-.17.25-.64.81-.78.97-.14.17-.29.19-.54.06-.25-.12-1.04-.38-1.98-1.22-.73-.65-1.23-1.46-1.37-1.71-.14-.25-.02-.38.11-.51.11-.11.25-.29.37-.43.12-.14.16-.25.25-.41.08-.17.04-.31-.02-.43-.06-.12-.56-1.35-.77-1.85-.2-.48-.41-.42-.56-.43-.14-.01-.31-.01-.48-.01a.92.92 0 0 0-.67.31c-.23.25-.87.85-.87 2.08s.89 2.41 1.02 2.58c.12.17 1.75 2.67 4.24 3.75.59.26 1.05.41 1.41.52.59.19 1.13.16 1.56.1.48-.07 1.47-.6 1.68-1.18.21-.58.21-1.07.14-1.18-.06-.11-.23-.17-.48-.29z"/></svg>
  </a>
  <button class="fab fab-cart" id="cartFab" aria-label="Open cart">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="9" cy="21" r="1"></circle><circle cx="20" cy="21" r="1"></circle><path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"></path></svg>
    <span class="cart-badge" id="cartBadge" style="display:none;">0</span>
  </button>
</div>

<!-- overlay -->
<div class="overlay" id="overlay"></div>

<!-- cart drawer -->
<div class="drawer" id="cartDrawer" role="dialog" aria-label="Shopping cart">
  <div class="drawer-header">
    <h2>Your basket</h2>
    <button class="close-btn" id="closeCart" aria-label="Close cart">&times;</button>
  </div>
  <div class="drawer-body" id="cartItems"></div>
  <div class="drawer-footer" id="cartFooter" style="display:none;">
    <div class="grand-total-row"><span>Grand total</span><span id="grandTotal">₹0</span></div>
    <button class="btn-primary" id="checkoutBtn">Place order</button>
  </div>
</div>

<!-- checkout drawer -->
<div class="drawer" id="checkoutDrawer" role="dialog" aria-label="Checkout form">
  <div class="drawer-header">
    <h2>Delivery details</h2>
    <button class="close-btn" id="closeCheckout" aria-label="Close checkout">&times;</button>
  </div>
  <div class="drawer-body">
    <div id="checkoutFormWrap">
      <div class="order-summary-box" id="orderSummaryBox"></div>
      <form id="orderForm">
        <div class="field">
          <label for="custName">Full name <span class="required-mark">*</span></label>
          <input type="text" id="custName" name="Customer Name" required>
        </div>
        <div class="field">
          <label for="custPhone">Phone number <span class="required-mark">*</span></label>
          <input type="tel" id="custPhone" name="Phone Number" required>
        </div>
        <div class="field">
          <label for="custAddress">Delivery address <span class="required-mark">*</span></label>
          <textarea id="custAddress" name="Delivery Address" required></textarea>
        </div>
        <div class="field">
          <label for="custNotes">Special instructions (optional)</label>
          <textarea id="custNotes" name="Special Instructions"></textarea>
        </div>
        <input type="hidden" name="Order Summary" id="orderSummaryField">
        <input type="hidden" name="Grand Total" id="grandTotalField">
        <input type="hidden" name="_subject" value="New order — LOOPSNHOOKS">
        <button type="submit" class="btn-primary" id="submitOrderBtn">Send order</button>
      </form>
    </div>
    <div class="confirmation" id="confirmationBox" style="display:none;">
      <div class="check">✓</div>
      <h3>Order placed!</h3>
      <p>LOOPSNHOOKS will contact you on WhatsApp to confirm availability, pricing, and delivery.</p>
      <a class="wa-inline-link" href="https://wa.me/918238841842" target="_blank" rel="noopener">💬 Chat on WhatsApp</a>
    </div>
  </div>
</div>

<script>
/* ====================== CONFIG ====================== */
// ⚠️ REPLACE THIS with your real Formspree endpoint (sign up free at https://formspree.io,
// create a form, and paste the "https://formspree.io/f/xxxxxxxx" URL here).
// The URL provided in the brief (form.typeform.com/to/gcz5MNUI) is a Typeform link, not a
// Formspree endpoint, so it will NOT work for this integration.
const FORMSPREE_ENDPOINT = "https://formspree.io/f/YOUR_FORM_ID";
const WHATSAPP_NUMBER = "918238841842"; // no + or spaces, for wa.me links

/* ====================== PRODUCT DATA ======================
   Images marked PLACEHOLDER need to be swapped for real imgbb.com URLs.
*/
const PRODUCTS = [
  { id:1, name:"Flower Bouquet", price:580, category:"FLOWERS",
    img:"https://i.ibb.co/xq7xGN4F/Whats-App-Image-2026-06-24-at-11-02-43-AM.jpg",
    desc:"Handmade with love" },
  { id:2, name:"Mini Sunflower Bouquet", price:280, category:"FLOWERS",
    img:"https://i.ibb.co/wZ8QZd1s/Whats-App-Image-2026-06-13-at-6-59-00-PM.jpg",
    desc:"Handmade with love" },
  { id:3, name:"Rose Bunch Bouquet", price:450, category:"FLOWERS",
    img:"https://placehold.co/600x600/F5E3E7/A8455E?text=Rose+Bunch%0A(PLACEHOLDER)",
    desc:"Soft pastel roses, forever fresh" },
  { id:4, name:"Crochet Tote Bag — Sage", price:650, category:"CROCHET BAGS",
    img:"https://i.ibb.co/wrLCFBSN/Whats-App-Image-2026-06-13-at-6-51-43-PM.jpg",
    desc:"Sturdy everyday tote, lined inside" },
  { id:5, name:"Crochet Market Bag — Cream", price:720, category:"CROCHET BAGS",
    img:"https://placehold.co/600x600/EFE8DA/6E8570?text=Market+Bag%0A(PLACEHOLDER)",
    desc:"Roomy net-weave for groceries" },
  { id:6, name:"Mini Crossbody Bag", price:520, category:"CROCHET BAGS",
    img:"https://placehold.co/600x600/EFE8DA/6E8570?text=Crossbody%0A(PLACEHOLDER)",
    desc:"Compact bag with adjustable strap" },
  { id:7, name:"Crochet Beanie", price:350, category:"CROCHET WINTER ESSENTIALS",
    img:"https://placehold.co/600x600/E8E2F0/8A3750?text=Beanie%0A(PLACEHOLDER)",
    desc:"Chunky-knit warmth for cold mornings" },
  { id:8, name:"Crochet Scarf", price:480, category:"CROCHET WINTER ESSENTIALS",
    img:"https://placehold.co/600x600/E8E2F0/8A3750?text=Scarf%0A(PLACEHOLDER)",
    desc:"Long wrap scarf, soft yarn blend" },
  { id:9, name:"Crochet Mittens", price:300, category:"CROCHET WINTER ESSENTIALS",
    img:"https://placehold.co/600x600/E8E2F0/8A3750?text=Mittens%0A(PLACEHOLDER)",
    desc:"Cosy pair, one size fits most" },
  { id:10, name:"Crochet Keychain Gift Set", price:150, category:"GIFTS",
    img:"https://placehold.co/600x600/F3EAD5/C79A46?text=Keychains%0A(PLACEHOLDER)",
    desc:"Set of 3 mini amigurumi keychains" },
  { id:11, name:"Crochet Photo Frame", price:380, category:"GIFTS",
    img:"https://placehold.co/600x600/F3EAD5/C79A46?text=Photo+Frame%0A(PLACEHOLDER)",
    desc:"Handframed keepsake for a favourite photo" },
  { id:12, name:"Amigurumi Bear", price:420, category:"GIFTS",
    img:"https://placehold.co/600x600/F3EAD5/C79A46?text=Amigurumi+Bear%0A(PLACEHOLDER)",
    desc:"Soft toy bear, hand-stitched details" },
];

const CATEGORIES = ["ALL", ...Array.from(new Set(PRODUCTS.map(p=>p.category)))];

/* ====================== STATE ====================== */
let cart = JSON.parse(localStorage.getItem("loopsnhooks_cart") || "{}");
let activeCategory = "ALL";

function saveCart(){
  localStorage.setItem("loopsnhooks_cart", JSON.stringify(cart));
  renderCartBadge();
}
function cartCount(){
  return Object.values(cart).reduce((s,i)=>s+i.qty,0);
}
function cartTotal(){
  return Object.values(cart).reduce((s,i)=>s+i.qty*i.price,0);
}

/* ====================== RENDER: FILTERS ====================== */
const filtersEl = document.getElementById("filters");
function renderFilters(){
  filtersEl.innerHTML = "";
  CATEGORIES.forEach(cat=>{
    const btn = document.createElement("button");
    btn.className = "filter-btn" + (cat===activeCategory ? " active":"");
    btn.textContent = cat;
    btn.addEventListener("click", ()=>{
      activeCategory = cat;
      renderFilters();
      renderGrid();
    });
    filtersEl.appendChild(btn);
  });
}

/* ====================== RENDER: GRID ====================== */
const gridEl = document.getElementById("grid");
function renderGrid(){
  const items = activeCategory==="ALL" ? PRODUCTS : PRODUCTS.filter(p=>p.category===activeCategory);
  gridEl.innerHTML = "";
  if(items.length===0){
    gridEl.innerHTML = `<div class="empty-state">No products in this category yet.</div>`;
    return;
  }
  items.forEach(p=>{
    const card = document.createElement("article");
    card.className = "card";
    card.innerHTML = `
      <div class="card-img-wrap">
        <img src="${p.img}" alt="${p.name} — ${p.desc}" loading="lazy">
      </div>
      <div class="card-body">
        <span class="card-cat">${p.category}</span>
        <h3 class="card-name">${p.name}</h3>
        <p class="card-desc">"${p.desc}"</p>
        <div class="card-footer">
          <span class="card-price price">₹${p.price}</span>
          <button class="add-btn" data-id="${p.id}">Add to cart</button>
        </div>
      </div>
    `;
    gridEl.appendChild(card);
  });
  gridEl.querySelectorAll(".add-btn").forEach(btn=>{
    btn.addEventListener("click", (e)=>{
      addToCart(parseInt(btn.dataset.id));
      btn.textContent = "Added ✓";
      btn.classList.add("added");
      setTimeout(()=>{ btn.textContent="Add to cart"; btn.classList.remove("added"); }, 900);
    });
  });
}

function addToCart(id){
  const p = PRODUCTS.find(x=>x.id===id);
  if(!p) return;
  if(cart[id]){ cart[id].qty += 1; }
  else{ cart[id] = { id:p.id, name:p.name, price:p.price, img:p.img, qty:1 }; }
  saveCart();
  bumpCartFab();
}
function bumpCartFab(){
  const fab = document.getElementById("cartFab");
  fab.style.transform = "scale(1.15)";
  setTimeout(()=>{ fab.style.transform = "scale(1)"; }, 160);
}

/* ====================== RENDER: CART BADGE ====================== */
function renderCartBadge(){
  const badge = document.getElementById("cartBadge");
  const count = cartCount();
  if(count>0){
    badge.style.display = "flex";
    badge.textContent = count;
  } else {
    badge.style.display = "none";
  }
}

/* ====================== RENDER: CART DRAWER ====================== */
const cartItemsEl = document.getElementById("cartItems");
const cartFooterEl = document.getElementById("cartFooter");
function renderCartDrawer(){
  const entries = Object.values(cart);
  if(entries.length===0){
    cartItemsEl.innerHTML = `<div class="cart-empty">Your basket is empty.<br>Add a handmade favourite!</div>`;
    cartFooterEl.style.display = "none";
    return;
  }
  cartFooterEl.style.display = "block";
  cartItemsEl.innerHTML = "";
  entries.forEach(item=>{
    const row = document.createElement("div");
    row.className = "cart-item";
    row.innerHTML = `
      <img src="${item.img}" alt="${item.name}" loading="lazy">
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-price">₹${item.price} each</div>
        <div class="qty-row">
          <button class="qty-btn" data-action="dec" data-id="${item.id}" aria-label="Decrease quantity">−</button>
          <span class="qty-num">${item.qty}</span>
          <button class="qty-btn" data-action="inc" data-id="${item.id}" aria-label="Increase quantity">+</button>
          <button class="remove-link" data-action="rm" data-id="${item.id}">Remove</button>
        </div>
      </div>
      <div class="item-subtotal price">₹${item.qty*item.price}</div>
    `;
    cartItemsEl.appendChild(row);
  });
  document.getElementById("grandTotal").textContent = "₹" + cartTotal();

  cartItemsEl.querySelectorAll("[data-action]").forEach(btn=>{
    btn.addEventListener("click", ()=>{
      const id = parseInt(btn.dataset.id);
      const action = btn.dataset.action;
      if(action==="inc") cart[id].qty += 1;
      if(action==="dec"){ cart[id].qty -= 1; if(cart[id].qty<=0) delete cart[id]; }
      if(action==="rm") delete cart[id];
      saveCart();
      renderCartDrawer();
    });
  });
}

/* ====================== DRAWER / OVERLAY CONTROLS ====================== */
const overlay = document.getElementById("overlay");
const cartDrawer = document.getElementById("cartDrawer");
const checkoutDrawer = document.getElementById("checkoutDrawer");

function openDrawer(drawer){
  overlay.classList.add("open");
  drawer.classList.add("open");
}
function closeDrawers(){
  overlay.classList.remove("open");
  cartDrawer.classList.remove("open");
  checkoutDrawer.classList.remove("open");
}
overlay.addEventListener("click", closeDrawers);
document.getElementById("cartFab").addEventListener("click", ()=>{
  renderCartDrawer();
  openDrawer(cartDrawer);
});
document.getElementById("closeCart").addEventListener("click", closeDrawers);
document.getElementById("closeCheckout").addEventListener("click", closeDrawers);

/* ====================== CHECKOUT FLOW ====================== */
document.getElementById("checkoutBtn").addEventListener("click", ()=>{
  buildOrderSummary();
  cartDrawer.classList.remove("open");
  document.getElementById("checkoutFormWrap").style.display = "block";
  document.getElementById("confirmationBox").style.display = "none";
  openDrawer(checkoutDrawer);
});

function buildOrderSummary(){
  const entries = Object.values(cart);
  const box = document.getElementById("orderSummaryBox");
  let text = "";
  entries.forEach(item=>{
    text += `${item.name} x${item.qty} — ₹${item.qty*item.price}\n`;
  });
  const total = cartTotal();
  text += `\nGrand Total: ₹${total}`;

  box.innerHTML = "";
  entries.forEach(item=>{
    const row = document.createElement("div");
    row.innerHTML = `<span>${item.name} × ${item.qty}</span><span>₹${item.qty*item.price}</span>`;
    box.appendChild(row);
  });
  const totalRow = document.createElement("div");
  totalRow.style.fontWeight = "700";
  totalRow.style.marginTop = "6px";
  totalRow.style.borderTop = "1px dashed var(--line)";
  totalRow.style.paddingTop = "6px";
  totalRow.innerHTML = `<span>Grand Total</span><span>₹${total}</span>`;
  box.appendChild(totalRow);

  document.getElementById("orderSummaryField").value = text;
  document.getElementById("grandTotalField").value = "₹" + total;
}

document.getElementById("orderForm").addEventListener("submit", async (e)=>{
  e.preventDefault();
  const btn = document.getElementById("submitOrderBtn");
  btn.disabled = true;
  btn.textContent = "Sending...";

  const form = e.target;
  const formData = new FormData(form);

  try{
    const res = await fetch(FORMSPREE_ENDPOINT, {
      method: "POST",
      body: formData,
      headers: { "Accept": "application/json" }
    });

    if(res.ok){
      cart = {};
      saveCart();
      form.reset();
      document.getElementById("checkoutFormWrap").style.display = "none";
      document.getElementById("confirmationBox").style.display = "block";
    } else {
      alert("Something went wrong sending your order. Please try again, or message us directly on WhatsApp.");
    }
  } catch(err){
    alert("Could not reach the order form. Check your connection, or message us directly on WhatsApp.");
  } finally {
    btn.disabled = false;
    btn.textContent = "Send order";
  }
});

/* ====================== INIT ====================== */
renderFilters();
renderGrid();
renderCartBadge();
</script>
</body>
</html>
