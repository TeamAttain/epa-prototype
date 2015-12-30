#EPA Prototype

FitAir is a prototype Android application that accesses the FitBit application programming interface (API) and AirNow data to allow FitBit users to view air quality conditions before undertaking exercise.  This information benefits people who may have health conditions affected by air quality (e.g., asthmatics) or those in compromised environments (e.g., non-attainment zones) to make healthier choices, while also providing data to environmental officials on exercise levels relative to air quality.  Additionally, this application can help EPA by identifying areas in the country where frequent exercise coincides with poor air quality, thus allowing for more targeted advisories to be issued. 

View our [concept video here](https://www.dropbox.com/s/6liwtkqvoxv6kig/EPA-draft-VO.mov?dl=0).

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

* Download the [Android APK](https://www.dropbox.com/s/emmgjmug07ni7sh/app-debug.apk?dl=0)
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

Team Attain held daily standup calls to check in on progress, discuss blockers, and ensure that all project work was being completed to spec. Development followed a strict process, going through peer code review as well as automated unit testing and manual user testing before being accepted as done. 

## Product Philosphy 

To know what is valuable to users, to validate our work, and to design the “wow”  elements of a product, we must know our users extremely well.

1.	Build fast. Test. Learn. Improve. Repeat.
2.	Prioritize delivery of more user value, not more features.
3.	Involve users early and often
4.	Until users validate our work, everything is a hypothesis.
5.	Delivering the “wow” elements of a product are equally as important as delivering the basic must-have requirements, but the must-haves must come first.

## Stages of Product Development

The short timeline of this project meant that discovery and delivery were happening simultaneously. In order to ensure that we delivered a quality end product, we developed a specific set of user stories while continuing to explore new ideas through design iterations. The timeline did not allow for additional market research, user research, or user testing - which would likely drastically change the end product delivered if completed. Note: for this exercise the Team Attain acted as the end user role and incorporated Customer-Centric Development.

For a complete list of future user stories, see the backlog of [our trello board](https://trello.com/b/IdjoinrZ/epa-prototype).

## Project Timeline, Challenges, Iterations

### Timeline:
* Project start - 12/2
* Project end - 12/30
* Total Duration - 4 weeks
* Total Working Days - 19

**12/2/15 | Initial Project Premise**
* Compare AQI air quality data with user collected activity data from FitBit devices

**12/9/15 | Technical Discussions**
* Project architecture is finalized
* Initial user stories are discussed & revised

**12/15/15 | Pivoting**
* Initial designs are reviewed
* Android is successfully retrieving FitBit Data
* Staging site is configured and is displaying data from an AQI CSV dump
* Project shifts from a focus on granular data analysis for the EPA, to a more broad focus on how air quality alerts and education may impact user decision making when choosing how to exercise. More emphasis is placed on the end user of the Android application.

**12/18/15 | Pivoting, Settling, Finalizing**
* New discussion around usefulness and accuracy of indoor/outdoor idea
* New ideas proposed for instead showing user the percentage of activity time they log within each AQI category - instead of indoor/outdoor classification as this does not tend to differ significantly 
* Due to holiday vacation time, it is determined that Android has approximately 3 working days until deadline
* Decision is made to stay the course for development, but iterate new ideas through the design process

**12/29/15 | System testing and Prototype Retrospective**
* End-to-end testing conducted
* Retrospective/Lessons Learned conducted

##Lessons Learned
The Attain Team reflected the iterative design/development of this prototype and identified actions for future improvement:
* Team co-location wasn’t always possible.  Use of the web application Slack improved team communication and product quality
* The team started development of first concept quickly and further designs/features could not be implemented in time allotted.  Additional design iterations prior to development may allow for a more comprehensive application.

#For More Information

* [AQI Official Website](http://airnow.gov/index.cfm?action=aqibasics.aqi)
* [AQI Handbook](http://www3.epa.gov/airnow/flag/handbook-2015.pdf)
* [FitBit Developer API](https://dev.fitbit.com/)
* [Google Places API](https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=google%20places%20api) - used on Android for gathering location data from the user.


