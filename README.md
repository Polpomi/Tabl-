<!DOCTYPE html>
<html lang="hu">
<head>
<meta charset="UTF-8">
<title>Keresés</title>

<style>
  body {
    font-family: Arial;
    text-align: center;
    background: white;
  }

  h1 {
    font-size: 40px;
    margin-top: 50px;
  }

  .search {
    margin: 20px;
  }

  .search input {
    width: 300px;
    padding: 10px;
    font-size: 16px;
  }

  .buttons {
    margin: 20px;
  }

  .buttons button {
    padding: 10px 20px;
    margin: 5px;
    border: none;
    background: #f1f1f1;
    cursor: pointer;
    border-radius: 5px;
  }

  .buttons button:hover {
    background: #ddd;
  }

  .gallery {
    display: none;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    margin-top: 20px;
  }

  .gallery img {
    width: 200px;
    border-radius: 10px;
  }

</style>
</head>

<body>

<h1>Googol</h1>

<div class="search">
  <input type="text" value="8.A osztály">
</div>

<div class="buttons">
  <button onclick="showGallery('a8')">8.A</button>
  <button onclick="showGallery('kirandulas')">Osztálykirándulás</button>
  <button onclick="showGallery('lesenacht')">Lesenacht</button>
</div>

<!-- 8.A -->
<div id="a8" class="gallery">
  <img src="kepek/a1.jpg">
  <img src="kepek/a2.jpg">
</div>

<!-- Kirándulás -->
<div id="kirandulas" class="gallery">
  <img src="kepek/k1.jpg">
  <img src="kepek/k2.jpg">
</div>

<!-- Lesenacht -->
<div id="lesenacht" class="gallery">
  <img src="kepek/l1.jpg">
  <img src="kepek/l2.jpg">
</div>

<script>
function showGallery(id) {
  let galleries = document.querySelectorAll('.gallery');
  galleries.forEach(g => g.style.display = 'none');

  document.getElementById(id).style.display = 'flex';
}
</script>

</body>
</html>
