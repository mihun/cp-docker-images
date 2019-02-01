Docker Images for Confluent Platform
===

Docker images for deploying and running the Confluent Platform.  The images are currently available on [DockerHub](https://hub.docker.com/u/confluentinc/).  They are currently only available for Confluent Platform 3.0.1 and after.

Full documentation for using the images can be found [here](http://docs.confluent.io/current/cp-docker-images/docs/intro.html).

# Build images based on OpenJDK-8-OpenJ9:
*Use Makefile to do all follow operations.*

Preperation:
1. clean-containers
2. clean-images

Install:
1. debian/base/include/etc/confluent/docker/docker-utils.jar 

*if mvn is not available by /bin/sh/ this step can be done from console*

*if parent pom is not resolved issue will be appeared - use WA that commented in pom.xml*

2. build-debian

Current component list in Makefile is related to kafka connect build and can be modified:

COMPONENTS := base kafka kafka-connect-base kafka-connect

# Important Caveat - Images Not Tested for Docker for Mac or Windows
	
These images are not tested on Docker for Mac or Docker for Windows. These images will be updated in the near future to support these platforms. For more details on these known issues, you can refer to the following links:

* [Hostname Issue](https://forums.docker.com/t/docker-for-mac-does-not-add-docker-hostname-to-etc-hosts/8620/4)
* Host networking on Docker for Mac: [link 1](https://forums.docker.com/t/should-docker-run-net-host-work/14215), [link 2](https://forums.docker.com/t/net-host-does-not-work/17378/7), [link 3](https://forums.docker.com/t/explain-networking-known-limitations-explain-host/15205/4)

# Contribute

Start by reading our guidelines on contributing to this project found [here](http://docs.confluent.io/current/cp-docker-images/docs/contributing.html).

- Source Code: https://github.com/confluentinc/cp-docker-images
- Issue Tracker: https://github.com/confluentinc/cp-docker-images/issues


# License

The project is licensed under the Apache 2 license. For more information on the licenses for each of the individual Confluent Platform components packaged in the images, please refer to the respective [Confluent Platform documentation for each component](http://docs.confluent.io/current/platform.html).  

