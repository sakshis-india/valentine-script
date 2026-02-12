<script>
function runCode() {
    document.getElementById("result").innerHTML = `
        <p style="margin-top:20px;">Will you be my Valentine? 💖</p>
        <button id="yes" onclick="sayYes()">Yes</button>
        <button id="no" onmouseover="moveNo()">No</button>
    `;
}

function sayYes() {
    document.getElementById("result").innerHTML = `
        <p style="margin-top:20px; font-size:22px; color:#ec4899;">
            Yaaay!! You just made my day ❤️✨
        </p>
    `;
}

function moveNo() {
    const noBtn = document.getElementById("no");
    const x = Math.random() * 200 - 100;
    const y = Math.random() * 200 - 100;
    noBtn.style.position = "relative";
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}
</script>
