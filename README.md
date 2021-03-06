# <a href="https://github.com/rhildred/hellophonegap" target="_blank">hellophonegap</a>

phonegap hello world. The config.xml sets the name and id:

```

<?xml version="1.0" encoding="UTF-8" ?>
<widget xmlns="http://www.w3.org/ns/widgets" xmlns:gap="http://phonegap.com/ns/1.0" id="io.github.rhildred.hellophonegap" version="0.0.1">

    <name>hello phonegap</name>

    <description>
        most basic of examples, responds to deviceready
    </description>
    <content src="index.html" />
    <author href="https://rhildred.github.io">
        Rich Hildred
    </author>
    <access origin="*" />
</widget>

```

The html5 phonegap code includes the javascript `cordova.js` file, which will be replaced during the build by a cordova.js that is built on the fly.

```

<!Doctype html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
    </head>
    <body>
        <h1>hello phonegap</h1>
        <h2> I can't believe it's this simple. ... </h2>
        <div id="connectionStatus" style="color:blue">Not connected to phonegap!</div>
        <script src="cordova.js"></script>
        <script>
            var phonegapReady = function(){
                oStatus = document.getElementById("connectionStatus");
                oStatus.innerHTML = "Now connected to phonegap";
                oStatus.style.color = "green";
            }

            document.addEventListener("deviceready", phonegapReady, false);

        </script>
    </body>
</html>

```

To test this in a local environment:

1. `npm install -g ripple-emulator` if you haven't already
1. `ripple emulate`
1. If your browser doesn't open up with your project in it surf to `http://localhost:4400/?enableripple=true`

To get the phonegap ready event select Cordova 2.0.

This can be loaded up on phonegap build, and turned into a apk that can be put on your phone.
To install this on phonegap build:

1) sign up for an adobe account and log in to https://build.phonegap.com
2) push this on to your own github
3) create an app on phonegap build
4) Click the `ready to build` button.
5) Download the APK on to your local machine.
6) Install [BlueStacks](https://www.bluestacks.com/download.html) if you haven't already.

![telechargement](https://rhildred.github.io/hellophonegap/readmeimages/BlueStacksCapture.PNG "telechargement")

7) Load the apk into BlueStacks

![install apk](https://rhildred.github.io/hellophonegap/readmeimages/installApkCapture.PNG "install apk")

8) Click on the app in your home screen

!["spy in this case"](https://rhildred.github.io/hellophonegap/readmeimages/HomeScreenCapture.PNG "spy in this case")

