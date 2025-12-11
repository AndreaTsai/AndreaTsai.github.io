<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<title>盲盒遊戲</title>
<style>
  body { font-family: Arial; display: flex; padding: 20px; }
  #leftPanel { width: 200px; border-right: 1px solid #ccc; padding-right: 20px; }
  #leftPanel h3 { text-align: center; }
  #collected img { width: 100%; margin-bottom: 10px; }
  #mainPanel { flex: 1; padding-left: 20px; text-align: center; }
  #preview img, #result img { max-width: 300px; margin: 10px; }
  button { padding: 10px 20px; font-size: 16px; margin-top: 10px; }
</style>
</head>
<body>

<div id="leftPanel">
  <h3>已抽到的盲盒</h3>
  <div id="collected"></div>
</div>

<div id="mainPanel">
  <h1>盲盒遊戲</h1>

  <!-- 管理者上傳區 -->
  <div id="uploadSection">
    <h2>上傳盲盒圖片 (管理者可見)</h2>
    <p>盲盒圖片 (5張):</p>
    <input type="file" id="fileInput" multiple accept="image/*"><br><br>
    <p>未開盲盒圖片:</p>
    <input type="file" id="closedInput" accept="image/*"><br><br>
    <button onclick="saveImages()">儲存圖片</button>
    <div id="preview"></div>
  </div>

  <!-- 玩家遊玩區 -->
  <div id="playSection" style="display:none;">
    <h2>開盲盒！</h2>
    <div id="boxArea">
      <img id="boxImage" src="" style="max-width:200px">
    </div>
    <br>
    <button onclick="openBox()">開盲盒</button>
    <button onclick="confirmBox()">確定</button>
  </div>
</div>

<script>
let images = [];        // 盲盒圖片
let closedImage = '';   // 未開盲盒圖片
let collected = [];     // 玩家已抽到的圖片
let currentBox = '';    // 玩家當前抽到的圖片
let isAdmin = true;     // 假設第一個人是管理者

// 預覽上傳圖片
document.getElementById('fileInput').addEventListener('change', function(e) {
  const files = e.target.files;
  const preview = document.getElementById('preview');
  preview.innerHTML = '<p>盲盒圖片預覽：</p>';
  for (let i = 0; i < files.length && i < 5; i++) {
    const img = document.createElement('img');
    img.src = URL.createObjectURL(files[i]);
    preview.appendChild(img);
  }
});
document.getElementById('closedInput').addEventListener('change', function(e){
  const file = e.target.files[0];
  const preview = document.getElementById('preview');
  const img = document.createElement('img');
  img.src = URL.createObjectURL(file);
  preview.appendChild(document.createElement('br'));
  preview.appendChild(document.createTextNode('未開盲盒預覽：'));
  preview.appendChild(document.createElement('br'));
  preview.appendChild(img);
});

// 儲存圖片 (管理者)
function saveImages() {
  const files = document.getElementById('fileInput').files;
  const closedFile = document.getElementById('closedInput').files[0];
  if (files.length < 5 || !closedFile) {
    alert("請上傳5張盲盒圖片與1張未開盲盒圖片！");
    return;
  }
  images = [];
  for (let i = 0; i < 5; i++) {
    images.push(URL.createObjectURL(files[i]));
  }
  closedImage = URL.createObjectURL(closedFile);
  alert("圖片已儲存！");
  document.getElementById('uploadSection').style.display = 'none';
  document.getElementById('playSection').style.display = 'block';
  document.getElementById('boxImage').src = closedImage;
}

// 開盲盒
function openBox() {
  if (images.length === 0) {
    alert("尚未有管理者設定圖片！");
    return;
  }
  const index = Math.floor(Math.random() * images.length);
  currentBox = images[index];       // 隨機抽取
  document.getElementById('boxImage').src = currentBox;
}

// 確定抽到的盲盒
function confirmBox() {
  if (!currentBox) {
    alert("請先點開盲盒！");
    return;
  }
  collected.push(currentBox);
  currentBox = '';
  document.getElementById('boxImage').src = closedImage;

  // 更新左邊已抽到列表
  const collectedDiv = document.getElementById('collected');
  collectedDiv.innerHTML = '';
  collected.forEach(src => {
    const img = document.createElement('img');
    img.src = src;
    collectedDiv.appendChild(img);
  });
}

// 非管理者使用時直接隱藏上傳區
if (!isAdmin) {
  document.getElementById('uploadSection').style.display = 'none';
  document.getElementById('playSection').style.display = 'block';
  document.getElementById('boxImage').src = closedImage || ''; // 如果管理者尚未設定圖片會是空白
}
</script>

</body>
</html>
