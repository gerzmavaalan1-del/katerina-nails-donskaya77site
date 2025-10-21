<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Knails ⚡ — Katerina Nails</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
:root{
  --bg:#fdf8f6;
  --primary:#d9b6b0;
  --secondary:#fff4f2;
  --text:#2b2b2b;
  --muted:#8f8a88;
  --accent:#e28c8c;
  --shadow:0 10px 25px rgba(0,0,0,0.07);
  --radius:14px;
}

*{box-sizing:border-box;margin:0;padding:0;}
html,body{height:100%;scroll-behavior:smooth;font-family:'Roboto',sans-serif;background:var(--bg);color:var(--text);}
a{text-decoration:none;color:inherit;}
img{display:block;width:100%;height:auto;border-radius:var(--radius);}

.lightning-bg{position:fixed;top:0;left:0;width:100%;height:100%;pointer-events:none;z-index:0;}
.lightning{position:absolute;font-size:20px;opacity:0.06;animation:flash 12s ease-in-out infinite;}
.star{position:absolute;font-size:16px;opacity:0.04;animation:twinkle 15s ease-in-out infinite;}

@keyframes flash{0%,100%{opacity:0.05;transform:scale(1)}50%{opacity:0.14;transform:scale(1.1)}}
@keyframes twinkle{0%,100%{opacity:0.04;transform:scale(1)}50%{opacity:0.09;transform:scale(1.06)}}

.logo-title{text-align:center;font-family:'Playfair Display',serif;font-size:80px;font-weight:700;color:var(--primary);margin:40px 0 20px;letter-spacing:4px;z-index:2;position:relative;}

.search-container{display:flex;justify-content:center;margin-bottom:30px;position:relative;z-index:2;}
.search-bar{display:flex;align-items:center;background:white;border-radius:50px;padding:10px 25px;box-shadow:var(--shadow);border:1px solid rgba(217,182,176,0.6);transition:all 0.3s;}
.search-bar:focus-within{box-shadow:0 8px 25px rgba(217,182,176,0.25);border-color:var(--primary);}
.search-bar input{border:none;outline:none;background:transparent;flex:1;font-size:16px;color:var(--text);}
.search-results{position:absolute;top:105%;left:50%;transform:translateX(-50%);width:320px;background:white;border-radius:var(--radius);box-shadow:0 10px 25px rgba(0,0,0,0.15);margin-top:5px;display:none;max-height:300px;overflow-y:auto;z-index:10;}
.search-result-item{padding:14px 18px;border-bottom:1px solid rgba(200,190,185,0.3);cursor:pointer;transition:background 0.2s;}
.search-result-item:hover{background:rgba(217,182,176,0.1);}
.search-result-title{font-weight:600;margin-bottom:4px;}
.search-result-price{color:var(--primary);font-weight:700;font-size:14px;}
.search-result-type{font-size:12px;color:var(--muted);background:rgba(217,182,176,0.1);padding:2px 6px;border-radius:10px;display:inline-block;margin-top:4px;}

.container{max-width:1200px;margin:0 auto;padding:20px;position:relative;z-index:2;}
.main-grid{display:grid;grid-template-columns:1fr 350px;gap:20px;}
.paper{background:var(--secondary);border-radius:var(--radius);padding:20px;box-shadow:var(--shadow);border:1px solid rgba(200,190,185,0.5);position:relative;overflow:hidden;transition:transform 0.3s;}
.paper:hover{transform:translateY(-5px) scale(1.01);}
.pin{position:absolute;top:12px;right:12px;background:var(--primary);color:white;padding:6px 10px;border-radius:10px;font-size:14px;}

.services-columns{display:grid;grid-template-columns:repeat(2,1fr);gap:16px;margin-top:18px;}
.note{background:linear-gradient(180deg,rgba(255,255,255,0.85),rgba(250,244,242,0.9));padding:22px;display:flex;flex-direction:column;justify-content:center;position:relative;cursor:pointer;border-radius:var(--radius);border:1px solid rgba(200,190,185,0.3);box-shadow:0 5px 15px rgba(0,0,0,0.03);transition:all 0.3s;}
.note:hover{transform:translateY(-8px) rotate(-0.3deg) scale(1.02);box-shadow:0 12px 25px rgba(0,0,0,0.06);}
.note-title{font-family:'Playfair Display',serif;font-size:20px;font-weight:600;margin-bottom:6px;}
.note-sub{color:var(--muted);font-style:italic;margin-bottom:8px;}
.note-price{color:var(--primary);font-weight:700;font-size:20px;margin-left:auto;}
.pin-small{position:absolute;top:12px;left:12px;background:rgba(255,255,255,0.85);border-radius:50%;width:32px;height:32px;display:flex;align-items:center;justify-content:center;box-shadow:0 4px 8px rgba(0,0,0,0.05);}

.contact-card{text-align:center;padding:20px;display:flex;flex-direction:column;gap:15px;}
.contact-btn{display:flex;flex-direction:column;align-items:center;gap:6px;text-decoration:none;padding:14px;background:linear-gradient(180deg,#fff,#fbf7f5);border-radius:var(--radius);box-shadow:var(--shadow);border:1px solid rgba(200,190,185,0.5);transition:transform 0.25s ease;color:var(--text);}
.contact-btn:hover{transform:translateY(-6px);}
.contact-btn i{font-size:28px;color:var(--primary);}
.contact-btn span{font-weight:600;font-size:14px;}

.portfolio-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:15px;}
.portfolio-item img{transition:transform 0.6s ease;}
.portfolio-item:hover img{transform:scale(1.08);}

.master-photo img{filter:brightness(1.05) contrast(1.05);}
.master-info .highlight{background:rgba(217,182,176,0.1);padding:10px;border-radius:8px;font-size:14px;}
.inspiration-text{font-style:italic;line-height:1.6;margin:15px 0;padding:15px;background:rgba(217,182,176,0.05);border-radius:10px;border-left:3px solid var(--primary);}

footer{margin-top:40px;text-align:center;color:var(--muted);font-size:14px;padding:40px 0;}

.modal{display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.55);z-index:1000;justify-content:center;align-items:center;}
.modal-content{background:var(--secondary);padding:30px;border-radius:var(--radius);max-width:500px;width:90%;position:relative;animation:fadeIn 0.3s;box-shadow:var(--shadow);}
.close-modal{position:absolute;top:15px;right:15px;font-size:24px;cursor:pointer;background:var(--primary);color:white;width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;border:none;}
.contact-options{display:flex;flex-direction:column;gap:15px;margin:25px 0;}
.contact-option{display:flex;align-items:center;padding:15px;background:#f8f4f0;border-radius:var(--radius);text-decoration:none;color:var(--text);transition:background 0.3s;}
.contact-option:hover{background:#eee6de;}
.contact-option i{margin-right:15px;font-size:24px;color:var(--primary);}
.promo-section{margin-top:20px;padding-top:20px;border-top:1px solid rgba(200,190,185,0.6);}
.promo-codes{display:flex;flex-wrap:wrap;gap:10px;}
.promo-code{padding:8px 15px;background:#f0e9e3;border-radius:6px;font-size:14px;font-weight:500;position:relative;}
.promo-discount{position:absolute;top:-8px;right:-8px;background:var(--primary);color:white;font-size:10px;padding:2px 6px;border-radius:10px;font-weight:600;}

@keyframes fadeIn{from{opacity:0;transform:translateY(-20px);}to{opacity:1;transform:translateY(0);}}

@media(max-width:900px){.main-grid{grid-template-columns:1fr;}.services-columns{grid-template-columns:1fr;}.logo-title{font-size:60px;}.about-master{flex-direction:column;}.master-photo{width:100%;max-width:300px;margin:0 auto;}.master-highlights{grid-template-columns:1fr;}}
@media(max-width:480px){.portfolio-grid{grid-template-columns:1fr;}.logo-title{font-size:40px;}.search-bar{width:250px;}}
</style>
</head>
<body>

<div class="lightning-bg" id="lightning-bg"></div>

<div class="logo-title">Knails ⚡</div>

<div class="search-container">
  <div class="search-bar">
    <input type="text" id="search-input" placeholder="Поиск услуг и промокодов...">
    <i class="fas fa-search" style="color: var(--primary);"></i>
  </div>
  <div class="search-results" id="search-results"></div>
</div>

<main class="container">
  <div class="main-grid">
    <div>
      <!-- Услуги и цены -->
      <div class="paper">
        <div style="display:flex;align-items:center;justify-content:space-between;">
          <h2 style="font-family:'Playfair Display', serif;">Услуги и цены</h2>
          <div class="pin">📌</div>
        </div>
        <div class="services-columns">
          <div class="note" data-service="Наращивание/Коррекция">
            <div class="pin-small">📌</div>
            <div style="display:flex;justify-content:space-between;align-items:center;">
              <div><div class="note-title">Наращивание/Коррекция</div><div class="note-sub">(макс. длина 4)</div></div>
              <div class="note-price">1.900₽</div>
            </div>
          </div>
          <div class="note" data-service="Гель-лак">
            <div class="pin-small">📌</div>
            <div style="display:flex;justify-content:space-between;align-items:center;">
              <div class="note-title">Гель-лак</div>
              <div class="note-price">1.500₽</div>
            </div>
          </div>
          <div class="note" data-service="Маникюр без покрытия">
            <div class="pin-small">📌</div>
            <div style="display:flex;justify-content:space-between;align-items:center;">
              <div class="note-title">Маникюр без покрытия</div>
              <div class="note-price">800₽</div>
            </div>
          </div>
          <div class="note" data-service="Снятие чужой работы">
            <div class="pin-small">📌</div>
            <div style="display:flex;justify-content:space-between;align-items:center;">
              <div class="note-title">Снятие чужой работы</div>
              <div class="note-price">300₽</div>
            </div>
          </div>
          <div class="note" data-service="Ремонт одного ногтя">
            <div class="pin-small">📌</div>
            <div style="display:flex;justify-content:space-between;align-items:center;">
              <div class="note-title">Ремонт одного ногтя</div>
              <div class="note-price">200₽</div>
            </div>
          </div>
        </div>
      </div>

      <!-- О мастере -->
      <div class="paper" style="margin-top:20px;">
        <h3 style="font-family:'Playfair Display', serif;">Привет! Меня зовут Катя)</h3>
        <div class="about-master" style="gap:20px;align-items:flex-start;">
          <div class="master-photo"><img src="https://i.postimg.cc/BPDmCPcz/IMG-0059.jpg" alt="Катя - мастер маникюра"></div>
          <div class="master-info">
            <p>Я — мастер маникюра с 3-летним опытом</p>
            <div class="master-highlights">
              <div class="highlight">✅ Работаю быстро, без потери качества</div>
              <div class="highlight">✅ Коррекция всего за 1 час</div>
              <div class="highlight">✅ Исправляю «проблемные» ногти</div>
              <div class="highlight">✅ Стойкий и эстетичный результат</div>
            </div>
            <div class="inspiration-text">
              Моя цель — создавать не просто маникюр, а настоящее произведение искусства, которое будет радовать вас каждый день. Красивые ухоженные ногти — важная часть уверенности и самовыражения.
            </div>
            <p>📍Запись в ЛС / по номеру телефона 89881605058</p>
            <p>📆 Места быстро разбирают — не откладывай красоту</p>
            <a href="https://www.instagram.com/kateina_nails" class="contact-btn" target="_blank" style="background:var(--primary);color:white;font-weight:700;margin-top:10px;">Мой Instagram</a>
          </div>
        </div>
      </div>

      <!-- Портфолио -->
      <div class="paper" style="margin-top:20px;">
        <h3 style="font-family:'Playfair Display', serif;">Портфолио</h3>
        <div class="portfolio-grid">
          <a class="portfolio-item" href="https://ibb.co/NcP7mdB" target="_blank"><img src="https://i.ibb.co/NcP7mdB/IMG-1.jpg" alt="Работа 1"></a>
          <a class="portfolio-item" href="https://ibb.co/k2KZ1ZFY" target="_blank"><img src="https://i.ibb.co/k2KZ1ZFY/IMG-2.jpg" alt="Работа 2"></a>
          <a class="portfolio-item" href="https://ibb.co/JR9g2K6w" target="_blank"><img src="https://i.ibb.co/JR9g2K6w/IMG-3.jpg" alt="Работа 3"></a>
          <a class="portfolio-item" href="https://ibb.co/9HXtBzt0" target="_blank"><img src="https://i.ibb.co/9HXtBzt0/IMG-4.jpg" alt="Работа 4"></a>
        </div>
      </div>
    </div>

    <!-- Sidebar -->
    <aside>
      <div class="paper">
        <div class="contact-card">
          <h3>Связаться со мной</h3>
          <div class="contacts">
            <a class="contact-btn" href="https://www.instagram.com/kateina_nails" target="_blank"><i class="fab fa-instagram"></i><span>Instagram</span></a>
            <a class="contact-btn" href="https://t.me/Lazaryan0" target="_blank"><i class="fab fa-telegram"></i><span>Telegram</span></a>
            <a class="contact-btn" href="https://wa.me/79881605058" target="_blank"><i class="fab fa-whatsapp"></i><span>WhatsApp</
            </span></a>
          </div>

          <div style="margin-top:20px; font-size:14px; color:var(--muted); text-align:left;">
            <strong>Промокоды:</strong>
            <div style="margin-top:5px;">
              <strong style="color:var(--primary)">NAILS10</strong> - скидка 10%<br>
              <strong style="color:var(--primary)">FIRSTVISIT</strong> - первое посещение -10%<br>
              <strong style="color:var(--primary)">KATEINA15</strong> - скидка 15%
            </div>
          </div>

          <div style="margin-top:15px; display:flex; gap:10px; justify-content:center;">
            <button onclick="scrollToSection('portfolio')" style="padding:8px 12px; border-radius:12px; border:1px solid rgba(200,190,185,0.6); background:transparent; color:var(--text); font-weight:600; cursor:pointer;">Портфолио</button>
            <button onclick="openBookingModal()" style="padding:8px 12px; border-radius:12px; background:var(--primary); color:white; font-weight:700; border:none; cursor:pointer;">Записаться</button>
          </div>
        </div>
      </div>
    </aside>
  </div>
</main>

<!-- Модальное окно -->
<div class="modal" id="booking-modal">
  <div class="modal-content">
    <button class="close-modal">&times;</button>
    <h2 style="font-family:'Playfair Display', serif; margin-bottom:10px;">Записаться на услугу</h2>
    <p style="color:var(--muted);">Выберите удобный способ связи для записи:</p>
    <div class="contact-options">
      <a href="https://t.me/Lazaryan0" class="contact-option" target="_blank">
        <i class="fab fa-telegram"></i>
        <div>
          <strong>Telegram</strong><br>@Lazaryan0
        </div>
      </a>
      <a href="https://wa.me/79881605058" class="contact-option" target="_blank">
        <i class="fab fa-whatsapp"></i>
        <div>
          <strong>WhatsApp</strong><br>+7 988 160 50 58
        </div>
      </a>
    </div>
    <div class="promo-section">
      <h3 style="font-family:'Playfair Display', serif; margin-bottom:15px;">Промокоды для скидок</h3>
      <div class="promo-codes">
        <div class="promo-code">NAILS10<div class="promo-discount">-10%</div></div>
        <div class="promo-code">KATEINA15<div class="promo-discount">-15%</div></div>
        <div class="promo-code">FIRSTVISIT<div class="promo-discount">-10%</div></div>
      </div>
      <p style="margin-top:15px; font-size:14px; color:var(--muted);">
        <strong>NAILS10</strong> - скидка 10% на любую услугу<br>
        <strong>FIRSTVISIT</strong> - скидка 10% на первое посещение<br>
        <strong>KATEINA15</strong> - скидка 15% на комплекс услуг
      </p>
    </div>
  </div>
</div>

<footer class="container">
  <p>Katerina Nails © 2025 — Все права защищены</p>
</footer>

<script>
// Lightning and stars background
function createBackgroundElements(){
  const cont = document.getElementById('lightning-bg');
  const lightningPos=[{l:'15%',t:'20%',d:'0s',dur:'14s'},{l:'75%',t:'65%',d:'3s',dur:'16s'},{l:'30%',t:'80%',d:'7s',dur:'12s'},{l:'85%',t:'25%',d:'10s',dur:'15s'}];
  lightningPos.forEach(pos=>{
    const el=document.createElement('div');el.className='lightning';el.style.left=pos.l;el.style.top=pos.t;el.style.animationDelay=pos.d;el.style.animationDuration=pos.dur;el.textContent='⚡';cont.appendChild(el);
  });
  const starPos=[{l:'10%',t:'10%',d:'2s',dur:'18s'},{l:'90%',t:'15%',d:'5s',dur:'20s'},{l:'20%',t:'90%',d:'8s',dur:'16s'},{l:'80%',t:'85%',d:'12s',dur:'22s'}];
  const starChars=['★','☆','✦','✧'];
  starPos.forEach((pos,i)=>{
    const el=document.createElement('div');el.className='star';el.style.left=pos.l;el.style.top=pos.t;el.style.animationDelay=pos.d;el.style.animationDuration=pos.dur;el.textContent=starChars[i];cont.appendChild(el);
  });
}
createBackgroundElements();

// Search functionality
const searchData=[
  {title:"Наращивание/Коррекция",price:"1.900₽",type:"услуга",description:"макс. длина 4"},
  {title:"Гель-лак",price:"1.500₽",type:"услуга",description:""},
  {title:"Маникюр без покрытия",price:"800₽",type:"услуга",description:""},
  {title:"Снятие чужой работы",price:"300₽",type:"услуга",description:""},
  {title:"Ремонт одного ногтя",price:"200₽",type:"услуга",description:""},
  {title:"NAILS10",price:"скидка 10%",type:"промокод",description:"на любую услугу"},
  {title:"FIRSTVISIT",price:"скидка 10%",type:"промокод",description:"первое посещение"},
  {title:"KATEINA15",price:"скидка 15%",type:"промокод",description:"на комплекс услуг"}
];
const searchInput=document.getElementById('search-input');
const searchResults=document.getElementById('search-results');

searchInput.addEventListener('input',function(){
  const query=this.value.toLowerCase().trim();
  searchResults.innerHTML='';
  if(query.length<2){searchResults.style.display='none';return;}
  const filtered=searchData.filter(item=>item.title.toLowerCase().includes(query)||item.description.toLowerCase().includes(query)||item.price.toLowerCase().includes(query));
  if(filtered.length>0){
    filtered.forEach(item=>{
      const div=document.createElement('div');div.className='search-result-item';
      div.innerHTML=`<div class="search-result-title">${item.title}</div><div class="search-result-price">${item.price}</div><div class="search-result-type">${item.type}</div>${item.description?`<div style="font-size:12px;color:var(--muted);margin-top:3px;">${item.description}</div>`:''}`;
      div.addEventListener('click',function(){searchInput.value=item.title;searchResults.style.display='none';if(item.type==='услуга')openBookingModal(item.title);});
      searchResults.appendChild(div);
    });
    searchResults.style.display='block';
  } else searchResults.style.display='none';
});
document.addEventListener('click',function(e){if(!e.target.closest('.search-container'))searchResults.style.display='none';});

// Modal
const modal=document.getElementById('booking-modal');
const closeModal=document.querySelector('.close-modal');
const notes=document.querySelectorAll('.note');
function openBookingModal(service=''){if(service){modal.querySelector('h2').textContent=`Записаться на ${service}`;}modal.style.display='flex';}
notes.forEach(note=>note.addEventListener('click',()=>openBookingModal(note.dataset.service)));
closeModal.addEventListener('click',()=>modal.style.display='none');
window.addEventListener('click',e=>{if(e.target===modal)modal.style.display='none';});

// Scroll
function scrollToSection(id){const el=document.getElementById(id);if(el)el.scrollIntoView({behavior:'smooth'});}
document.querySelector('.portfolio-grid').parentElement.parentElement.id='portfolio';
</script>

</body>
</html>
