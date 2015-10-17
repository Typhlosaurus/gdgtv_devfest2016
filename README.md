# devfest2015
Material Design App Engine Template for DevFest 2015 Season

This is a fork of [devfest2015](https://github.com/ajmikzer/devfest2015), restructured as a [Google App Engine](https://cloud.google.com/appengine/) template. Includes some inspirations from project [zeppelin](https://github.com/gdg-x/zeppelin).

Demo can be found here: http://rtv-devfest.appspot.com

## Prerequisites
* [Apache Maven](https://maven.apache.org/download.cgi).
* Java 7.

## Quick start
* Create a new [cloud console project](https://console.developers.google.com/project). Note the project id.
* Development:
```
git clone https://github.com/omerio/devfest2015.git
cd devfest2015
mvn install
#to test it locally:
mvn appengine:devserver
```
* App Engine local server packages the project as a war before running it, if you are on Mac OSx you can use a simple http server during development as explained [here](http://www.andyjamesdavies.com/blog/javascript/simple-http-server-on-mac-os-x-in-seconds)
```
cd src/main/webapp/
python -m SimpleHTTPServer 8080
```
* To deploy it to App Engine, update the `<app.id>rtv-devfest</app.id>` property in pom.xml with your project id
* Deploy the app:
```
mvn appengine:update
```
