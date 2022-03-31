---
layout: page
permalink: /publications/
title: Publications
description: See my <a href="https://scholar.google.com/citations?user=q4wBpWAAAAAJ">Google Scholar profile</a> for more information.<br>Click <a href="#books">here for books, patents and theses that I (co-)authored</a>.
years: [2022,2021,2020,2019,2018,2016,2015,2014,2013,2012,2011,2009]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>


___
## Books
<a id="books"></a>

<table>
  <tr>
    <td style="padding:10px 40px 10px 40px">
      <img width="100px" class="z-depth-1 rounded" src="/assets/img/reconfig_book_cover.jpg" alt="Reconfigurable Logic Book">
    </td>
    <td style="padding:0px 00px 0px 20px">
      Mohamed S. Abdelfattah and Vaughn Betz, "Embedded Networks-on-Chip for FPGAs", Chapter 6 in <a href="https://www.routledge.com/Reconfigurable-Logic-Architecture-Tools-and-Applications/Gaillardon/p/book/9781482262186">Reconfigurable Logic: Architecture Tools and Applications</a>, P. Gaillardon, Taylor and Francis, 2015, pp. 149 - 184.
    </td>
  </tr>
</table>
<br>

___
### Theses  
- PhD Thesis: [Embedded Networks on Chip for Field-Programmable Gate Arrays](/assets/pdf/phd_thesis.pdf). 2016.
- MSc Thesis: [Evaluation of advanced techniques for structural FPGA self-test](/assets/pdf/msc_thesis.pdf). 2011.
- BSc Thesis: [RF Transmitters for RFID Tags in a New Technology with Ultra Thin Silicon](/assets/pdf/bsc_thesis.pdf). 2009.

___
### Patents
1. Method and Apparatus for Video Super Resolution. *2020. Application Number: UKX*
1. Method and Apparatus for Neural Architecture Search. *2020. Application Number: UK2015231.0*
1. Method and Apparatus for Analysing Neural Network Performance. *2020. Application Number: UK20199106.4*
1. Method for Designing Accelerator Hardware. *2019. Application Number: UK1913353.7*
1. Field Programmable Gate-Array with Embedded Network-on-Chip Hardware and Design Flow. *2015. Application Number: US14060253*