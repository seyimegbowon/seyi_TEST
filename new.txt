# MEAN STACK DEPLOYMENT TO UBUNTU IN AWS

> *Task: To implement a simple Book Register web form using MEAN stack*

# *Step 1: Install NodeJs*

sudo apt update

sudo apt upgrade

Add certificates

sudo apt install -y nodejs

# *Step 2: Install MongoDB*

To add fields to our db (MongoDB), fields required for the Book Record and its contents

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6

echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list

*To Install and Start MongoDb*

sudo apt install -y mongodb

sudo service mongodb start

*To check service status*

sudo systemctl status mongodb

![Screenshot from 2022-07-25 11-18-16](https://user-images.githubusercontent.com/106885875/180780159-f27f397b-13d1-419a-912c-f49d77f22319.png)

*To Install NPM and  body-parser package*

sudo apt install -y npm

sudo npm install body-parser

> COMMENT: While installing NPM, I had an error that NPM not supported by my Node.js version, so I had to upgrade to Node v 12 before the error cleared
> Node js upgrade to v12 via this command

*curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -*

*sudo apt-get install -y nodejs*
#### Credit: https://www.codegrepper.com/code-examples/shell/update+node+10+to+12+ubuntu


mkdir Books && cd Books

In Books dir;

npm init

create a new file in this directory and update its content appropriately

server.js

# *Step 3: Install Express and set up routes to the server*

sudo npm install express mongoose

> Mongoose provides a straight-forward, schema-based solution to model your application data; it establish a schema for the database to store data of our book register.

*In Books Directory*

mkdir apps && cd apps

create a new file in this directory and update its content appropriately

routes.js

*In Apps Directory*

mkdir models && cd models

create a new file in this directory and update its content appropriately

book.js

*In Books Directiry*

mkdir public && cd public

create a new file in this directory and update its content appropriately

script.js

Also

create a new file in this directory and update its content appropriately

index.html

### At the root directory; (Books) Start the server by running this command;

node server.js

![Screenshot from 2022-07-25 12-45-28](https://user-images.githubusercontent.com/106885875/180784078-3fd4ad18-9dee-4d16-b413-4cdd4bdc8b6e.png)

*To test what curl command returns locally, via port 3300*

curl -s http://localhost:3300

![Screenshot from 2022-07-25 12-56-53](https://user-images.githubusercontent.com/106885875/180784537-16087c74-d6e3-4a72-b001-d9d1c71dd80e.png)

![Screenshot from 2022-07-25 12-57-03](https://user-images.githubusercontent.com/106885875/180784582-67beea94-4c77-4326-8778-b6427552735c.png)

*TCP Port 3300 opened on my EC2 instance and puclic IP launched on my browser*

http://44.206.225.69:3300/

![Screenshot from 2022-07-25 12-53-57](https://user-images.githubusercontent.com/106885875/180785149-d0520807-c289-4137-902d-d5c5d4fc3d5f.png)


> ## *Task Beautifully Completed :)*




