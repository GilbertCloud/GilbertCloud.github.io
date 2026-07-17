---
layout: default
title: SeaIceStripes
---
## Sea Ice Stripes

Uses NSIDC reconstruction (1850-2017) and NSIDC sea ice index (1978-)

<div markdown="1">
  
  <label for="seaicestripe">Select month(s):</label>
  <select id="seaicestripe" onchange="showImage()">
    <option value="janstripe" data-image="/assets/img/N_1850_January_Labeled.pdf">January</option>
    <option value="febstripe" data-image="/assets/img/N_1850_February_Labeled.pdf">February</option>
  </select>
  
  <img id="displayImage" src="" alt=""/>
  <script>
    function showImage() {
      var dropdown = document.getElementById("seaicestripe");
      var selectedOption = dropdown.options[dropdown.selectedIndex];
      var imgSrc = selectedOption.getAttribute("data-image");
      var altTxt = selectedOption.getAttribute("value");
      document.getElementById('displayImage').src = imgSrc;
      document.getElementById('displayImage').alt = altTxt;
    }
  </script>
  
</div>
