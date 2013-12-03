## Deploy any Java app in 10 minutes

- Dokku (https://github.com/progrium/dokku)
- DigitalOcean (http://digitalocean.com)

### Quick setup for Dokku running at DigitalOcean

http://goo.gl/1UtP1X<br>
https://github.com/progrium/dokku#deploy-an-app

### Java application sample

Simple Maven project with maven-jar-plugin

https://github.com/mvberg/dokku-java-sample

### Remote push

<code>git remote add dokku dokku@SERVER:java-sample</code> <br />
<code>git push dokku master</code>

> Counting objects: 5, done.<br/>
Delta compression using up to 8 threads.<br/>
Compressing objects: 100% (3/3), done.<br/>
Writing objects: 100% (3/3), 632 bytes, done.<br/>
Total 3 (delta 1), reused 0 (delta 0)<br/>
...<br/>
remote: -----> Building one-tester ...<br/>
remote:        Java app detected<br/>
remote: -----> Installing OpenJDK 1.6... done<br/>
remote: -----> Installing settings.xml... done<br/>
remote: -----> executing /cache/.maven/bin/mvn -B -Duser.home=/build/app clean install<br/>
...<br/>
remote: -----> Discovering process types<br/>
remote:        Procfile declares types -> web<br/>
remote: -----> Releasing one-tester ...<br/>
remote: -----> Deploying one-tester ...<br/>
remote: -----> Cleaning up ...<br/>
remote: =====> Application deployed:<br/>
remote:        http://XXX.XXX.XXX.XXX:49156<br/>

### Confirm app is deployed

List deployed apps: <code>docker ps -a </code> <br/>
Get logs from app: <code>docker logs [CONTAINER_ID]</code>

Redeploy with <code>git push dokku master</code>

### Have a beer


