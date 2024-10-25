#  App Architecture Decisions

Contents:
  - [Summary](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#summary)
    - [Issue](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#issue)
    - [Decision](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#decision)
    - [Status](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#status)
  - [Details](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#details)
    - [Assumptions](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#assumtions)
    - [Constraints](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#constriants)
    - [Positions](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#positions)
    - [Argument](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#argument)
    - [Implications](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#implications)
  - [Related](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#related)
    - [Related decisions](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#related-decisions)
    - [Related requirements](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#related-requirements)
    - [Related artifacts](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#related-artifacts)
    - [Related principles](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#related-principles)
  - [Notes](https://github.com/Miiikeey/AppArchitecture/blob/main/index.md#notes)


##  Summary

### Issue
We need to determine some architecture decisions for each issues:
- Development Framework
- Navigation Strategy
- Hardware
- Database Storage
###  Decision
- For our development framework we decided on React Native as our team is very design centered. React Native is usually employed in the development of cross-platform applications, seeing that our device target is android were able to write code on JavaScript which will produce high quality UI and a smoother more responsive user ecperience.
- For our navigation strategy we decided on
- For our hardware we will need to support speakers, bluetooth, haptic feedback and GPS. Our music app will have direct access to device speakers, bluetooth will connect to devices outside the device speaker, haptic feedback will create a immersive feel, and GPS to recomend songs choices for certain locations.
- For our database storage we decided on SQLite as it was designed for mobile apps. It is compatible with React Native, and it works well with handling playlists, user preferences and more.
###  Status
Some architecural decisions were already set
- Target Devices: Android
- CSS Framework: Bootstrap

For the other architectural decisions we decided on:
- Development Framework: React Native
- Navigation Strategy:
- Hardware: Speakers, Bluetooth, Haptic Feedback, GPS
- Database Storage: SQLite (Open for other ones along the way)

##  Details

###  Assumptions
We are creating a music player app that provides a smooth and simple user experience, focusing on accessibility and performance. We assume that users will seek a minimalistic interface while expecting quick access to their music library and playback controls. 
###  Constraints
1. Performance on Low-End Devices: The application must perform efficiently on devices with lower specifications (e.g., 1GB RAM, basic processors) to reach a wider audience. 

2. Development Timeline: All development and testing phases must be completed by December 14, including iterations based on user feedback. 

3. Network Dependency: The app must provide some offline functionality to allow users to access previously downloaded content without an internet connection. 

4. Battery Consumption: The use of GPS and other hardware features must be optimized to minimize battery drain, maintaining user satisfaction. 

5. Security Compliance: The app must comply with data protection regulations, such as GDPR, ensuring user data privacy and security. 
###  Positions

###  Argument
Choosing React Native allows for rapid development and cross-platform support, which aligns with our project timeline. The framework's component-based architecture facilitates code reusability, leading to a quicker turnaround for features. Tab-based navigation enhances user experience by providing easy access to various features of the app, such as playlists, settings, and user profiles, thus minimizing navigation time. 
###  Implications
1. GPS Utilization: Utilizing GPS for location-based features may require users to grant additional permissions, which could impact their privacy perception. Clear communication about how this data will be used is essential. 

2. Remote Database Dependence: The choice of a remote database necessitates a stable internet connection for optimal functionality. Users should be informed about the need for an internet connection for features such as music streaming and content updates. 

3. Offline Mode: Implementing an offline mode will require local storage solutions to cache music and user preferences while ensuring that these are properly synchronized with the remote database once the connection is restored. 
##  Related

###  Related decisions

###  Related requirements
1. User authentication must be robust to ensure secure access to user accounts and personal playlists. This includes password encryption and secure login procedures. 

2. Data encryption for user data, both in transit and at rest, is crucial for maintaining user trust and complying with legal standards. 
###  Related artifacts
1. UI Wireframes: Initial design sketches that outline the layout and functionality of the app, serving as a guide for the development team. 

2. API Design Documentation: Specifications for the backend services that will interact with the mobile app, detailing endpoints, data formats, and authentication methods. 
###  Related principles
1. User-Centered Design: The app should be designed with the end user in mind, ensuring that features are intuitive and meet user needs. 

2. Maintainability and Scalability: The architecture should allow for easy updates and scaling as the user base grows, accommodating future feature additions without major overhauls. 
##  Notes
Further discussions are needed on specific GPS implementation and its impact on battery life. Team members should prepare for the next meeting by reviewing relevant documentation, including privacy policies related to GPS usage. Additionally, the feasibility of offline storage solutions should be explored to enhance user experience, especially in low-connectivity environments. Regular check-ins should be scheduled to ensure progress aligns with the December 14 deadline. 