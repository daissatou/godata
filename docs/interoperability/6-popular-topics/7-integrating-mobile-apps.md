---
layout: default
title: Integrating with Mobile Apps
parent: Frequently Asked Questions
grand_parent: Go.Data Interoperability
nav_order: 7
permalink: /integrating-mobile-apps/
---
# Integrating Go.Data with Mobile Data Collection Apps 
Many Go.Data implementers leverage other mobile apps for offline-supported data collection and case management. Popular mobile apps include open-source options like Kobo Toolbox,
Open Data Kit (ODK), CommCare, Ona, and SurveyCTO. While these mobile tools offer different features and implementation options, they for the most part all support 2 main integration approaches: 
## 1. Integration via REST Service/ Webhook
Many mobile data collection features provide this feature to automatically publish or "push" data collected via mobile to an external data source. Users can therefore configure a REST service/ webhook 
to automatically forward new mobile form submissions in `JSON` or `XML` format to an external app whenever new data is collected. This approach enables real-time data integration and can 
be entirely controlled in the data source-side. 

See the [reference implementation #4](https://worldhealthorganization.github.io/godata/godata--mobile-integration/) for an example implementation where a [REST Service](https://support.kobotoolbox.org/rest_services.html) was configured in Kobo Toolbox to automatically forward new submissions to the 
[OpenFn](https://docs.openfn.org/kobo-toolbox.html) integration layer where automation was configured to transform & map the Kobo data into Go.Data via the API. 

## 2. Integration via APIs 
Many of mobile data collection tools also provide a REST API for enhanced data sharing options to extract mobile data collection. Data extraction options are limited to what is supported
by each app's API (for example, see [Kobo Toolbox](https://support.kobotoolbox.org/api.html) and [ODK API docs](https://docs.getodk.org/aggregate-data-access/?highlight=json#odk-api) to compare).  

## Resources 
1. See [reference implementation #4](https://worldhealthorganization.github.io/godata/godata--mobile-integration/) for specific step-by-step guidance with a real-world mobile integration example with Kobo Toolbox.
2. For summarized instructions on REST service setup and API documentation links for popular mobile tools like Kobo Toolbox, ODK, SurveyCTO, etc., check out each app's technical documentation or see [OpenFn 'Source Apps' docs](https://docs.openfn.org/source-apps.html). 
