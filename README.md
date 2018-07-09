 As part of creating addons for maximo we see that IBM's contribution and development of well written tool helps a lot (ibm-maximo-dev).

To make the build environment clean and light weight thought of making that as a dockerized environment. Which in turn can be distributed to the developers without any hassle.

 

Below attached Dockerfile contains a Ubuntu 14.04 image which comprise Java 8,node,maximodev-cli.

All you need to do is to add the Docker file to your SMP folder and run the below command to build a clean image with addon support for maximo.

docker build -t anyname . --nocache

Here nocache is to ignore previous cached layers if that fails in middle this will help.

Once the image is built sucessfully you can run

In case  you forget the name you gave during the build. You can list the existing images by using

docker images command

docker run -it name you mentioned in the previous build /bin/bash

You will be now into the container Holla..

Start building addons to your base maximo. 
