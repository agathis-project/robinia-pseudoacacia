```
AP:      6
Title:   Remote Test Station
Repo:    robinia-pseudoacacia
State:   Draft
Type:    Development
License: CC BY-SA / GPL
Author:  jonsnow1357
```

# AP Guideline

## 1. Abstract

It is expected that the work on this project will include participants spread
across different locations, and some will need access to the actual HW
developed by the project. This document specifies the current lab setup used
and the methods to allocate and access the equipments in the lab.

## 2. Rationale

To access the HW board(s) for development and/or debug the current solution is
based on the following:

* [VPN](https://en.wikipedia.org/wiki/Virtual_private_network)
* [raspberry pi](https://www.raspberrypi.org/)

A high level view of the lab setup is the following:

![Remote Test Concept](https://github.com/agathis-project/robinia-pseudoacacia/blob/AP-6_Draft/doc/AP-6_concept.png)

It consists of:

* DUT - the HW board made by the project
* Test Unit - **raspberry pi** (rpi) + DUT
* Lab Sites - the place where Test Units are located

The private network connects the Lab Sites and the developers.
This allows for easy geographical relocation/extension of the Test Units and
also access from almost anywhere for the developers.

Also the current solution assumes that the **rpi** can be used as
a cheap front-end interface for:

* programming uC/flash devices on the HW board
* access debug UART/I2C/SPI ports on the HW board
* monitor various digital signals

## 3. Lab Setup

### 3.1. Deployment

A Lab Site is anywhere a number of Test Units are located and connected to the private network. This is usually administrated by a member of the project who aggrees to supervise the access to the Test Units and fix any problems with them

Currently there are **0** Lab Sites.

### 3.2. Getting Access

Any commercial or free VPN solution should be good for this setup as long as all the users agree on it.

The current VPN used is [Hamachi](https://www.vpn.net/).

To ask for access to one of the HW boards just open a issue in this project.

Usually the Lab Site administrator will provide you with VPN access information, the IP and SSH login of the Test Unit you're supposed to use and answer any other reasonable questions you might have.

After you have that information, try to access your Test Unit. All rpi will have a control web interface available at http://<rpi_IP_address>:8100

## 4. References

## 5. License

* This document is licensed under Creative Commons Attribution-ShareAlike 4.0
  International License ([CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/))
* All code is licensed under [GPL v3](https://www.gnu.org/licenses/gpl.html)
