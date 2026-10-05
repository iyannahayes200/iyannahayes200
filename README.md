## Sonjas Garden
[index (1) (9).html](https://github.com/user-attachments/files/33077350/index.1.9.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sonja's Letters Garden & Café 🌸</title>
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Quicksand:wght@500;700&family=Sacramento&display=swap" rel="stylesheet">
<style>
:root {
--cafe-milk: #FFFDF9;
--cafe-cream: #FDF3E7;
--pastel-pink: #FFD1DC;
--strawberry-blush: #FFA6BC;
--sage-green: #2E5A44;
--sage-light: #527E67;
--accent-rose: #E88EA7;
}

* {
box-sizing: border-box;
margin: 0;
padding: 0;
}

body {
font-family: 'Quicksand', sans-serif;
background-color: var(--pastel-pink);
color: var(--sage-green);
min-height: 100vh;
display: flex;
justify-content: center;
align-items: center;
overflow-x: hidden;
position: relative;
}

/* Background floating decorations */
.bg-decorations {
position: fixed;
width: 100vw;
height: 100vh;
top: 0;
left: 0;
pointer-events: none;
z-index: 1;
overflow: hidden;
}

.floating-item {
position: absolute;
bottom: -50px;
font-size: 24px;
opacity: 0.6;
animation: floatUp 8s infinite linear;
}

@keyframes floatUp {
0% {
transform: translateY(0) translateX(0) rotate(0deg);
opacity: 0;
}
10% { opacity: 0.6; }
90% { opacity: 0.6; }
100% {
transform: translateY(-105vh) translateX(50px) rotate(360deg);
opacity: 0;
}
}

/* Miffy Vector Logo Drawing Component */
.miffy-container {
display: flex;
justify-content: center;
align-items: center;
margin-bottom: 15px;
}

.miffy-vector {
width: 70px;
height: 100px;
position: relative;
background: #FFF;
border: 3px solid var(--sage-green);
border-radius: 35px 35px 30px 30px;
box-shadow: 0 4px 10px rgba(0,0,0,0.05);
}

.miffy-vector::before, .miffy-vector::after {
content: '';
position: absolute;
background: #FFF;
border: 3px solid var(--sage-green);
width: 22px;
height: 50px;
top: -42px;
border-radius: 20px 20px 0 0;
border-bottom: none;
}

.miffy-vector::before { left: 8px; }
.miffy-vector::after { right: 8px; }

.miffy-eyes {
position: absolute;
top: 35px;
left: 16px;
width: 6px;
height: 8px;
background: #000;
border-radius: 50%;
box-shadow: 26px 0 #000;
}

.miffy-mouth {
position: absolute;
top: 48px;
left: 29px;
width: 10px;
height: 10px;
}

.miffy-mouth::before, .miffy-mouth::after {
content: '';
position: absolute;
background: #000;
width: 10px;
height: 2px;
top: 4px;
}
.miffy-mouth::before { transform: rotate(45deg); }
.miffy-mouth::after { transform: rotate(-45deg); }

/* Café Login Screen Container */
#login-screen {
background-color: var(--cafe-milk);
border: 3px solid var(--strawberry-blush);
box-shadow: 0 15px 35px rgba(232, 142, 167, 0.3);
padding: 40px;
border-radius: 30px;
text-align: center;
max-width: 450px;
width: 90%;
z-index: 10;
position: relative;
border-bottom-width: 8px;
}

h1 {
font-family: 'Dancing Script', cursive;
font-size: 2.8rem;
color: var(--sage-green);
margin-bottom: 10px;
}

.subtitle {
font-size: 1rem;
margin-bottom: 25px;
color: var(--sage-light);
font-weight: 500;
}

.mc-input-wrapper {
margin: 20px 0;
}

input[type="password"] {
font-family: 'Quicksand', sans-serif;
font-size: 1.4rem;
width: 100%;
padding: 12px;
text-align: center;
border: 2px solid var(--pastel-pink);
background-color: var(--cafe-cream);
color: var(--sage-green);
outline: none;
border-radius: 20px;
transition: all 0.3s ease;
}

input[type="password"]:focus {
border-color: var(--strawberry-blush);
background-color: #FFF;
}

.mc-btn {
font-family: 'Quicksand', sans-serif;
font-weight: 700;
font-size: 1.2rem;
background-color: var(--strawberry-blush);
color: #FFF;
padding: 12px 25px;
border: none;
cursor: pointer;
border-radius: 20px;
box-shadow: 0 5px 0px var(--accent-rose);
transition: all 0.1s ease;
width: 100%;
margin-top: 15px;
}

.mc-btn:active {
transform: translateY(4px);
box-shadow: 0 1px 0px var(--accent-rose);
}

#error-msg {
color: #D32F2F;
font-weight: 700;
font-size: 1rem;
margin-top: 15px;
display: none;
}

/* Main Whimsical Content Screen Container */
#main-content {
display: none;
width: 95%;
max-width: 850px;
background-color: var(--cafe-milk);
border: 3px solid var(--strawberry-blush);
box-shadow: 0 20px 50px rgba(0,0,0,0.05);
padding: 40px 30px;
border-radius: 40px;
z-index: 10;
margin: 40px 0;
animation: fadeIn 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
border-bottom-width: 10px;
}

@keyframes fadeIn {
from { opacity: 0; transform: scale(0.95) translateY(20px); }
to { opacity: 1; transform: scale(1) translateY(0); }
}

.header-area {
text-align: center;
border-bottom: 3px dashed var(--pastel-pink);
padding-bottom: 25px;
margin-bottom: 35px;
}

.header-area h1 {
font-size: 3.8rem;
margin-bottom: 5px;
}

.lily-banner {
font-family: 'Dancing Script', cursive;
font-size: 1.5rem;
color: var(--sage-light);
margin-top: 5px;
display: flex;
justify-content: center;
align-items: center;
gap: 10px;
}

/* Beautiful Whimsical Menu Button Grid */
.letters-grid {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
gap: 20px;
margin-bottom: 40px;
}

.letter-row-btn {
background: var(--cafe-cream);
border: 2px solid transparent;
padding: 18px;
text-align: left;
font-family: 'Quicksand', sans-serif;
font-size: 1.1rem;
font-weight: 700;
color: var(--sage-green);
cursor: pointer;
display: flex;
align-items: center;
transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
border-radius: 22px;
box-shadow: 0 4px 15px rgba(0,0,0,0.02);
}

.letter-row-btn:hover {
background-color: #FFF;
border-color: var(--strawberry-blush);
transform: translateY(-5px);
box-shadow: 0 10px 20px rgba(255, 166, 188, 0.2);
}

.letter-row-btn .emoji {
font-size: 1.6rem;
margin-right: 15px;
background: #FFF;
padding: 8px;
border-radius: 15px;
box-shadow: 0 4px 8px rgba(0,0,0,0.02);
}

/* Whimsical 3D Envelope Unfolding Mechanics */
.envelope-wrapper {
display: none;
perspective: 1000px;
margin: 40px auto 20px auto;
width: 100%;
max-width: 600px;
animation: slideDown 0.4s ease-out forwards;
}

@keyframes slideDown {
from { opacity: 0; transform: translateY(-20px); }
to { opacity: 1; transform: translateY(0); }
}

.envelope {
position: relative;
width: 100%;
height: 220px;
background: var(--cafe-cream);
border-radius: 0 0 20px 20px;
box-shadow: 0 15px 30px rgba(0,0,0,0.06);
margin-top: 100px;
transition: transform 0.5s;
border: 2px solid var(--strawberry-blush);
border-top: none;
}

.envelope-flap {
position: absolute;
top: -100px;
left: -2px;
width: calc(100% + 4px);
height: 100px;
background: var(--cafe-cream);
border: 2px solid var(--strawberry-blush);
border-bottom: none;
clip-path: polygon(0% 100%, 50% 0%, 100% 100%);
transform-origin: bottom;
transition: transform 0.6s ease-in-out;
z-index: 3;
}

.envelope.open .envelope-flap {
transform: rotateX(180deg) translateY(2px);
z-index: 1;
}

/* Slide Out Reading Stationery Paper */
.letter-paper {
position: absolute;
top: 10px;
left: 5%;
width: 90%;
background: #FFF;
border-radius: 20px;
padding: 30px;
box-shadow: 0 5px 20px rgba(0,0,0,0.05);
transition: all 0.8s cubic-bezier(0.19, 1, 0.22, 1);
z-index: 2;
opacity: 0;
transform: translateY(0);
border: 2px dashed var(--pastel-pink);
height: auto;
pointer-events: none;
}

.envelope.open .letter-paper {
opacity: 1;
transform: translateY(-260px);
position: relative;
z-index: 5;
pointer-events: auto;
box-shadow: 0 10px 40px rgba(0,0,0,0.08);
margin-bottom: -150px;
}

.letter-paper-header {
text-align: center;
margin-bottom: 20px;
border-bottom: 2px solid var(--cafe-cream);
padding-bottom: 15px;
}

#letter-title {
font-family: 'Dancing Script', cursive;
font-size: 2.2rem;
color: var(--sage-green);
margin-top: 10px;
}

#letter-body {
font-size: 1.15rem;
line-height: 1.8;
color: var(--sage-green);
white-space: pre-wrap;
font-weight: 500;
}

/* Beautiful Dashboard Footer Sign-off */
.footer-sig {
text-align: center;
margin-top: 50px;
font-family: 'Dancing Script', cursive;
font-size: 2.2rem;
border-top: 3px dashed var(--pastel-pink);
padding-top: 25px;
color: var(--sage-green);
}

.cafe-heart {
color: var(--strawberry-blush);
display: inline-block;
animation: pulse 1.5s infinite;
margin: 0 5px;
}

@keyframes pulse {
0%, 100% { transform: scale(1); }
50% { transform: scale(1.2); }
}
</style>
</head>
<body>

<div class="bg-decorations" id="bg-items"></div>

<!-- Gate Passcode Screen Box -->
<div id="login-screen">
    <div class="miffy-container">
        <div class="miffy-vector">
            <div class="miffy-eyes"></div>
            <div class="miffy-mouth"></div>
        </div>
    </div>
    <h1>Enter Secret Code</h1>
    <p class="subtitle">(Our birthdays MM/DD then the day we met one another!)</p>
    <div class="mc-input-wrapper">
        <input type="password" id="passcode-input" placeholder="••••••••••••" autocomplete="off">
    </div>
    <button class="mc-btn" onclick="checkCode()">UNLOCK LETTERS</button>
    <div id="error-msg">Incorrect code, try again my love! 💕</div>
</div>

<!-- Main Café / Garden Experience Frame -->
<div id="main-content">
    <div class="header-area">
        <div class="miffy-container">
            <div class="miffy-vector">
                <div class="miffy-eyes"></div>
                <div class="miffy-mouth"></div>
            </div>
        </div>
        <h1>Sonja's Letters Garden</h1>
        <div class="lily-banner">❀ Lily Garden De Sonja ❀</div>
        <p class="subtitle" style="margin-top: 10px; margin-bottom: 0;">Pick how you are feeling right now, my beautiful girl:</p>
    </div>

    <!-- Letter Selector Row Container Grid -->
    <div class="letters-grid">
        <button class="letter-row-btn" onclick="openEnvelope('sad')"><span class="emoji">😢</span> Open when you're sad</button>
        <button class="letter-row-btn" onclick="openEnvelope('happy')"><span class="emoji">☀</span> Open when you're happy</button>
        <button class="letter-row-btn" onclick="openEnvelope('excited')"><span class="emoji">🎉</span> Open when you're excited</button>
        <button class="letter-row-btn" onclick="openEnvelope('upset')"><span class="emoji">😤</span> Open when you're upset at me</button>
        <button class="letter-row-btn" onclick="openEnvelope('mad')"><span class="emoji">😡</span> Open when you're mad at someone</button>
        <button class="letter-row-btn" onclick="openEnvelope('stressed')"><span class="emoji">🤯</span> Open when you're stressed</button>
        <button class="letter-row-btn" onclick="openEnvelope('doubtful')"><span class="emoji">🧸</span> Open when you're doubtful</button>
        <button class="letter-row-btn" onclick="openEnvelope('motivation')"><span class="emoji">🔋</span> Open when you lack motivation</button>
        <button class="letter-row-btn" onclick="openEnvelope('exam')"><span class="emoji">📚</span> Open for an exam / huge event</button>
        <button class="letter-row-btn" onclick="openEnvelope('random')"><span class="emoji">🎲</span> Open randomly</button>
    </div>

    <!-- Dynamic Unfolding Envelope Space -->
    <div class="envelope-wrapper" id="envelope-wrapper">
        <div class="envelope" id="main-envelope">
            <div class="envelope-flap"></div>
            
            <!-- Sliding Stationery Card -->
            <div class="letter-paper">
                <div class="letter-paper-header">
                    <div class="miffy-container" style="transform: scale(0.8); margin-bottom: 0;">
                        <div class="miffy-vector">
                            <div class="miffy-eyes"></div>
                            <div class="miffy-mouth"></div>
                        </div>
                    </div>
                    <h2 id="letter-title">Letter Title</h2>
                </div>
                <div id="letter-body">Letter body content goes here...</div>
            </div>
        </div>
    </div>

    <!-- Requested Sign-off Concluding Anchor -->
    <div class="footer-sig">
        With all love, yaya;) <span class="cafe-heart">♥</span>
    </div>
</div>

<script>
// Live Whimsical Floating Background Elements Generator
const componentsList = ['🌸', '☕', '🥐', '✨', '🤍', '🍰', '❀'];
const bgContainer = document.getElementById('bg-items');

for (let i = 0; i < 24; i++) {
    const item = document.createElement('div');
    item.className = 'floating-item';
    item.innerText = componentsList[Math.floor(Math.random() * componentsList.length)];
    item.style.left = Math.random() * 100 + 'vw';
    item.style.animationDelay = Math.random() * 6 + 's';
    item.style.fontSize = (Math.random() * 15 + 18) + 'px';
    bgContainer.appendChild(item);
}

// Secure token match
const secretCode = "032509040820";

// Verified 100% English Emotional Letter Database Matrix
const lettersContent = {
sad: {
title: "When You're Feeling Sad",
body: "Hey my beautiful lady, I'm so sorry you're feeling down right now. Remember how you almost drowned at the beach, and I told you to stand up, MIND YOU still afloat, yet scared the pooh out of me. (Hoped you laughed and didn't make a face. Lol.)\n\nSeriously, just call me and we can add some joy to that blue helper from inside out. :) & Take a deep breath. Yaya is always right here with you. 💕"
},
happy: {
title: "When You're Happy",
body: "Your happiness is literally my favorite thing in the entire world! Seeing you smile or hearing you laugh brightens up my whole life. Seeing you happy is amazing and heartwarming to me. Just you in general Sonja. So, whatever is making you happy to open this, I want you to know your joy brings me additional joy. Keep shining and keep completing your goals!"
},
excited: {
title: "When You're Excited",
body: "Whatever just happened, I know you worked hard for it and 101% deserve it!! Tell me everything! I love seeing your beautiful eyes light up when you're excited about something. Big or small. You deserve all the exciting, amazing things the world has to offer!"
},
upset: {
title: "When You're Upset At Me",
body: "I probably overreacted, but maybe I am just as dramatic as you are, but... I will always communicate with you on everything. My frustration brings me a lot of overwhelming emotions and I tend to get overly emotional. Knowing this makes me want to become more considerate about what I say and how I react. I am only improving every day.\n\nNow text me, after we have had our little minute apart to talk and fix our conflicted feelings."
},
mad: {
title: "When You're Mad At Someone",
body: "First off, you're 100% right, and they are just 100% incomprehensible. Do not let others frustrate you or have control over how you react. That was always their goal to make you react. Do not let them accomplish that, and don't let them rent space in your head. Take a deep breath, and remember that you are a total badass.\n\nAlso, you can always vent to me, but if I cannot respond in time, here's this letter to read for quicker reassurance."
},
stressed: {
title: "When You're Stressed or Overwhelmed",
body: "Stop whatever you are doing for just a second. Drop your shoulders, unclench your jaw, and breathe. You are trying your absolute best and that is more than enough. We can take things one tiny step at a time together. Call me if needed, I will do it with you."
}, 
doubtful: {
title: "When You're Feeling Doubtful",
body: "I wish you could see yourself through my eyes for just one minute. If you did, you would never doubt yourself in any aspect. You are stunning, whimsical, bright, gorgeous, doing amazing in life, a pleasure, caring, kind, and just every beauty in this life on earth.\n\nAs of right now, talk to yourself KINDLY RIGHT NOW! OR call me, and I will reassure you. :)"
},
motivation: {
title: "When You're Lacking Motivation",
body: "Getting started is always the hardest block to place. Just focus on doing five minutes of whatever task is ahead of you. If you need a break, let's take a cozy rest together. I believe in your work ethic and your dreams!"
},
exam: {
title: "When You Have An Exam / Big Event",
body: "You have studied so hard and prepared beautifully for this! Don't let the nerves take over. Walk in there with your head held high. No matter what the outcome is, I am already so proud of you and your beautiful mind."
},
random: {
title: "Open Randomly!",
body: "Surprise! Hey, gorgeous! I like you a lot, and I do not want to take things slow, however I want to increase our knowledge of one another. I am so excited to learn who you are and who we will become. You are amazing, you take one thing and make it so beautiful in every way there is to do so.\n\nI too wish to become the person you imagine to let be with you one day. Till then let's continue to learn each other inside and out."
}
};

// Access Authentication Guard Controller
function checkCode() {
    const userInput = document.getElementById("passcode-input").value;
    const errorMsg = document.getElementById("error-msg");
    const loginScreen = document.getElementById("login-screen");
    const mainContent = document.getElementById("main-content");
    
    if (userInput === secretCode) {
        errorMsg.style.display = "none";
        loginScreen.style.display = "none";
        mainContent.style.display = "block";
    } else {
        errorMsg.style.display = "block";
    }
}

// 3D Flap Motion Letter Mechanical Launcher
function openEnvelope(key) {
    const wrapper = document.getElementById("envelope-wrapper");
    const envelope = document.getElementById("main-envelope");
    const titleElem = document.getElementById("letter-title");
    const bodyElem = document.getElementById("letter-body");
    
    if (lettersContent[key]) {
        // Reset envelope state instantly
        envelope.classList.remove("open");
        wrapper.style.display = "block";
        
        // Wait slightly, inject clean content, then launch the 3D unfolding mechanical timeline
        setTimeout(() => {
            titleElem.innerHTML = lettersContent[key].title;
            bodyElem.innerHTML = lettersContent[key].body;
            envelope.classList.add("open");
            
            // Smoothly anchor viewpoint to active reading canvas
            setTimeout(() => {
                wrapper.scrollIntoView({ behavior: 'smooth', block: 'end' });
            }, 400);
        }, 100);
    }
}

// Permit quick-unlock using Enter Key
document.getElementById("passcode-input").addEventListener("keyup", function(event) {
    if (event.key === "Enter") {
        checkCode();
    }
});
</script>
</body>
</html>
