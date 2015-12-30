#EPA Prototype

FitAir is a prototype Android application that accesses the FitBit application programming interface (API) and AirNow data to allow FitBit users to view air quality conditions before undertaking exercise.  This information benefits people who may have health conditions affected by air quality (e.g., asthmatics) or those in compromised environments (e.g., non-attainment zones) to make healthier choices, while also providing data to environmental officials on exercise levels relative to air quality.  Additionally, this application can help EPA by identifying areas in the country where frequent exercise coincides with poor air quality, thus allowing for more targeted advisories to be issued. 

View our [concept video here]()

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


