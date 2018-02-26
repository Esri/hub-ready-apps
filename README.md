# hub-ready-apps

> documentation for creating civic tech apps that scale (working draft)

## Table of Contents

- [What _is_ a **Hub**?](#what-is-a-hub)
- [What _is_ a **Hub Ready App**?](#what-is-a-hub-ready-app)
- Required
  - [X] [Configurable](#configurable)
  - [X] [Indicator Aware](#indicator-aware)
  - [X] [ArcGIS Identity](#arcgis-identity)
  - [X] [Shared Theme](#shared-theme)
  - [X] [Accessible](#accessible)
  - [X] [Mobile Responsive](#mobile-responsive)

- Best Practices
  - [ ] [Localized (i18n)](#localized)
  - [ ] [Durable State](#durable-state)
  - [ ] [Data Citation](#data-citation)
  - [ ] [Telemetry](#telemetry)

- Optional
  - [ ] [Open License](#license)

- [Tools](#tools)

## What _is_ a **Hub**?

[ArcGIS Hub](http://hub.arcgis.com/) provides a two-way engagement platform to connect government and citizens.

[![video introducing hub](https://www.gislounge.com/wp-content/uploads/2017/06/arcgis-hub.png)](https://esri.app.box.com/s/edd8di8sy5r8wxyrcnl2v4mh3n5bwjpj)

> An interactive platform to organize people, processes, and technology. ArcGIS Hub comes with built-in event creation and allows you to gather feedback from inside and outside your organization to find or create new solutions to existing problems.

## What _is_ a **Hub Ready** App?

Hub-Ready Apps integrate with the Hub administrative and community user experience and provide simple workflows to inform, listen and monitor important initiatives.

Hub-Ready Apps extend the ArcGIS configurable app pattern to share and re-use solutions that integrate directly with the Hub architecture and organization datasets and branding.

**Note: Your own app doesn't need to implement _each and every_ pattern described in our checklist to be considered *Hub Ready*.**

## Configurable

<!--
~~static data~~
1. hardcoded web service
2. configurable app
3. with or w/o webmap
4. indicator aware app 🙏
-->

using Item config and Group Permissions (with Configurable ArcGIS Content)

Apps should be centrally managed, but then reusable through dynamic configurations that are loaded at runtime. This supports many organizations each maintaining [configured](http://doc.arcgis.com/en/arcgis-online/create-maps/create-app-templates.htm) versions of the app using a single deployment. This minimizes development, deployment, and operational overhead. Read more about the [configurable app specification](http://doc.arcgis.com/en/arcgis-online/create-maps/configurable-templates.htm)

A [Configurable App Template](http://doc.arcgis.com/en/arcgis-online/create-maps/create-app-templates.htm) defines its `configurationSettings`, and a Configured App stores its `values`.

- [StoryMap Template](https://www.arcgis.com/sharing/rest/content/items/94c57691bc504b80859e919bad2e0a1b/data?f=json)

A Template can also include default `values`.

Using the same StoryMap template, we have configured versions for two cities:

- [StoryMap: Los Angeles](http://www.arcgis.com/apps/StoryMapBasic/index.html?appid=ddd535ae55c843c0a569729efb0bdd0b)
 - [StoryMap Configuration](https://www.arcgis.com/sharing/rest/content/items/ddd535ae55c843c0a569729efb0bdd0b/data?f=json)
- [StoryMap: Albany](http://www.arcgis.com/apps/StoryMapBasic/index.html?appid=dd4813fd4ee64b5fa9db764ebd0dda80)
 - [StoryMap Configuration](https://www.arcgis.com/sharing/rest/content/items/dd4813fd4ee64b5fa9db764ebd0dda80/data?f=json)

Our [Configurable App Examples](https://github.com/Esri/configurable-app-examples-4x-js) leverage a helper called [`ApplicationBase`](https://github.com/Esri/application-base-js) to handle configuration JSON.

## ArcGIS Identity

ArcGIS Hub includes ArcGIS Identity, a web-based user authentication and personal content management system. Apps may require authentication (sign in) and authorization (permission) to access sensitive data or services such as spatial analysis. Additionally, users may want to save information that can be reused or shared. 

ArcGIS Identity allows a person to create an account or sign in with social media credentials (e.g. Google and Facebook), an email address, or with enterprise credentials provided through services such as LDAP or Active Directory. Once an account is created, it can be used in any web app, mobile app, website, or other service that requires authentication. This makes it simple for users to maintain one account that can be reused across multiple experiences.

You can learn more about the [benefits of ArcGIS Identity](http://www.esri.com/products/arcgis-capabilities/) or start [implementing ArcGIS Identity](https://developers.arcgis.com/documentation/core-concepts/security-and-authentication/) in your application.

## Shared Theme

Hub Ready Apps should have a consistent theme, or branding, that gives awareness and confidence to users about the source of the app. This theme is typically the branding of the organization such as the government or agency, but can also be the theme for a specific program, interest group or community.

![shared theme UI](images/shared_theme.png)


* [Introducing Shared Themes](https://blogs.esri.com/esri/arcgis/2017/02/27/introducing-a-new-app-styling-capability-in-arcgis-online/)
* [Using Shared Themes in StoryMaps](https://blogs.esri.com/esri/arcgis/2017/03/03/shared-theme-in-story-maps/)

### Organization Theme

ArcGIS Hub includes a configurable theme for organizations to set their logo, colors, fonts and other brand styling. This theme is then available via the API for automatic use in any app that is configured for the organization. The result is centralized management of the brand theme that is consistent across all apps.

Get `https://www.arcgis.com/sharing/rest/portals/{org.id}?f=json` or `https://{orgkey}.maps.arcgis.com/sharing/rest/portals/self?f=json`

```json
{
  "portalProperties": {
    "sharedTheme": {
      "header": {
        "background": "#002b49",
        "text": "#ffffff"
      },
      "body": {
        "text": "#1a1a1a",
        "background": "#ebebeb",
        "link": "#005ce6"
      },
      "button": {
        "text": "#002673",
        "background": "#ffffff"
      },
      "logo": {
        "small": "https://cityx.maps.arcgis.com/sharing/rest/content/items/5c9e486b701e4222bf5386da64908ae1/data",
        "link": "https://cityx.maps.arcgis.com/sharing/rest/content/items/5c9e486b701e4222bf5386da64908ae1/data"
      }
    }
  }
}
```


### Site & Initiative Themes

Each Hub site can also have its own theme, which allows for apps to be branded for individual departments or initiatives. 


`https://www.arcgis.com/sharing/rest/content/items/{item.id}/data?f=json`

```json
{
  "values": {
    "theme": {
      "header": {
        "background": "#012c3b",
        "text": "#ffffff"
      },
      "body": {
        "background": "#fafafa",
        "text": "#586370",
        "link": "#136fbf"
      },
      "button": {
        "background": "#136fbf",
        "text": "#ffffff"
      },
      "logo": {
        "small": "http://octo.dc.gov/sites/default/files/dc/sites/octo/multimedia_content/images/OpenData-HeaderLogo-WhiteText-2.png"
      },
      "fonts": {
        "base": {
          "url": "",
          "family": "Avenir Next"
        },
        "heading": {
          "url": "",
          "family": "Avenir Next"
        }
      }
    }
  }
}
```

## Durable State

When using an Hub Ready App, it's important that the user can easily share the current URL to others or refresh their browser and the app will reload with the current view the user sees. This also applies to mobile apps that can be opened with an app URL. Additionally, it's important to keep the URL to application consistent over time so that users or sites that link to the app continue to work, even with new versions of the app.

This is commonly referred to as Durable State - meaning that the current app state is maintained in the URL. 

Besides gracefully handling browser refreshing, the a URL can be created the directs new visitors to a specific feature, geographic location, page location, or other state that shows a particular view. 


Here are the current list of URL parameters which should be supported:

- _Location_: `?find=<location string>`
  - example: `?find=380 new york street, redlands, ca`
- _Zoom/Center_: `?center=<longitude>,<latitude>&level=<zoom>`
- _Extent_: `?extent=<longitude_west>,<latitude_south>,<longitude_east>,<latitude_north>`
  - example: `?extent=-117.20,34.055,-117.19,34.06`
- _Configuration_: `?id=<item.id>`
  - example: `?id=da80a448ac9246192da0811bddc18c94`
- Theme/Org
- _Selected features_: `?query=<layer name>,<field name>,<field value>` or `?query=<layer name>, <where clause>`
  - example: `?query=Census_8491,STATE_NAME='California'`
- Additional Layers
- Language locale: `?locale=<two-letter country code>`
  - example: `?locale=es`

[Learn more about URL parameters](https://doc.arcgis.com/en/web-appbuilder/manage-apps/app-url-parameters.htm)

## Accessibile

Hub Ready Apps are inclusive for all users. This includes people who use supportive devices such as screen-readers or keyboard navigation. Standards such as [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/intro/wcag) and [Section 508](https://www.section508.gov/) prescribe patterns and practices for ensuring proper accessibility.

Hub Ready Apps should support accessibility guidelines.

## Indicator Aware

for Initiative configuration

## Telemetry

> 'That which is measured, improves' - [Thomas S Monson](https://english.stackexchange.com/questions/14952/that-which-is-measured-improves)

A Hub Ready App should provide the option to measure usage and efficacy for organization in order to measure their impact and improve content usability. By logging information on visits, usage, performance, errors and the successful completion of pre-defined user workflows the organization managers can report on usage and continually improve the app configuration to meet user needs.

In the future, ArcGIS Hub will include libraries for integrating app telemetry with the Hub for comparison of app engagement with real-world engagement and outcomes.

## Mobile Responsive

> "The share of Americans that own smartphones is now 77%, up from just 35% ... in 2011." [- Pew Research](http://www.pewinternet.org/fact-sheet/mobile/)

> "Today just over one-in-ten American adults are “smartphone-only” internet users – meaning they own a smartphone, but do not have traditional home broadband service." [- Pew Research](http://www.pewinternet.org/fact-sheet/mobile/)

Building a mobile friendly application should be considered a requirement if your goal is to reach anyone with internet access.

## Localized

Besides making it more likely that your application could be deployed in more than one location, providing translations for languages other than english broadens the reach of your application _within_ a city by including a more diverse collection of stakeholders.

Open source frameworks like Dojo and JQuery have provided tooling to help create [i18n](https://en.wikipedia.org/wiki/Internationalization_and_localization) applications for many years. These days there are compact framework agnostic options like [Polyglot](https://github.com/airbnb/polyglot.js) as well.

## Data Citation

Its absolutely crucial that you attribute the providers of the data your application consumes.

<img width="692" alt="hub_design__hub_apps__profile" src="https://cloud.githubusercontent.com/assets/1218/24055897/3fcae98c-0b18-11e7-86c3-9cc55f0d0b44.png">

- Link to Open Data
- Link to Item Page
- Link to Service

## New Experiences

<img width="694" alt="hub_design__hub_apps__profile" src="https://cloud.githubusercontent.com/assets/1218/24055883/33cd2e1a-0b18-11e7-8dd5-744c97b7a105.png">

## Tools

<!-- to do:
discuss continuum of small building blocks to death star lego sets
-->

https://github.com/Esri/arcgis-rest-js
https://github.com/Esri/arcgis-ember-portal-services
https://github.com/Esri/configurable-app-examples-4x-js

## License

For Open Data, a license is a [**must**](https://creativecommons.org/licenses/). For Hub Ready Apps, an Open License is optional.

For the projects Esri shares on GitHub, we usually choose [`Apache-2.0`](https://spdx.org/licenses/Apache-2.0.html).

Copyright 2018 Esri

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
