#EPA Prototype

FitAir is a prototype Android application that accesses the FitBit application programming interface (API) and AirNow data to allow FitBit users to view air quality conditions before undertaking exercise.  This information benefits people who may have health conditions affected by air quality (e.g., asthmatics) or those in compromised environments (e.g., non-attainment zones) to make healthier choices, while also providing data to environmental officials on exercise levels relative to air quality.  Additionally, this application can help EPA by identifying areas in the country where frequent exercise coincides with poor air quality, thus allowing for more targeted advisories to be issued. 

[![ScreenShot](https://www.dropbox.com/s/6liwtkqvoxv6kig/EPA-draft-VO.mov?dl=0)

#Repositories

* [Android](https://github.com/smashingboxes/epa-prototype-android)
* [Frontend](https://github.com/smashingboxes/epa-prototype-frontend)
* [API](https://github.com/smashingboxes/epa-prototype-api)

## How to synchronize scripts

```
./sync
```

## Deployment

This application uses [Anisble](http://www.ansible.com/) for server management and application deployment.

### Deploy to existing server

**:bangbang: You must have ssh access to the server**
```
./sync
cd epa-prototype-api
tape ansible deploy
```

### Provisioning a new server

**:bangbang: You must have ssh access to the server**

```
./sync
cd epa-prototype-api
```

1. Update the IP address in the `taperole/hosts` file to the IP address of your server.
2. Ensure you have ssh access as root to that server.
2. Ensure that Ubuntu 14.x LTS is the OS

```
tape ansible everything
```
# Demo Instructions

To demo as an end user, you must have a fitbit account and Android device. If you do not have one or both of the required devices, you can watch our demo video [here](https://www.dropbox.com/s/y96wiw1notdg6p5/2015_12_30_08_10_09.mp4?dl=0).

* Download the [Android APK]()
* Your device will prompt you to install, and then open
* Click to 'Sign in with FitBit'
* Enter your FitBit account email address and password
* Select your location
* Return to view current AQI and activity data
* Please note that our application tracks manually added activity via the FitBit API. Your automatically tracked step data will not be represented here. For information about how to record your activity, [visit FitBit help](https://help.fitbit.com/articles/en_US/Help_article/How-do-I-use-exercise-mode-on-my-tracker). 

To demo as an EPA user, visit [our staging site here](http://epa-prototype.sbox.es/air_quality_observations/27601).

# Project Process

##Project Documents / Information
* [Technology Architecture](https://www.dropbox.com/s/vqho1tkfqv2lztl/prototype-architecture.pdf?dl=0)
* [Initial Sketches](https://www.dropbox.com/s/73h1srrmh5wdgzo/sketch-set-1.pdf?dl=0)
* [Design Iteration 1](https://www.dropbox.com/s/18ei84vbl2h256q/airfit_v1.pdf?dl=0)
* [Design Iteration 2](https://www.dropbox.com/s/ifxev70hmz8w4dy/airfit_v2.pdf?dl=0)
* [Design Iteration 3](https://www.dropbox.com/s/3rz531dy0651ugz/airfit_v3.pdf?dl=0)
* [Design Iteration 4](https://www.dropbox.com/s/e9uc20vzedlvk56/airfit_v4.pdf?dl=0)
* [Additional Sketches](https://www.dropbox.com/s/t8wrq65da0azznh/sketch-set-2.pdf?dl=0)
* [Initial User Stories](https://www.dropbox.com/s/tm3n68whdlp325c/EPA%20Prototype%20User%20Stories_cfd.xlsx?dl=0)
* [Trello Board](https://trello.com/b/IdjoinrZ/epa-prototype)

## Process Approach

Team Attain approached this project using a [Trello KanBan board](https://trello.com/b/IdjoinrZ/epa-prototype) to create and manage user stories. It was determined that a traditional sprint schedule was not appropriate given the timeline constraints and holiday scheduling.







