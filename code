<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Caesar Cipher Encryption & Decryption</title>

<style>
    body {
        font-family: Arial, sans-serif;
        background: #f4f6f9;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }

    .container {
        background: white;
        padding: 25px;
        border-radius: 10px;
        width: 400px;
        box-shadow: 0px 0px 10px #0002;
    }

    h2 {
        text-align: center;
        color: #333;
    }

    label {
        font-weight: bold;
    }

    textarea, input {
        width: 100%;
        padding: 10px;
        margin-top: 5px;
        margin-bottom: 15px;
        border: 1px solid #ccc;
        border-radius: 5px;
    }

    button {
        width: 48%;
        padding: 10px;
        font-size: 16px;
        border: none;
        cursor: pointer;
        border-radius: 5px;
        color: white;
    }

    .encrypt {
        background: #007bff;
    }

    .decrypt {
        background: #28a745;
    }

    .output {
        font-weight: bold;
        color: #444;
        margin-top: 10px;
    }

</style>
</head>
<body>

<div class="container">
    <h2>Caesar Cipher Tool</h2>
    
    <label>Enter Text:</label>
    <textarea id="text" rows="4"></textarea>

    <label>Shift Value:</label>
    <input type="number" id="shift" value="3">

    <div style="display: flex; justify-content: space-between;">
        <button class="encrypt" onclick="encryptText()">Encrypt</button>
        <button class="decrypt" onclick="decryptText()">Decrypt</button>
    </div>

    <div class="output">
        <p id="result">Output will appear here...</p>
    </div>
</div>

<script>
function caesarCipher(text, shift) {
    let result = "";

    for (let i = 0; i < text.length; i++) {
        let char = text[i];

        if (char.match(/[a-zA-Z]/)) {
            let code = text.charCodeAt(i);

            if (char >= 'A' && char <= 'Z') {
                char = String.fromCharCode(((code - 65 + shift) % 26 + 26) % 26 + 65);
            }
            else if (char >= 'a' && char <= 'z') {
                char = String.fromCharCode(((code - 97 + shift) % 26 + 26) % 26 + 97);
            }
        }

        result += char;
    }

    return result;
}

function encryptText() {
    let text = document.getElementById("text").value;
    let shift = parseInt(document.getElementById("shift").value);
    document.getElementById("result").innerText = "Encrypted: " + caesarCipher(text, shift);
}

function decryptText() {
    let text = document.getElementById("text").value;
    let shift = parseInt(document.getElementById("shift").value);
    document.getElementById("result").innerText = "Decrypted: " + caesarCipher(text, -shift);
}
</script>

</body>
</html>
