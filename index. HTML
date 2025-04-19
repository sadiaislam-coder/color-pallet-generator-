<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Color Palette Generator</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f9f9f9;
      text-align: center;
      padding: 30px;
    }

    h1 {
      color: #333;
      margin-bottom: 20px;
    }

    .palette {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 15px;
      margin-bottom: 20px;
    }

    .color-box {
      width: 120px;
      height: 120px;
      border-radius: 10px;
      position: relative;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
      cursor: pointer;
      transition: transform 0.2s;
    }

    .color-box:hover {
      transform: scale(1.05);
    }

    .color-code {
      position: absolute;
      bottom: 10px;
      left: 0;
      right: 0;
      font-weight: bold;
      color: #fff;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      background-color: #4CAF50;
      color: white;
      cursor: pointer;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
    }

    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <h1>Color Palette Generator</h1>
  <div class="palette" id="palette"></div>
  <button onclick="generatePalette()">Generate Colors</button>

  <script>
    function getRandomColor() {
      const hex = "0123456789ABCDEF";
      let color = "#";
      for (let i = 0; i < 6; i++) {
        color += hex[Math.floor(Math.random() * 16)];
      }
      return color;
    }

    function generatePalette() {
      const container = document.getElementById("palette");
      container.innerHTML = "";

      for (let i = 0; i < 6; i++) {
        const color = getRandomColor();
        const box = document.createElement("div");
        box.className = "color-box";
        box.style.backgroundColor = color;

        const label = document.createElement("div");
        label.className = "color-code";
        label.innerText = color;

        box.appendChild(label);
        container.appendChild(box);
      }
    }

    // Generate default palette on load
    window.onload = generatePalette;
  </script>

</body>
</html>
