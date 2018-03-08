<!-- .slide: data-background="img/bg-7.png" -->

### More recommended patterns

---

<!-- .slide: data-background="img/bg-7.png" -->

### Localized (i18n)

---

<!-- .slide: data-background="img/bg-7.png" -->

```
//.yaml
geoservice:
  plan: "The source license grants permission..."

copylabel.append('span')
  .html(t('geoservice.plan'));
```

![localized](./localized.png)<br>
[(source)](https://github.com/mapmeld/iD/blob/98703e8c67b3d821fb27b66606b2b328955ed5dc/modules/ui/map_data.js#L562-L563)

---

<!-- .slide: data-background="img/bg-7.png" -->

### Durable state 

`http://yourapp.com/?center=-117,34&zoom=12`

---

### [Durable state](https://developers.arcgis.com/javascript/latest/api-reference/esri-core-urlUtils.html)

```js
require(["esri/core/urlUtils"], function(urlUtils) { 
    urlUtils.urlToObject("http://www.myworld.com?state_name=Ohio&city_name=Akron")
    // { 
    //   path: "http://www.myworld.com",
    //   query: {
    //     state_name: "Ohio", 
    //     city_name: "Akron"
    //   } 
    // }
});

```

---

<!-- .slide: data-background="img/bg-7.png" -->

### Data Citation

<img alt="attribution" style='width:60%;' src="https://cloud.githubusercontent.com/assets/1218/24055897/3fcae98c-0b18-11e7-86c3-9cc55f0d0b44.png">

- Link to Open Data
- Link to Item Page
- Link to Service

---

<!-- .slide: data-background="img/bg-7.png" -->

### Telemetry

> 'That which is measured, improves' - [Thomas S Monson](https://english.stackexchange.com/questions/14952/that-which-is-measured-improves)

---

<!-- .slide: data-background="../../../template/img/ds2018/bg-9.png" -->

please, _please_, **please** fill out a session survey

1. download the Esri Events App
2. select Dev Summit
3. search for "Hub ready"
4. leave feedback!

---

<!-- .slide: data-background="../../../template/img/ds2018/bg-1.png" -->

idea, question, issue, or success story?

[@geogangster](https://twitter.com/geogangster) / [@tomwayson](https://twitter.com/tomwayson)

Slides: [`http://bit.ly/2I7qOd3`](http://bit.ly/2I7qOd3)

---

<img class="transparent" src="./img/esri-science-logo-white.png">