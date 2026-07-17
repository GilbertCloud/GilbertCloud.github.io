---
layout: default
title: SeaIceStripes
---
## Sea Ice Stripes

I created sea ice stripes ala the [WarmingStripes](https://showyourstripes.info/) from Ed Hawkins. These stripes are available for individual months and all months on one plot. The stripes represent sea ice extent anomalies relative to the 1981-2010 climatological average. The data for the stripes comes from the [NSIDC reconstruction of Arctic sea ice extent (1850-2017)](https://nsidc.org/data/g10010/versions/2) and the [NSIDC sea ice index (1978-)](https://nsidc.org/data/g02135/versions/4). Stripes include data up to June 2026.

<div markdown="1">
  
  <label for="seaicestripe">Select month(s):</label>
  <select id="seaicestripe" onchange="showImage()">
    <option value="" ></option>
    <optgroup label="Without labels">
      <option value="allstripe" data-image="/assets/img/N_1850.png">All months</option>
      <option value="janstripe" data-image="/assets/img/N_1850_January.png">January</option>
      <option value="febstripe" data-image="/assets/img/N_1850_February.png">February</option>
      <option value="marstripe" data-image="/assets/img/N_1850_March.png">March</option>
      <option value="aprstripe" data-image="/assets/img/N_1850_April.png">April</option>
      <option value="maystripe" data-image="/assets/img/N_1850_May.png">May</option>
      <option value="junstripe" data-image="/assets/img/N_1850_June.png">June</option>
      <option value="julstripe" data-image="/assets/img/N_1850_July.png">July</option>
      <option value="augstripe" data-image="/assets/img/N_1850_August.png">August</option>
      <option value="sepstripe" data-image="/assets/img/N_1850_September.png">September</option>
      <option value="octstripe" data-image="/assets/img/N_1850_October.png">October</option>
      <option value="novstripe" data-image="/assets/img/N_1850_November.png">November</option>
      <option value="decstripe" data-image="/assets/img/N_1850_December.png">December</option>
    </optgroup>
    <optgroup label="Labeled">
      <option value="allstripelabel" data-image="/assets/img/N_1850_Labeled.png">All months</option>
      <option value="janstripelabel" data-image="/assets/img/N_1850_January_Labeled.png">January</option>
      <option value="febstripelabel" data-image="/assets/img/N_1850_February_Labeled.png">February</option>
      <option value="marstripelabel" data-image="/assets/img/N_1850_March_Labeled.png">March</option>
      <option value="aprstripelabel" data-image="/assets/img/N_1850_April_Labeled.png">April</option>
      <option value="maystripelabel" data-image="/assets/img/N_1850_May_Labeled.png">May</option>
      <option value="junstripelabel" data-image="/assets/img/N_1850_June_Labeled.png">June</option>
      <option value="julstripelabel" data-image="/assets/img/N_1850_July_Labeled.png">July</option>
      <option value="augstripelabel" data-image="/assets/img/N_1850_August_Labeled.png">August</option>
      <option value="sepstripelabel" data-image="/assets/img/N_1850_September_Labeled.png">September</option>
      <option value="octstripelabel" data-image="/assets/img/N_1850_October_Labeled.png">October</option>
      <option value="novstripelabel" data-image="/assets/img/N_1850_November_Labeled.png">November</option>
      <option value="decstripelabel" data-image="/assets/img/N_1850_December_Labeled.png">December</option>
    </optgroup>
  </select>
  
  <img id="displayImage" src="" alt=""/>

  <a id="downloadImage" href="">
    <button type="button">Download</button>
  </a>
  <script>
    function showImage() {
      var dropdown = document.getElementById("seaicestripe");
      var selectedOption = dropdown.options[dropdown.selectedIndex];
      var imgSrc = selectedOption.getAttribute("data-image");
      var altTxt = selectedOption.getAttribute("value");
      document.getElementById('displayImage').src = imgSrc;
      document.getElementById('displayImage').alt = altTxt;
      document.getElementById('downloadImage').href = imgSrc;
    }
  </script>
  
</div>

### References
Fetterer, F., Knowles, K., Meier, W. N., Savoie, M., Windnagel, A. K. & Stafford, T. (2025). Sea Ice Index. (G02135, Version 4). [Data Set]. Boulder, Colorado USA. National Snow and Ice Data Center. **DOI:** [10.7265/a98x-0f50](https://doi.org/10.7265/a98x-0f50).

Walsh, J. E., Chapman, W. L., Fetterer, F. & Stewart, J. S. (2019). Gridded Monthly Sea Ice Extent and Concentration, 1850 Onward. (G10010, Version 2). [Data Set]. Boulder, Colorado USA. National Snow and Ice Data Center. **DOI:** [10.7265/jj4s-tq79](https://doi.org/10.7265/jj4s-tq79).
