# hub-ready-apps

> documentation for creating civic tech apps that scale (working draft)

## Table of Contents

- [What _is_ a **Hub Ready** App?](#what-is-a-hub-ready-app)
  - [X] [Live Content](#live-content)
  - [X] [Identity](#identity)
    - [X] [Global Profile](#global-profile)*
  - [X] [Shared Theme](#shared-theme)
  - [X] [Durabe State](#durable-state)
  - [X] [Accessibility](#accessibility)
  - [X] [Indicator Aware](#indicator-aware)
  - [X] [Telemetry](#telemetry)
  - [X] [Data Citation](#data-citation)
  - [X] [Discussions](#disussions)
  - [X] [Versioning](#versioning)
  - [X] [Connected Apps](#connected-apps)*
  - [X] [App Switcher](#app-switcher)*
- [Contributing](#contributing)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [License](#license)

## What _is_ a **Hub Ready** App?

Hub-Ready Apps integrate with the Hub administrative and community user experience and provide simple workflows to inform, listen and monitor important initiatives.

Hub-Ready Apps extend the ArcGIS configurable app pattern to make it easier to share and re-use solutions that integrate directly with the Hub architecture and organization system and branding.

## Live Content

using Item config and Group Permissions (with Configurable ArcGIS Content)

Apps should be centrally managed, but then reusable through dynamic configurations that are loaded at runtime. This supports many organizations each maintaining configured versions of the app without requiring rehosting the app. This minimizes development, deployment, and operational overhead. [Read more about Configurable apps](http://doc.arcgis.com/en/arcgis-online/create-maps/create-app-templates.htm) and [configurable app specification](http://doc.arcgis.com/en/arcgis-online/create-maps/configurable-templates.htm)

A [Configurable App Template](http://doc.arcgis.com/en/arcgis-online/create-maps/create-app-templates.htm) defines its `configurationSettings`, and a Configured App stores its `values`.

- [StoryMap Template](https://www.arcgis.com/sharing/rest/content/items/94c57691bc504b80859e919bad2e0a1b/data?f=json)

A Template can also include default `values`.

Using the same StoryMap template, we have configured versions for two cities:

- [StoryMap: Los Angeles](http://www.arcgis.com/apps/StoryMapBasic/index.html?appid=ddd535ae55c843c0a569729efb0bdd0b)
 - [StoryMap Configuration](https://www.arcgis.com/sharing/rest/content/items/ddd535ae55c843c0a569729efb0bdd0b/data?f=json)
- [StoryMap: Albany](http://www.arcgis.com/apps/StoryMapBasic/index.html?appid=dd4813fd4ee64b5fa9db764ebd0dda80)
 - [StoryMap Configuration](https://www.arcgis.com/sharing/rest/content/items/dd4813fd4ee64b5fa9db764ebd0dda80/data?f=json)

If you are using Dojo, you can start with the [Map Tools Template](https://github.com/Esri/map-tools-template). This includes [code for loading configurations](https://github.com/Esri/map-tools-template/blob/master/js/template.js).

## Identity

for authentication and community

### Global Profile

for saving views and collaboration

<img width="706" alt="hub_design__hub_apps__profile" src="https://cloud.githubusercontent.com/assets/1218/24055918/4ff20156-0b18-11e7-8245-c669ebaf7e26.png">

- Log into any app
- Save current view to a group
- Zoom to saved bookmarks
- Add layers to app
- Save layers from app to my favorites

## Shared Theme

for consistent branding and design

### Global Navigation

See the [Global Navigation UX](https://esri.invisionapp.com/share/4RE6B00DY#/screens), including the sidebar controsl. Use the [Esri Global Nav](https://github.com/ArcGIS/esri-global-nav) project.

## Durable State

Consistent URI parameters across all apps: (using URL of current view)

- Location
- Zoom/Center
- Basemap
- Theme/Org
- Selected features
- Additional Layers

## Accessibility

for impaired users following WCAG & a11y

## Indicator Aware

for Initiative configuration

## Telemetry

to track usage and performance

## Data Citation

link back and attribute data provider

<img width="692" alt="hub_design__hub_apps__profile" src="https://cloud.githubusercontent.com/assets/1218/24055897/3fcae98c-0b18-11e7-86c3-9cc55f0d0b44.png">

- Link to Open Data
- Link to Item Page
- Link to Service

## Discussions

for collaboration and feedback

## Versioning

for collaborative editing and publishing

## Connected Apps

between Hub Initiatives

<img width="699" alt="hub_design__hub_apps__profile" src="https://cloud.githubusercontent.com/assets/1218/24055907/477076e8-0b18-11e7-8111-6ba66edac3be.png">

- Discover related apps for the same theme, area, initiative
- Selecting related app opens at same 'state' (e.g. at my house)

## App Switcher

between related Hub apps

## New Experiences

<img width="694" alt="hub_design__hub_apps__profile" src="https://cloud.githubusercontent.com/assets/1218/24055883/33cd2e1a-0b18-11e7-8dd5-744c97b7a105.png">

### Contributing

Esri welcomes contributions from anyone and everyone. Please see our [guidelines for contributing](https://github.com/Esri/contributing/blob/master/CONTRIBUTING.md).

### License

Copyright 2017 Esri

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

> http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

A copy of the license is available in the repository's [LICENSE](./LICENSE) file.
