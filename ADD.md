# App Design Document

## Name: SchoolPool

### Purpose
To help families add, maintain, and join new carpools. 

### Audience
This app is intended to help families keep track of their transportation options and is particularly targeted toward families with students who do not drive to school. Parents can keep track of when and where they need to pick up students, and students can keep track of drivers, vehicles, and drop-off locations. 

### User Experience
One day at school, a student finds a club that interests them. They attend the introductory meeting at lunch. This student cannot or does not drive to school, so they hesitate before signing up, as transportation may prove to be a difficulty. 

Until now, to organize a carpool, the student would have to talk to other students and exchange parental contact information. Then the parents would need to set up a group message. If there are not enough people in the carpool, parents would need to search for other students and parents who also live near them and are interested in the club. 

This entire process breeds confusion and disorder. With SchoolPool, students and parents no longer have to go through this process just to organize a carpool.

After opening the app for the first time, parents and students make a family profile, in which they enter drivers, students, vehicles, location, available driving times, and school communities to join. The public only sees a designated family coordinator, who will be the point of contact for the family. 

Afterwards, the family can set up a carpool in the appropriate school community and invite other families. This carpool can be discovered by other families in the same school community, who can then request to join the carpool. The request can be approved by anyone already in the carpool who knows the outside family. Once the carpool has reached capacity, the organizer can mark it “Full” and it will no longer appear in search results. People within the carpool have access to everyone’s contact information, and they can even see what the driver’s cars look like so they know what to expect. Communication becomes quick and easy, and notifications remind members about their driving duties.

Now, when the student is at school, they can simply create a new carpool and wait for other users to start joining. Once enough members have joined, they can communicate pickup and drop-off information without worrying about asking for contact information or availability.

### Technical Details for Minimum Viable Product
#### External Services
* Firebase
* FB SDK
* Google Login SDK
* SwiftyJSON
* Alamofire
* Google Maps API

Also likely: Bolts, Bond, ConvenienceKit

#### Screens
Splash Screen: 
![Splash Screen](/PrototypeScreenshots/SplashScreen.png)

Sign Up/Login Screen:
![Signup Screen](/PrototypeScreenshots/Signup.png)

Home Tab:
![Home Screen](/PrototypeScreenshots/YourCarpools.png)

Search Tab:
![Search Screen](/PrototypeScreenshots/FindaCarpool.png)

Requests Tab:
![Requests Screen](/PrototypeScreenshots/Requests.png)

Profile Tab:
![Profile Screen](/PrototypeScreenshots/iPhone 6.png)

#### Data Model
Launchscreen.storyboard

##### View Controllers 
- Sign up/Login
- ⋅⋅⋅ SetupFamilyViewController
- Tab Bar Controller
- ⋅⋅⋅ HomeViewController
- ⋅⋅⋅⋅⋅ CarpoolDetailViewController
- ⋅⋅⋅ SearchViewController
- ⋅⋅⋅⋅⋅ SearchResultsViewController
- ⋅⋅⋅ RequestsViewController
- ⋅⋅⋅⋅⋅ CarpoolDetailViewController
- ⋅⋅⋅ ProfileViewController
- ⋅⋅⋅⋅⋅ FamilyProfileScopeView
- ⋅⋅⋅⋅⋅⋅  MemberViewController
- ⋅⋅⋅⋅⋅ GivenScopeView
- ⋅⋅⋅⋅⋅ TakenScopeView

##### Object Hierarchy
- School Community
- ⋅⋅⋅ Carpool
- ⋅⋅⋅⋅⋅ Family
- ⋅⋅⋅⋅⋅⋅  Family Member
- ⋅⋅⋅⋅⋅⋅⋅⋅⋅⋅ Email
- ⋅⋅⋅⋅⋅⋅⋅⋅⋅⋅ Profile Photo
- ⋅⋅⋅⋅⋅⋅⋅⋅⋅⋅ Number
- ⋅⋅⋅⋅⋅⋅⋅⋅⋅⋅ Driver Status boolean
- ⋅⋅⋅⋅⋅⋅  Vehicle
- ⋅⋅⋅⋅⋅⋅⋅⋅⋅⋅ Photo
- ⋅⋅⋅⋅⋅⋅  Ratio (rides taken vs given)
- ⋅⋅⋅⋅⋅⋅  School Communities that this family is a member of

### Ideas for Future Versions
