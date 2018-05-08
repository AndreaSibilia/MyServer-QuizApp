# QuizApp and WebApp Technical Documentation

The document is an overview of the technical requirements needed to run both the location based applications QuizApp and WebApp.
This document is structured thorugh the following points:
- System requirements;
- Tests performed;
- Template and API;
- QuizApp: the app structure;
- WebApp: the app struture.

## System requirements

QuizApp is a mobile application deployed thorugh Phonegap and available [here]( https://build.phonegap.com/apps/3148274/share ). The app is developed for Android OS, while 
iOS and Windows OS are not supported. The phonegap documentation explains that the oldest Android version supported is the 5.1.0, however no test 
was carried out on that OS version, so further studies are required to verify that.

WebApp is a browser-based applocation. It is created as a Phonegap app, but does not require to be downloaded and istalled on a mobile device. 
This App simply require a browser to by run; it works on MS Internet Explorer, MS Edge, Google Chrome, Mozilla Firefox, Safari.

## Tests performed

QuizApp has been tested on two different Android devices: an Huawei P9 lite and a Samsung Galaxi J3. Both of them run Android 7.0.0. Further test should be
performed in order to verify if the app is actually compatible with previous version of Android, like specified in the [Phonegap documentation]( https://build.phonegap.com/current-support ).
Another test was carriedout on a Nokia Lumia 735 equipped with Windows 8, however the smartphone was not able to complete the installation 
process. Therefore, the defaul app is not supported by Windows devices and require a further work to be compatible.

WebApp has been tested succesfully on five different browsers: Microsoft Edge version 41.16299.371.0, Microsoft Internet Explorer version 11.371.16299.0, 
Google Chrome Version 66.0.3359.139, Mozilla Firefox version 59.0.3 and Safari

## Template and API

Both the app are developed by using the [Material Design Dashboard template]( https://getmdl.io/templates/index.html ). 
For the map, the Leaflet API is used, version 1.3.0.

## QuizApp: the app structure

bla bla bla

## WebApp: the app struture