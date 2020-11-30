# Creating docker images for the bucketlist application
## setup
Docker installation [Go to the Downloading Web Site](https://docs.docker.com/get-docker/) 

## Bucketlist app (With ReactJS)
This app enables you to keep track of your goals. A bucketlist is a list of goals you wish to persue in the future, or just next week. Features include:

- Creating, editing and deleting bucketlists.
- Adding goals to bucketlists.
- Editing and deleting goals.
- Creating a user account, login and logout.

### Creating the frontend image
Entering to the directory where dockerfile is residing <br>

   *cd /bucketlist-react*

build the bucketlist react docker image  naming the image frontend <br>

   *docker build -t frontend .*

Run the image <br>  

   *docker run frontend*
 
### Creating the database image
Entering to the directory where dockerfile is residing <br>

   *cd /database*

Build the database image <br>

   *docker build -t database .*

run the database image <br>

   *docker run database*

### Creating the api image
This project is an API for a bucketlist app, that enables you to keep track of your goals or dreams.

Entering to the directory where dockerfile is residing<br>

   *cd /bucketlist-api*

Build the image <br>

   *docker build -t bucketlist_api .*
 
 running the image(_for this to run the database image must be running_) <br>
 
   *docker run bucketlist_api*


Documentation can be found at `/apidocs` when the app is running.
