# Compete Running

## General Description:
Compete Running is my senior project - I graduate May 11 2019 and currently looking for a permanent job. Compete Running is a web application built to use trademarked running performance scoring system of the same name. Webapp synchronizes users' run metrics from tracking service API and combines them with weather service API data on temperature, dew point and wind speed at time and location of the run. This data is used to calculate intermediate scores based on each metric and a total score. All of the parameters are then visualized for a user in an interactive chart providing reach opportunities for exploration. 

### Technology used:
Core: Node.js, Express, Angular, MySQL
Testing: Jest, SuperTest
Vizualizations: Chart.js
Deployment: AWS S3, ElasticBeanstalk, RDS

Here is a high-level diagram of application logic

![Chart](img/E2E.png)

### User Stories:
* I am a user, I login from desktop and want to find out how popular some band is today. 

![Desktop use case](gitimages/pc.gif)

* I am a user, I login from my smartphone and want to find out how popular some song is today.

![Desktop use case](gitimages/phone.gif)

### Notable features:
* Custom router. This app uses custom-built router, that is asynchronously loading HTML elements onto the page via Fetch API to imitate SPA functionality - page change without page reload. 

* Responsive design. Mainstream Meter is fully responsive across a wide range of devices using media queries and responsive images. Units used for majority of properties are rem, vw, vh for best experience of users with both default and custom browser font size. 

![Desktop use case](gitimages/res.jpg)

* Login via token. To login user is redirected to Spotify website, which returns token in URL hash. Token is extracted after redirect and stored in Local Storage reflecting expiration time. If user reloads page, valid token will allow user to use app immediately, while expired token would ask user to sign in. 


