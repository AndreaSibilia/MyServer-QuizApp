# QuizApp and WebApp Technical Documentation

## Introduction

The MyServer-QuizApp folder contains the NodeJS Server that manages both the WebApp and the QuizApp. It provides the connection to the database 
in order to set up new questions through the WebApp and to download the questions set through QuizApp. It also records the user's answers.
The following document is a technical guide that provides the initial support to approach the app in order to proceed with its development and to fix it.

## Guide content

The document is an overview of the technical requirements needed to run both the location-based applications QuizApp and WebApp.
This document is structured thorugh the following points:
- System requirements;
- Tests performed;
- Template and API;
- QuizApp: the app structure;
- WebApp: the app struture;
- The server.

## System requirements

QuizApp is a mobile application deployed thorugh Phonegap and available [here]( https://build.phonegap.com/apps/3148274/share ). The app is developed for Android OS, while 
iOS and Windows OS are not supported. The phonegap documentation explains that the oldest Android version supported is the 5.1.0, however no test 
was carried out on that OS version, so further studies are required to verify this.

WebApp is a browser-based application. It is created as a Phonegap app, but does not require to be downloaded and istalled on a mobile device. 
This App simply requires a browser to run; it works on MS Internet Explorer, MS Edge, Google Chrome, Mozilla Firefox, Safari.

## Tests performed

QuizApp has been tested on two different Android devices: a Huawei P9 lite and a Samsung Galaxy J3. Both of them run Android 7.0.0. Further tests should be
performed in order to verify if the app is actually compatible with previous versions of Android, like specified in the [Phonegap documentation]( https://build.phonegap.com/current-support ).
Another test was carried out on a Nokia Lumia 735 equipped with Windows 8, however the smartphone was not able to complete the installation 
process. Therefore, the default app is not supported by Windows devices and require further work to be compatible.

WebApp has been tested succesfully on five different browsers: Microsoft Edge version 41.16299.371.0, Microsoft Internet Explorer version 11.371.16299.0, 
Google Chrome Version 66.0.3359.139, Mozilla Firefox version 59.0.3 and Safari version 11.1 (12605.1.33.1.4).

## Template and API

Both the app are developed by using the [Material Design Dashboard template]( https://getmdl.io/templates/index.html ). 
For the map, the [Leaflet API]( https://leafletjs.com/ ) is used, version 1.3.0.

## QuizApp: the app structure

The app is developed by using the Material Design Dashboard template as base. The index.html file has been changed for what concerns its functionalities,
while the general structure remained the same. The body is composed of the left-side menu and the main interface where the Leaflet map is located. The left-side
menu contains the options that allow the app to fulfill its tasks; each button makes reference to a .js file which is located in the js folder. At the end of
the html code there are the scripts that provide the link to the respective js file. The main interface is between the <main> tags and contains four main divisions:
- the Leaflet map;
- the division that shows the user coordinates as soon as they activate the tracking;
- the question and the related answers;
- the button that allows to check the user's answer.
Some minor changes occur also in the <header>; the main title is turned into "UCL Quiz App" and the top-right menu contains the links to the documentation.  

## WebApp: the app struture

WebApp has a structure which is very similar to the QuizApp one, since the two apps has been developed by using the same criteria. Like the QuizApp, WebApp 
<<<<<<< HEAD
shows exactly the same structure of the top-right menu located in the "header", with the links to the documentation. The left-side menu, which compose the 
first part of the body, contains the buttons that add the functionalities to the app; the first one allows to open the "Question Form" to create new questions.
The html file of the form is located in the "www" folder, together with the index.html. The second option allows to load the points of interest already stored
in the database by using the loadPointData() located into a .js file; the script that makes reference to this function is located below in the html code. 
The main interface -between the "main" tags- is composed of the Leaflet map only. 
=======
shows exactly the same structure of the top-right menu located in the <header>, with the links to the documentation. The left-side menu, which compose the 
first part of the body, contains the buttons that add the functionalities to the app; the first one allows to open the "Question Form" to create new questions.
The html file of the form is located in the "www" folder, together with the index.html. The second option allows to load the points of interest already stored
in the database by using the loadPointData() located into a .js file; the script that makes reference to this function is located below in the html code. 
The main interface -between the <main> tags- is composed of the Leaflet map only. 
>>>>>>> 1cbb2ff61509bfcdb800af312bc09afad6e68204

## The server

The NodeJSserver.js file manages the upload/download of data. In the terminal, within the SFTP window, it is located in the folder with the following path:
/home/studentuser/code. A copy of the file is located in the "MyServer-QuizApp" folder which is the GitHub repository. However, the server is not able to 
manage the interactions between the apps and the database from this folder. For this reason, the NodeJSserver.js must be launched from the "code" folder -/home/studentuser/code path-.
If the user wants to launch the server, they need to type the following commands in the console:

```
$ cd /home/studentuser/code
$ node NodeJSserver.js
```

If the user wants to launch both the server and WebApp, they need to launch the server in background and then the Phonegap server from the app's folder:

```
$ cd /home/studentuser/code
$ node NodeJSserver.js &
$ cd /home/studentuser/code/WebApp/ucesibi
$ sudo su --> type the password (they need to access as superuser to start the phonegap server)
$ phonegap server
```

At this point both the server and WebApp are running, therefore the user can create new questions and upload them onto the database.

NB: QuizApp requires only the server (NodeJSserver.js).

## Further information

<<<<<<< HEAD
The following [link]( https://www.dropbox.com/s/od2t6g29cekp8u6/Web%26Mobile-Report.pdf?dl=0 ) provides further information about the development of the apps.
=======
The following [link](  ) provides further information about the development of the apps.
>>>>>>> 1cbb2ff61509bfcdb800af312bc09afad6e68204
