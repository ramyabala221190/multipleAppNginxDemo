1. Create empty workspace
ng new multipleAppNginx --create-application=false 

2. Generate 2 applications within the workspace
ng g application firstApp

ng g application secondApp

3. Update the base href in the index.html in the 2 applications
Update the <base href> in the firstApp project to "/first/"

Update the <base href> in the secondApp project to "/second/"

firstApp is deployed to /usr/share/nginx/html/first (Check Dockerfile)

secondApp is deployed to /usr/share/nginx/html/second (Check Dockerfile)

4. Run "docker compose build" and "docker compose up". We have a single docker container and single nginx server.

nginx root directive location is /usr/share/nginx/html

5. Deployment details

localhost:8082/first/ will take us to firstApp

localhost:8082/second/ will take us to secondApp

