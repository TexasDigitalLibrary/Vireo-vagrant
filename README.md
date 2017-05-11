Vireo Development Vagrants
==========================

These vagrants are to provision a virtual machine with Vireo and all its dependencies installed. Vireo will not be deployed in Tomcat, it will be manually started via maven spring-boot for development purposes. The vagrant will be running Vireo on port 9000, which must be available. The available operating systems for the guest virtual machine are all linux distributions; oracle, centos, and ubuntu. In order to use the vagrants please have the following prerequisites installed.

Prerequisites
-------------

Install the following software.

1.	[git](https://help.github.com/articles/set-up-git)
2.	[vagrant](https://www.vagrantup.com)
3.	[virtual box](https://www.virtualbox.org)
4.	[eclipse](https://eclipse.org/)

Setup
-----

Add the following required vagrant plugins.

1.	`vagrant plugin install vagrant-vbguest`

Provision VM
------------

Follow these instructions to provision the Vireo virtual machine.

1.	`git clone https://github.com/TexasDigitalLibrary/Vireo-vagrant.git`
2.	select desired operating system for the guest virtual machine: oracle, centos, or ubuntu -> [os]
3.	`cd [os]`
4.	`vagrant up` (this will take a while)

Start Vireo
-----------

Follow these instructions to start Vireo.

1.	`vagrant ssh`
2.	`cd Vireo`
3.	`mvn clean spring-boot:run`

Open Vireo
----------

Test Vireo in the browser.

1.	http://localhost:9000

Develop
-------

Import Vireo project into Eclipse

1.	open Eclipse
2.	open `File` menu
3.	select `Import`
4.	open `Maven`
5.	select `Existing Maven Projects`
6.	click `Next`
7.	navigate to the `Vireo-vagrant` directory
8.	navigate further to the `[os]/src/Vireo` directory
9.	click `Open` (should see the Vireo project)
10.	click `Finish`
11.	develop on Vireo
