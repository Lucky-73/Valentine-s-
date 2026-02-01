# Valentine-s-
For you cutie 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine</title>

<style>
  body {
    margin: 0;
    height: 100vh;
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #fff;
    overflow: hidden;
  }

  .card {
    text-align: center;
  }

  img {
    width: 180px;
    margin-bottom: 20px;
  }

  h2 {
    color: #e06666;
    margin-bottom: 25px;
  }

  #yesBtn {
    padding: 15px 35px;
    font-size: 20px;
    background: #ff4081;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: transform 0.2s;
  }

  #noBtn {
    position: absolute;
    padding: 12px 25px;
    font-size: 16px;
    background: #ddd;
    border: none;
    border-radius: 6px;
    cursor: pointer;
  }

  .fullscreen {
    position: fixed;
    inset: 0;
    background: #ff4081;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-size: 40px;
    z-index: 999;
  }
</style>
</head>

<body>

<div class="card" id="card">
  <img src="https://i.imgur.com/4AiXzf8.png" alt="Bear">
  <h2>Will you be my Valentine?</h2>
  <button id="yesBtn">Yes</button>
</div>

<button id="noBtn">No</button>

<script>
  const yesBtn = document.getElementById("yesBtn");
  const noBtn = document.getElementById("noBtn");
  const card = document.getElementById("card");

  let scale = 1;

  noBtn.addEventListener("click", () => {
    // Increase YES size
    scale += 0.25;
    yesBtn.style.transform = `scale(${scale})`;

    // Move NO randomly
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = `${x}px`;
    noBtn.style.top = `${y}px`;
  });

  yesBtn.addEventListener("click", () => {
    document.body.innerHTML = `
      <div class="fullscreen">
        I'm just kidding 😄
      </div>
    `;
  });
</script>

</body>
</html>
