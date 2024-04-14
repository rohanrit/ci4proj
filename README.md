https://www.youtube.com/watch?v=N_FpDLtfXpk
1) create folder with project name "ci4proj"
1.1) make required changes to docker files
2) check docker is installed on your system and open CMD --> docker --version
2.1) check docker images on your system and open CMD --> docker images
3) copy the docker-compose.yml, dockerfile, makefile in your project file and run docker app
4) Open you project in VS code and run terminal, check if docker form microsoft extention is installed in vscode
4) run docker build in terminal --> docker-compose up --build
5) Open new terminal and run command --> docker ps
6) copy the codeignitor-docker project container id -- 1e9a8f75d1b6
7) run command -->  docker exec -it 1e9a8f75d1b6 bash
8) run command --> composer create-project codeigniter4/appstarter .
9) run command --> cp env .env
10) in .env file change environment to developemnt
11) create new controller with spark --> php spark make:controller welcomeController
12) Change routes from home to welcome controller --> $routes->get('/', 'welcomeController::index');
13) make project folder readable --> sudo chmod -R 777 cigniter-app (not required it is for linux)
14) make project folder editable (run the command direct in windows CMD not inside terminal) --> docker exec -it ci4-docker chown -R www-data:www-data /var/www/html/writable/
change <container_name> to cigniter4-docker 
15) change "public string $uriProtocol = 'REQUEST_URI';" to "public string $uriProtocol = 'PATH_INFO';"

run the project --> docker-compose up --build
start docker service on EC2 instance --> sudo service docker start
grant permission to docker --> sudo usermod -a -G docker ubuntu
check the current director in ec2 --> Password
make new directory --> mkdir sbtdev
go to the dirctory --> cd sbtdev/


project details: http://localhost:8080/public/
phpmyadmin details: http://localhost:8081/
Server: mysql_db
Username: root
Password: hellodemo