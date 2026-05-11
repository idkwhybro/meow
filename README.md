<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>hey you</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Inter", sans-serif;
    }

    body {
      height: 100vh;
      overflow: hidden;
      background:
        radial-gradient(circle at top, #23233a, #0a0a0f 70%);
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
    }

    .card {
      width: 390px;
      padding: 42px;
      border-radius: 28px;
      background: rgba(255,255,255,0.05);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(255,255,255,0.08);
      text-align: center;
      box-shadow: 0 15px 50px rgba(0,0,0,0.45);
    }

    .tiny {
      color: #ff98ba;
      font-size: 13px;
      letter-spacing: 1px;
      margin-bottom: 14px;
    }

    h1 {
      font-size: 34px;
      line-height: 1.2;
      margin-bottom: 16px;
    }

    .sub {
      color: rgba(255,255,255,0.65);
      font-size: 15px;
      line-height: 1.6;
      margin-bottom: 34px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 14px;
    }

    button {
      border: none;
      padding: 14px 26px;
      border-radius: 14px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.25s ease;
      font-weight: 600;
    }

    #yesBtn {
      background:
        linear-gradient(135deg, #ff78a9, #ff4f8b);
      color: white;
      box-shadow: 0 10px 25px rgba(255, 79, 139, 0.35);
    }

    #yesBtn:hover {
      transform: translateY(-2px) scale(1.03);
    }

    #maybeBtn {
      background: rgba(255,255,255,0.08);
      color: rgba(255,255,255,0.85);
    }

    #maybeBtn:hover {
      background: rgba(255,255,255,0.13);
    }

    #success {
      display: none;
      position: fixed;
      inset: 0;
      background:
        radial-gradient(circle at top, #1a1a2b, #050507 75%);
      justify-content: center;
      align-items: center;
      flex-direction: column;
      animation: fadeIn 0.45s ease;
      text-align: center;
      padding: 20px;
      overflow-y: auto;
    }

    #success h2 {
      font-size: 52px;
      margin-bottom: 10px;
    }

    #success p {
      color: rgba(255,255,255,0.7);
      margin-bottom: 28px;
      font-size: 18px;
    }

    .footer {
      margin-top: 22px;
      font-size: 14px;
      color: rgba(255,255,255,0.45);
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
      }

      to {
        opacity: 1;
      }
    }
  </style>
</head>

<body>

  <div class="card">
    <div class="tiny">
      one important question...
    </div>

    <h1>
      Would you wanna go out with me sometime?
    </h1>

    <div class="sub">
      i was gonna ask normally<br>
      but then i remembered i enjoy doing unnecessary things
    </div>

    <div class="buttons">
      <button id="yesBtn">
        yes :)
      </button>

      <button id="maybeBtn">
        let me think
      </button>
    </div>
  </div>

  <div id="success">
    <h2>YEPIEEE 😭</h2>

    <p>
      this just made my whole day
    </p>

    <div
      class="tenor-gif-embed"
      data-postid="716006509349864265"
      data-share-method="host"
      data-aspect-ratio="0.843373"
      data-width="100%"
      style="max-width:320px;">
    </div>

    <script
      type="text/javascript"
      async
      src="https://tenor.com/embed.js">
    </script>

    <div class="footer">
      happiness levels are now critically high
    </div>
  </div>

  <script>
    const yesBtn =
      document.getElementById("yesBtn");

    const maybeBtn =
      document.getElementById("maybeBtn");

    const success =
      document.getElementById("success");

    yesBtn.addEventListener("click", () => {
      success.style.display = "flex";
    });

    maybeBtn.addEventListener("click", () => {
      const texts = [
        "interesting response",
        "hmmm 🤨",
        "the yes button looks friendlier",
        "i believe in u",
        "take ur time 😭"
      ];

      maybeBtn.innerText =
        texts[Math.floor(Math.random() * texts.length)];
    });
  </script>

</body>
</html>
