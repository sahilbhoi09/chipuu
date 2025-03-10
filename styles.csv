function playMusic() {
    document.getElementById("bg-music").play();
    alert("🎵 Playing 'Ik Kudi' for you! 💖");
}

function showQuote() {
    let quotes = [
        "You're amazing! ✨",
        "Keep smiling! 😊",
        "You're stronger than you know! 💪",
        "Believe in yourself! 🌟",
        "You deserve happiness! 💖"
    ];
    let randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
    document.getElementById("quote-box").innerText = randomQuote;
}

function changeBackground() {
    let colors = [
        "linear-gradient(45deg, #ff9a9e, #fad0c4, #ffdde1, #fccb90)",
        "linear-gradient(45deg, #a18cd1, #fbc2eb, #fad0c4)",
        "linear-gradient(45deg, #ff758c, #ff7eb3, #ffb199)",
        "linear-gradient(45deg, #4facfe, #00f2fe, #43e97b)"
    ];
    let randomColor = colors[Math.floor(Math.random() * colors.length)];
    document.body.style.background = randomColor;
}

// Sparkling surprise effect
function triggerSurprise() {
    let canvas = document.getElementById("sparkleCanvas");
    let ctx = canvas.getContext("2d");

    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    let particles = [];

    function Particle(x, y) {
        this.x = x;
        this.y = y;
        this.size = Math.random() * 6 + 3;
        this.speedX = Math.random() * 3 - 1.5;
        this.speedY = Math.random() * 3 - 1.5;
        this.color = "rgba(255, 255, 255, 0.9)";

        this.update = function () {
            this.x += this.speedX;
            this.y += this.speedY;
            if (this.size > 0.2) this.size -= 0.1;
        };

        this.draw = function () {
            ctx.fillStyle = this.color;
            ctx.beginPath();
            ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
            ctx.fill();
        };
    }

    function createParticles() {
        for (let i = 0; i < 100; i++) {
            particles.push(new Particle(window.innerWidth / 2, window.innerHeight / 2));
        }
    }

    function animateParticles() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        for (let i = 0; i < particles.length; i++) {
            particles[i].update();
            particles[i].draw();
        }
        particles = particles.filter(p => p.size > 0.2);
        requestAnimationFrame(animateParticles);
    }

    createParticles();
    animateParticles();
}