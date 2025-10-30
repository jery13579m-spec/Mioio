<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>響應式範例 + 圖片</title>
  <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
  <style>
    body {
      margin: 0;
      padding: 20px;
      font-family: Arial, sans-serif;
    }

    h1, p {
      text-align: center;
    }

    /* 圖片讓它不會超出容器 */
    .responsive-img {
      max-width: 100%;
      height: auto;
      display: block;
      margin: 0 auto;
    }

    /* 圖表容器 */
    #myPlot {
      width: 100%;
      max-width: 700px;
      margin: 20px auto;
    }

    /* 影片響應式容器 (16:9) */
    .video-container {
      position: relative;
      width: 100%;
      padding-bottom: 56.25%;
      height: 0;
      overflow: hidden;
      max-width: 900px;
      margin: 20px auto;
    }

    .video-container iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }
  </style>
</head>
<body>

  <h1>響應式網頁加圖片範例</h1> 
  <p>41443148
     廖炫榮
  </p>
  <p>下面是一張圖片 + 圖表 + 影片</p>
 

  <!-- 加入圖片 -->
  <img
    src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7baOHUCm_fpu068IkpAGZBKlba_xEn8t5Ww&s"
    alt="示意圖"
    class="responsive-img"
  />

  <!-- Plotly 圖表 -->
  <div id="myPlot"></div>
  <script>
    const xArray = ["pp19", "mp5", "ak74n", "沙漠之鷹", "ML槓桿步槍"];
    const yArray = [55, 49, 44, 24, 90];

    const data = [{
      x: xArray,
      y: yArray,
      type: "bar",
      orientation: "v",
      marker: { color: "rgba(0,0,255,0.6)" }
    }];

    const layout = {
      title: "暗區突圍中我常用武器使用統計圖",
      autosize: true,
      margin: { t: 40 }
    };

    Plotly.newPlot("myPlot", data, layout, { responsive: true });
  </script>

  <!-- YouTube 影片 -->
   <p>這是某遊戲的主題曲</p>
  <div class="video-container">
    <iframe
      src="https://www.youtube.com/embed/pzt6SmvGpXk?list=RDpzt6SmvGpXk"
      title="〈Sacrifice〉ft.G.E.M."
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen>
    </iframe>
  </div>
  <!-- 新增的超連結 -->
<p style="text-align: center; margin-top: 20px;">
  👉 <a href="https://newbie123-blip.github.io/homework1/index.html" target="_blank">
    點我前往一個同學的作業頁面
  </a><br><br>
  👉 <a href="https://a6706976-5455.github.io/the-internet-homework/" target="_blank">
    點我前往另一個同學的作業頁面
  </a>
</p>



</body>
</html>
