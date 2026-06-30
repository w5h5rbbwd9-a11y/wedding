// ===============================
// Таймер до свадьбы
// ===============================

const weddingDate = new Date("July 24, 2026 15:00:00").getTime();

const timer = document.getElementById("timer");

function updateTimer(){

const now = new Date().getTime();

const distance = weddingDate - now;

if(distance < 0){

timer.innerHTML = "<h2>Сегодня наш счастливый день ❤️</h2>";

return;

}

const days = Math.floor(distance / (1000 * 60 * 60 * 24));

const hours = Math.floor((distance % (1000*60*60*24))/(1000*60*60));

const minutes = Math.floor((distance % (1000*60*60))/(1000*60));

const seconds = Math.floor((distance % (1000*60))/1000);

timer.innerHTML = `

<div class="time-box">
<span>${days}</span>
<span>дней</span>
</div>

<div class="time-box">
<span>${hours}</span>
<span>часов</span>
</div>

<div class="time-box">
<span>${minutes}</span>
<span>минут</span>
</div>

<div class="time-box">
<span>${seconds}</span>
<span>секунд</span>
</div>

`;

}

updateTimer();

setInterval(updateTimer,1000);


// ===============================
// Плавное появление блоков
// ===============================

const sections = document.querySelectorAll(".section,.gallery,.countdown");

const observer = new IntersectionObserver((entries)=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.classList.add("show");

}

});

},{
threshold:0.2
});

sections.forEach(section=>{

observer.observe(section);

});


// ===============================
// Небольшая анимация кнопки
// ===============================

const button=document.querySelector("button");

button.addEventListener("mouseenter",()=>{

button.style.transform="scale(1.05)";

});

button.addEventListener("mouseleave",()=>{

button.style.transform="scale(1)";

});


// ===============================
// Параллакс первого экрана
// ===============================

window.addEventListener("scroll",()=>{

const hero=document.querySelector(".hero");

hero.style.backgroundPositionY=window.scrollY*0.4+"px";

});


// ===============================
// Плавное увеличение фото
// ===============================

const gallery=document.querySelectorAll(".gallery img");

gallery.forEach(img=>{

img.addEventListener("click",()=>{

img.classList.toggle("zoom");

});

});
