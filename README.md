# work_sample_1
Dockerizing a bucketlist application

# Bucketlist app (With ReactJS)
This app enables you to keep track of your goals. A bucketlist is a list of goals you wish to persue in the future, or just next week. Features include:

- Creating, editing and deleting bucketlists.
- Adding goals to bucketlists.
- Editing and deleting goals.
- Creating a user account, login and logout.

## setup
install docker on your machine and make sure its running 

## Installation
Enter to the dockerfile directory
- "cd /bucketlist-react"

build the bucketlist react docker image 
- "docker build -t frontend ."

Run the image 
- "docker run frontend"

You can now view bucketlist in the browser.
-  http://[yourlocalhost]:3000/

**Checkout the live app on heroku**

https://bucketlist-john555.herokuapp.com

# Database image to work with api 

## setup
install docker on your machine and make sure its running 

## Installation
Enter to the dockerfile directory
- "cd /database"

Build the database image
- "docker build -t database ."

run the database image
- "docker run database"

# Bucketlist API

This project is an API for a bucketlist app, that enables you to keep track of your goals or dreams.

## How to run the app
Enter to the dockerfile directory
- "cd /bucketlist-api"

Build the image 
- "docker build -t bucketlist_api ."
 
 running the image(_for this to run the database image must be running_)
 - "docker run bucketlist_api"
 
 Now you can view it on your browser 
 http://[yourlocalhost]:5000

## Documentation
Documentation can be found at `/apidocs` when the app is running.
