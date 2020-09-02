---
title: "Analysis of The Characteristics of the Oldest Living Cats"
always_allow_html: true
author: "beep"
date: "01 September, 2020"
output: 
  html_document:
    keep_md: true
bibliography: references.bib  
nocite: '@*'
---



---

## Introduction

This is an analysis of an unofficial list from [Wikipedia](https://en.wikipedia.org/wiki/List_of_oldest_cats) of world's oldest cats. The reported ages range from precise to vague estimates. The minimum age requirement for cats to be added to this list was 25 years old. Despite this dataset being small and imprecise, I hope by examining it to discover possible factors contributing to these cats' longevity. 

---

## Method

To obtain this dataset, I used the `rvest` package to webscrape the table from its Wikipedia page. In the case of cats with imprecise ages, I calculated their approximate age. For instance, if a cat was listed as being 29 years old and 8 months, I inputted their age as $29 + (8 * 30 )/365 = 29.6575$ days. Then, I used the `plotly` package to create visualizations.

---

## Exploratory Analysis

<br>

<!--html_preserve--><div id="htmlwidget-dc0c684985c8a407d1bb" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-dc0c684985c8a407d1bb">{"x":{"visdat":{"280465cb7d4a":["function () ","plotlyVisDat"]},"cur_data":"280465cb7d4a","attrs":{"280465cb7d4a":{"x":{},"y":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"bar"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"title":"Ages and Names","yaxis":{"domain":[0,1],"automargin":true,"title":"Reported age"},"xaxis":{"domain":[0,1],"automargin":true,"title":"Name","type":"category","categoryorder":"array","categoryarray":["Hobo","Tammy","Banjo","Corduroy","Kataleena Lady","Wadsworth","Tiffany Two","Cola","Soot","Tattie","Missan","Squeak","Henry","Scooter","Whiskey","Tiger","Rubble","Spike","Kitty","Nutmeg","Miez Maz","Sasha","Sarah","Granpa Rexs Allen","Ma","Puss","Baby","Creme Puff"]},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["Creme Puff","Baby","Puss","Ma","Granpa Rexs Allen","Sarah","Miez Maz","Sasha","Rubble","Nutmeg","Kitty","Spike","Tiger","Whiskey","Henry","Scooter","Missan","Squeak","Cola","Soot","Tattie","Tiffany Two","Wadsworth","Banjo","Kataleena Lady","Corduroy","Tammy","Hobo"],"y":[38.0082191780822,38,36.0027397260274,34.4109589041096,34.1643835616438,33.4986301369863,33,33,31.1643835616438,32,31.9150684931507,31.1643835616438,31,30.1123287671233,30,30,29,29,28,28,28,27.1917808219178,27,27,27,27,26.0712328767123,26],"type":"bar","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->


<br><br>


<!--html_preserve--><div id="htmlwidget-935a458c10e3e38d80c1" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-935a458c10e3e38d80c1">{"x":{"visdat":{"28043b601cb0":["function () ","plotlyVisDat"]},"cur_data":"28043b601cb0","attrs":{"28043b601cb0":{"x":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"histogram"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"title":"Country of Origin","xaxis":{"domain":[0,1],"automargin":true,"title":"Country","type":"category","categoryorder":"array","categoryarray":["Australia","Canada","New Zealand","Sweden","Switzerland","United Kingdom","United States"]},"yaxis":{"domain":[0,1],"automargin":true},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["United States","United States","United Kingdom","United Kingdom","United States","New Zealand","Switzerland","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United States","United Kingdom","United Kingdom","United States","Sweden","United States","United Kingdom","Canada","Canada","United States","United Kingdom","United Kingdom","Australia","United States","United Kingdom","United States"],"type":"histogram","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

<br>
<br>

<!--html_preserve--><div id="htmlwidget-e1f8f6dd39bc608db932" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-e1f8f6dd39bc608db932">{"x":{"visdat":{"28046afd6339":["function () ","plotlyVisDat"]},"cur_data":"28046afd6339","attrs":{"28046afd6339":{"x":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"histogram"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"title":"Cat Breeds","xaxis":{"domain":[0,1],"automargin":true,"title":"Breed","type":"category","categoryorder":"array","categoryarray":["Black-and-white longhair","Black and white DSH","Black cat","Black DSH","Burmese cat","Calico cat","longhair (orange and white)","Maine Coon","Orange tabby","Siamese cat","Sphynx-Devon Rex","Tabby","Tabby DSH","Tabby mix","Tortoiseshell cat","White DSH"]},"yaxis":{"domain":[0,1],"automargin":true},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["Tabby mix","Black DSH","Tabby","Tabby DSH","Sphynx-Devon Rex","Tortoiseshell cat","Maine Coon","Tabby","Black DSH","longhair (orange and white)","Orange tabby","Black and white DSH","Tabby","Siamese cat","Calico cat","Black cat","Black cat","Calico cat","Tortoiseshell cat","Black and white DSH","Burmese cat","Tabby","Black-and-white longhair","White DSH"],"type":"histogram","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

<br>
<br>


<!--html_preserve--><div id="htmlwidget-783323033884b7c4f26b" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-783323033884b7c4f26b">{"x":{"visdat":{"28046a006036":["function () ","plotlyVisDat"]},"cur_data":"28046a006036","attrs":{"28046a006036":{"x":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"histogram"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"title":"Count of Sex","xaxis":{"domain":[0,1],"automargin":true,"title":"Sex","type":"category","categoryorder":"array","categoryarray":["female","male"]},"yaxis":{"domain":[0,1],"automargin":true},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"x":["female","male","male","female","male","female","male","female","male","male","female","male","male","male","male","male","female","female","female","male","female","female","male","male","male","female","female"],"type":"histogram","marker":{"color":"rgba(31,119,180,1)","line":{"color":"rgba(31,119,180,1)"}},"error_y":{"color":"rgba(31,119,180,1)"},"error_x":{"color":"rgba(31,119,180,1)"},"xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

---





# References
