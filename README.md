<!DOCTYPE 
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Quote Generator</title>
<style>
    body {
        margin: 0;
        padding: 0;
        background: linear-gradient(135deg, #0a0a0a, #1f1f1f);
        color: #fff;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: "Poppins", sans-serif;
    }
    .container {
        background: #111;
        border-radius: 20px;
        box-shadow: 0 0 25px #00eaff;
        width: 400px;
        text-align: center;
        padding: 30px;
        transition: 0.3s;
    }
    h2 {
        color: #00eaff;
        margin-bottom: 20px;
    }
    p {
        font-size: 18px;
        line-height: 1.6;
        min-height: 100px;
        transition: 0.3s;
    }
    button {
        background: #00eaff;
        border: none;
        padding: 12px 20px;
        font-size: 16px;
        border-radius: 8px;
        cursor: pointer;
        color: #000;
        font-weight: bold;
        transition: 0.3s;
    }
    button:hover {
        background: #0098b0;
    }
    .fade {
        animation: fadeIn 0.5s ease-in-out;
    }
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }
</style>
</head>
<body>

<div class="container">
    <h2>💡 AI Quote Generator</h2>
    <p id="quote">Click the button to get inspired!</p>
    <button onclick="generateQuote()">New Quote</button>
</div>

<script>
const quotes = [
    "The best way to predict the future is to create it. — Peter Drucker",
    "Do what you can, with what you have, where you are. — Theodore Roosevelt",
    "Success is not final, failure is not fatal: it is the courage to continue that counts. — Winston Churchill",
    "Your time is limited, so don’t waste it living someone else’s life. — Steve Jobs",
    "Dream big. Start small. Act now. — Robin Sharma",
    "It always seems impossible until it’s done. — Nelson Mandela",
    "Great things never come from comfort zones.",
    "Believe you can and you’re halfway there. — Theodore Roosevelt",
    "Don’t watch the clock; do what it does. Keep going. — Sam Levenson",
    "Discipline is the bridge between goals and accomplishment. — Jim Rohn"
];

function generateQuote() {
    const quoteBox = document.getElementById("quote");
    const randomIndex = Math.floor(Math.random() * quotes.length);
    quoteBox.textContent = quotes[randomIndex];
    quoteBox.classList.remove("fade");
    void quoteBox.offsetWidth; // reset animation
    quoteBox.classList.add("fade");
}
</script>

</body>
</html>
