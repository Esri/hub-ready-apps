<!-- .slide: data-background="img/bg-7.png" -->

<h2><img src="img/icons8-change_theme.png" class="inline transparent"> Shared Themes</h2>

---

<!-- .slide: data-background="img/bg-7.png" -->

### Communicates source of the app

<a href="https://sharedtheme.maps.arcgis.com/apps/MapAndAppGallery/index.html?appid=c4c6831ded304dd4a2e58d93528e1507"><img src="img/Basic-Viewer-Forest-Service-Theme.png" class="transparent" height="400"></a>

Notes:
Gives confidence to users

---

<!-- .slide: data-background="img/bg-7.png" -->

### Organization Shared Themes

<a href="https://doc.arcgis.com/en/arcgis-online/administer/configure-general.htm"><img src="img/SharedThemeSettingBlog.png" class="transparent" height="400" /></a>

---

<!-- .slide: data-background="img/bg-7.png" -->

### Fetch from [portals self](http://tomwayson.maps.arcgis.com/sharing/rest/portals/self?culture=en&f=json) API


Only available to logged in users

<img src="img/icons8-lock_2.png" class="transparent">

Note:
may be available in configuration panel
if not need to create a self-configurable app

---

<!-- .slide: data-background="img/bg-7.png" -->

### Hub Site Shared Themes

<a href="https://doc.arcgis.com/en/hub/sites/design-the-layout-of-your-hub-site.htm"><img src="img/hub-site-admin.png" class="transparent" height="500" /></a>

Note:
created at runtime

---

<!-- .slide: data-background="img/bg-7.png" -->

### Fetch from [Hub site item ](https://www.arcgis.com/sharing/rest/content/items/ce0da32bc96047c882585609c63d537d/resources/theme.json)

- A resource on the site item
- Access based on site permission (public, group, private)

<img src="img/icons8-lock_2.png" class="transparent">
<img src="img/icons8-unlock_2.png" class="transparent">

Example: [MyStreet](https://github.com/Esri/MyStreet)

Note:

---

<!-- .slide: data-background="img/bg-7.png" -->

<h2><img src="img/icons8-sporty_wheelchair_user.png" class="inline transparent"> Accessible Apps</h2>

---

<!-- .slide: data-background="img/bg-7.png" -->

[Accessible Web Mapping Apps: ARIA, WCAG and 508 Compliance](https://devsummit2018.schedule.esri.com/schedule/1610726097)

Kelly Hutchins, Tao Zhang

Friday, March 09
8:30 am - 9:30 am
Smoketree A-E

Note:
- I'm far from an expert
- JavaScript API team takes this very seriously

---

<!-- .slide: data-background="img/bg-7.png" -->

### Hub's [short list](https://github.com/Esri/hub-ready-apps/blob/master/ACCESSIBLE.md)
<ul>
  <li class="fragment">text alternatives (`alt="logo"`)
  <li class="fragment">semantics and relationships (`<nav>`, `<label for="username">`)
  <li class="fragment">keyboard (`tabindex="2"`, visible focus)
  <li class="fragment">color ([minimum contrast](https://blogs.esri.com/esri/arcgis/2016/09/01/accessibility-guidelines-color-contrast-testing-for-configurable-apps/))
  <li class="fragment">language (`lang="fr"`)
</ul>

Note:
- bypass blocks `<a href="#maincontent">Skip to main content</a>`
- `document.addEventListener('keydown', keydownListener)`

---

<!-- .slide: data-background="img/bg-7.png" -->

## Engaging citizens where they are

<img src="img/icons8-subway.png" class="transparent">
<img src="img/icons8-multiple_smartphones.png" class="transparent">
<img src="img/icons8-regular_biking.png" class="transparent">

Note:
- hopefully not looking at phone while riding bike on train tracks


---

<!-- .slide: data-background="img/bg-7.png" -->

### Responsive required

<img src="img/icons8-multiple_devices.png" class="transparent">

Note:
- not new
- not hard

---

<!-- .slide: data-background="img/bg-7.png" -->

<img src="img/esri.png" class="transparent" height="300">

Built into the [ArcGIS API for JavaScript](https://developers.arcgis.com/javascript/latest/sample-code/index.html?search=responsive)

---

<!-- .slide: data-background="img/bg-7.png" -->

### Responsive UI frameworks

- [Bootstrap](https://getbootstrap.com/)
- [Foundation](https://foundation.zurb.com/)
- [Skeleton](http://getskeleton.com/)...

---

<!-- .slide: data-background="img/bg-7.png" -->

### CSS solutions for modern browsers

- [flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- [grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)

Note:
- CSS grid: https://hackernoon.com/how-css-grid-beats-bootstrap-85d5881cf163

---

<!-- .slide: data-background="img/bg-7.png" -->

### Beyond responsive

<div style="width: 100px; margin: 40px auto;">
  <div class="spinner">
    <div class="rect1"></div>
    <div class="rect2"></div>
    <div class="rect3"></div>
    <div class="rect4"></div>
  </div>
</div>

<p class="fragment">We need to _respond_<p>

Note:
- should not have to "send link to desktop"

---

<!-- .slide: data-background="img/bg-7.png" -->

### Maps are heavy

<img src="img/globe-seesaw.png" class="transparent" />

<p class="fragment">We're working on it</p>

---

<!-- .slide: data-background="img/bg-7.png" -->

### No map? No problem

<img src="img/search-app.svg" class="transparent" height="240" />
<img src="img/search-phone.svg" class="transparent" height="240" />

Use something like [arcgis-rest-js](https://esri.github.io/arcgis-rest-js/)

---

<!-- .slide: data-background="img/bg-7.png" -->

### Map only on _some_ routes

<img src="img/search-app.svg" class="transparent" height="240" />
<img src="img/icons8-right.png" class="transparent" />
<img src="img/details-page.svg" class="transparent" height="240" />

Use something like [esri-loader](https://github.com/Esri/esri-loader)

Note:
- Also helps for SEO
- may _need_ esri-loader if using a CLI

---

<!-- .slide: data-background="img/bg-7.png" -->

### _Especially_ for mobile first apps

<img src="img/search-phone.svg" class="transparent" height="240" />
<img src="img/icons8-right.png" class="transparent" />
<img src="img/map-phone.svg" class="transparent" height="240" />

Use something like [esri-loader](https://github.com/Esri/esri-loader)

---

<!-- .slide: data-background="img/bg-7.png" -->

### All about the map / 3D scene?

<img src="img/all-about-the-map.svg" class="transparent" height="240" />

Use something like [maps-app-javascript](https://github.com/Esri/maps-app-javascript)

---

<!-- .slide: data-background="img/bg-7.png" -->

### [Progressive Web Apps](https://developers.google.com/web/progressive-web-apps/)

<ul>
  <li class="fragment">Reliable (_some_ offline)
  <li class="fragment">Fast (service worker to cache content)
  <li class="fragment">Engaging (install on homescreen)
</ul>

Note:

Beyond minimizing and deferring bits you download

Example: [Hub Events](https://github.com/tomwayson/hub-events)