VISVESVARAYA TECHNOLOGICAL UNIVERSITY, BELGAUM, KARN![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.001.png)‘ ATAKA

![](Photo/Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.002.jpeg)

MAJOR-PROJECT REPORT ON

“BlueChat: Bluetooth Chatting App”

Submitted in partial fulfillmentof the requirement for the award of the degree of

BACHELOR OF ENGINEERING

IN

COMPUTER SCIENCE AND ENGINEERING

Submitted By

Gaurav Kumar 2SD18CS035 Kashis Agarwal 2SD18CS046 Maruti Nandan 2SD18CS055 Shashank Raj 2SD18CS095

Under the Guidance of

Dr. S.M. Joshi

Dept. of CSE, SDMCET, Dharwad

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.003.png)

DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING S.D.M. COLLEGE OF ENGINEERING & TECHNOLOGY,      DHARWAD-580002

2021-2022

S.D.M COLLEGE OF ENGINEERING & TECHNOLOGY,![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.004.png)

DHARWAD-580002

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.005.png)

DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING

CERTIFICATE

Certifiedthat the Major-Project work and presentation entitled “BlueChat: Bluetooth Chatting App” is a Bonafide work carried out by Gaurav Kumar (2SD18CS035), Kashis Agarwal (2SD18CS046), Maruti Nandan (2SD18CS055), and Shashank Raj (2SD18CS095) , students of S. D. M. College of Engineering & Technology, Dharwad, in partial fulfillment for the award of Bachelor of Engineering in Computer Science and Engineering of Visvesvaraya Technological University, Belgaum, during the year 2021-2022. It is certified that all corrections/suggestions indicated for internal assessment have been incorporated in the report deposited in the department library. The Major-Project has been approved, as it satisfiesthe academic requirements in respect of project report prescribed for the said degree.

—————————- —————————- Dr. Shrihari M. Joshi Dr. Shrihari M. Joshi

Project Guide HOD-CSE

External Viva

Name of Examiners Signature with date

\1.

\2.

ACKNOWLEDGEMENT![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.006.png)

We consider it a privilege to express our sincere gratitude and respect to all those who guided and inspired us throughout this project.

We express our heartfelt thanks to our guide Dr. S.M. Joshi, HOD, Department of Computer Science and Engineering, S.D.M. College of Engineering and Technology, Dharwad, for his valuable suggestions and guidance during the course of this project. The successful completion of this project owes to his coordination and streamlining of the project progress.

We extend our gratitude to our Project Coordinator(s) Prof.Anand D Vaidya, Prof. Anand Pashupatimath and Prof Yashodha Sambrani.We would also like to thank Department of Computer Science and Engineering, S.D.M. College of Engineering and Technology, Dharwad, for their valuable suggestions and guidance during the course of this project. We are thankful to Dr.S.M. Joshi, Head of the Department, Department of Computer Science and Engineering, S.D.M. College of Engineering and Technology, Dharwad, for his encouragement and help throughout the BE course. We acknowledge gratitude to Dr.K.Gopinath, Principal, S.D.M. College of Engineering and Technology, Dharwad, for his timely help and inspiration during the tenure of the course. We would like to thank all teaching and non-teaching staff of CSE department, SDMCET, for helping us to carry out our project successfully.

ABSTRACT![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.006.png)

With the development of digital technologies in recent decades, there has been drastic change in the mode of communication and usages of digital accessories in our today lives. It is sure that invention of mobile phone/smart phone has enhanced our life standard and made life easier. The main aim of this research paper is to analyze, design, build and test Bluetooth chat software. The software has been developed as an Interactive and collaborative learning aid. That tool could benefit students in general specially students with disability. Using the developed system, disable students can connect with their peer students, who are within Bluetooth range, without having access to Wi-Fi or Internet. The application does not require any Internet connection, the application works just with Bluetooth connectivity, users can send free message to their friends sitting over classroom, school playgrounds and festivals, when nearby, without a cellular connection or Wi-Fi. Moreover, the application is very easy to use. Bluetooth messaging is also great for making new friends in a library or chatting up someone in crowded places, because one can hook up with anyone who has a Bluetooth-enabled phone.

BlueChat allows you to see other BlueChat allows you to see other Bluetooth Chat users around, ping anyone of them, and create private chat sessions. This application allows two Android devices to carry out two-way text chat over Bluetooth. Start the application from the first screen; Sign Up in the Application page and then go to Login page, where user will be logged into main chatting screen where the App provide the basic chatting operation. Connection option which attempts to discover other users in the area. Detected user-profiles are listed as select-able Drop down options. While a profileis selected, user can initiate a chat with the friend.

BlueChat: Bluetooth Chatting App

Contents![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

1 Problem Statement 3 2 Introduction 4 3 Literature Survey 9 4 Detailed Design 12 5 Project SpecificRequirement 16 6 Implementation 18 7 Result 20 8 Conclusion 22 9 References 23

List of Figures![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

1. Bluetooth ProfileStack . . . . . . . . . . . . . . . . . . . . . . . . . 6
1. Bluetooth ProfileHierarchy . . . . . . . . . . . . . . . . . . . . . . . 7
1. Comparison of Wireless Communication Technologies . . . . . . . . 8

3.1 Flow Diagram . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10

1. System Architecture . . . . . . . . . . . . . . . . . . . . . . . . . . . 12
1. Use Case Diagram - 1 . . . . . . . . . . . . . . . . . . . . . . . . . . 13
1. Use Case Diagram - 2 . . . . . . . . . . . . . . . . . . . . . . . . . . 14
1. System Architecture . . . . . . . . . . . . . . . . . . . . . . . . . . . 15
1. Sign-up Page . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
1. Sign-in Page . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
1. BlueChat App . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21

Chapter 1 Problem![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png) Statement

This project is to create a Bluetooth chat application which enables the users to chat with each other’s.

To develop an instant messaging solution to enable users to seamlessly communicate with each other’s without the use of internet.

Chapter 2 Introduction![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

The Bluetooth Chat Messenger application proposed by this paper is a two-way, sending and receiving, text chat program for any device, i.e. phones, tablets, computers, e-book etc., These devices are largely used in open and closed spaces; and everywhere as streets, squares, hotels and other places. The Bluetooth Chat Messenger does not require a GSM or Wi-Fi connection, all it needs is two Bluetooth compatible Android devices in range of about 50 feet of each other.

The proposed Bluetooth Chat Messenger application has advantages over existing applications. It works as a client and a server at the same time speaking from network wise or perspective of view. The application creates a server then waits for another client to connect to it (i.e., Server situation); or ask another device to chat with it (i.e. Client situation). It has a friendly graphical user interface (GUI) using well-proportioned and harmonious colour within its interface. It is easy to use. It cans also, beside exchanges text messages, sends smiley.

Introduction to Bluetooth

Bluetooth® is a Wireless Technology for Communication of Voice and Data, based on Short-range Radio Standard. Designed for OTA -Over the Air communication to eliminate the cables connected among devices which arc at small distances. The main task was to move away from electronic equipment cables, which are interconnected amongthem. Afterthediscoveryofitspotential,begantorapidlyincreaseitspopularity. today as integral part of any better equipped mobile phone. members.

Using Bluetooth

Bluetoothtechnologyhastodaycountlessdifferentusesinmanyindustries. Thefollowing list indicates some areas where the Bluetooth technology no longer applies.

1. Datacommunicationbetweentwoidenticaldevices(Mobilephones,PDAdevices, laptops, etc.)
2. Data communication between two different devices (PC and mobile phone, PC and PDA, mobile phone and printer,![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png) etc.)
2. Voice transmission between mobile phone and hands free set.
2. Connection to PC peripherals (keyboard, mouse, headset, printer).
2. Voice transmission between mobile phone and hands free set.
2. Connection to PC peripherals (keyboard, mouse, headset, printer).
2. Ad-hoc local area network between computers.
2. Remote control devices in the home (PC, etc.).

Other uses of Bluetooth can specify the programmer himself. And simply by typing application working with this driver and install it in appropriately equipped facilities. Alternatively they may also offer equipment itself to suit the exact requirements of its application.

Bluetooth Protocol Stack

Core Bluetooth specification is called ”Bluetooth protocol stack, which defines how a technology works. Bluetooth divides the individual layers, much like ISO OSI model ofcomputernetworks. HischartshowsinFig, thelowerlayerfromhigherseparatesthe so-called HCI (Host Controller Interface). Radio is the lowest layer, which takes care of modulation and demodulation signals and describes the physical requirements for Bluetooth transmitter and receiver of a particular device. Baseband I Link Controller layer handles format data into a form suitable for transmission by air and requirements forBluetoothtransmitterandreceiverofaparticulardevice. BasebandILinkController layerhandlesformatdataintoaformsuitablefortransmissionbyairandsynchronization connections. Link Layer manager will establish and maintain connections between devices. Like in computer networks, here we distinguish by type of communication connection is established. There are two types of communication:

1. Synchronouscommunicationmergers-Synchronous,Connection-OrientedSCO), mainly used for voice communication (e.g. headset profile)
1. Asynchronous communication without joining - Asynchronous, Connection-less (ACL) suited mainly for data communication

HCI (Host Controller Interface) is responsible for co-operation of higher layers with lower layers (Radio, Baseband, Link manager). The higher layers such as L2CAP (LogicalLinkControlandAdaptationProtocol), whichisresponsibleforencapsulating packets into a format suitable for the lower layer connection multiplexing, so that could be used more applications etc. SDP (Service Discovery Protocol) formulate

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.008.png)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 2.1: Bluetooth ProfileStack

action in offering a search of Bluetooth devices. RFCOMM layer allows emulating a serial connection cable, with all the specificsof the standard RS-232. So they can via Bluetooth communication applications designed for serial communication.

Bluetooth Profiles

For a device to use the Bluetooth technology must be able to interpret individual Bluetoothprofiles. Theyaretheretopreventanyincompatibilitywaseliminateddeveloped programs for Bluetooth devices of different manufacturers. Each profile represents a different application, or any other task.

Its specificationmust include:

1. Dependencies on other profiles
1. The proposed user interface formats
1. Parts Bluetooth protocol stack used by the profile

A Bluetooth device can support one or more profiles. The four ”basic” profiles are

the Generic Access Profile (GAP), the Serial Port Profile(SPP), the Service Discovery Application Profile (SOAP), and the Generic Object Exchange Profile (GOEP). The

GAP is the basis of all other profiles. Strictly speaking, all profiles are based on the

GAP. GAP definesthe generic procedures related to establishing connections between twodevices,includingthediscoveryofBluetoothdevices,linkmanagementandconfiguration, and Procedures related to use of different security levels. The SOAP describes the fundamentaloperationsnecessaryforservicediscovery. Thisprofiledefinestheprotocols

and procedures to be used by applications to locate services in other Bluetooth enabled

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.009.png)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 2.2: Bluetooth ProfileHierarchy

devices. The SPP defines the requirements for Bluetooth devices necessary for setting up emulated serial cable connections using RFCOMM between two peer devices. SPP directlymapstotheRFCOMMprotocolandenableslegacyapplicationsusingBluetooth wireless technology as a cable replacement.

The GOEP is an abstract profileon which concrete usage case Profilescan be built. These are profiles using OBEX. The profile defines all elements necessary for support of the OBEX usage models (e.g., file transfer, synchronization , or object push). The basic profiles-GAP SDAP, SPP and GOEP-also are known as transport profiles, Upon which other profiles,known as application profiles,can be built.

Comparison to other Technology: Why not others?

There are many short-range wireless standards, but the three main ones are Infrared from the Infrared Data Association® (IrDA®), Bluetooth wireless technology and wireless local area network (WLAN). WLAN is also known as IEEE 802. l l and

it comes in three main variants, 802.11b and 802. l lg, which operate at 2.4 gigahertz (GHz),and802.11a,whichoperatesat5GHz. TheIrDAcreatedawirelesscommunications system that makes use of infrared light. Whereas RF communication can penetrate many objects, IrDA is limited to line of sight. Both 802.11b and Bluetooth wireless technologies communicate in the 2.4-GHz RF band but are aimed at different market segments. The 802.11b technology has a longer range but consumes substantially more power than Bluetooth wireless technology. The 802.11 variant is primarily for data. The only protocol for supporting voice is Voice over Internet Protocol (VoIP). Comparison of Wireless Communication Technologies.

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.010.png)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 2.3: Comparison of Wireless Communication Technologies

Introduction to Firebase

Firebase is a NoSQL database which make use of sockets which allows the users to store and retrieve the data from the database . An Android version should be greater than 2.3, android studio 1.5 or higher version, and android studio project are the prerequisites to connect the firebase to an android application. Firebase provides a various kind of services such as: Firebase Authentication: Firebase Authentication is useful to both developers and the users. Developing and maintaining sign-in set-up may be a bit difficultand time taking. Firebase provides an easy API for sign in. It also providesthedatabackupusingrealtimedatabases. Firebasecloud: Forstoringthedata such as video, text, pictures building the infrastructure would be difficultand expensive for a new developer so the firebase provides the platform of cloud storage . Real time database: It is a cloud hosted NoSQL database. Apart from the authentication, cloud service and real time databases firebase.

Chapter 3 Literature![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png) Survey

There were previous attempts to make a similar application. As far as it shows on market.android.com ,the official Google’s Android market, there are some attempts to do applications with the same type and idea as the proposed application with little success. For example application “feeble”; as Google’s Android market shows, user’s reviews shows dissatisfaction with the application (i.e. reviews of the users said: “Couldn’t connect to a friend’s phone.”, “Crashes constantly on Android”).

The first and foremost step is to search for nearby devices, which is also known device inquiry. Every Bluetooth hardware comes with a globally unique 48-bit address referred to as the Bluetooth address.

When a Bluetooth enabled devices inquiries about the nearby devices its actually, they enquire about this 48-bit address. For two devices to communicate with each other both of them should know each other’s Bluetooth address. The next step is to query each device for its device name. Every Bluetooth device can be given a Bluetooth name which will work as alias for the Bluetooth address. Whenever a device searches for its nearby devices, it actually asks their nearby devices for the Bluetooth address along with its name. The next step is to select device with whom one wants to connect. The next step is to select a common protocol so as to communicate between them. The most commonly used Bluetooth protocols are RFCOMM and L2CAP. Other than these two there are other protocols such as OBEX, ACL or SCO. The next step for the device performing an outgoing connection is to select the service from the list of services as present in the SDP records of the device at the other end. The port number in which the server is listening is generally hard-coded or predefined. Bluetooth devices uses Service Discovery Protocol (SDP) in which every Bluetooth device maintains an SDP server listening on a well-known port number. When a server application starts up, it registers a description of itself and a port number with the SDP server on the local device. Then, when a remote client application firstconnects to the device, it provides a description of the service it searching for to the SDP server, and the SDP server provides a listing of all services that match. The next step is to establish a socket and to connect to a listening socket on the device which is accepting the connection. After the connection has been established messages can be sent or received depending upon our

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.011.png)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 3.1: Flow Diagram

requirements. In the last step whenever exchange of data has ended the client needs to close the socket connection.![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Bluetooth programming in Android Environment:

Classes Interfaces required:

1. Bluetooth Adapter: Represents the local Bluetooth adapter (Bluetooth radio).
1. Bluetooth Device: Represents a remote Bluetooth device. Use this to request a connection with a remote device through a Bluetooth Socket or query information about the device such as its name, address, class, and bonding state.
1. Bluetooth Socket: Represents the interface for a Bluetooth socket (similar to a TCP Socket).
1. BluetoothServerSocket: Representsanopenserversocketthatlistensforincoming requests (similar to a TCP Server Socket).
1. BluetoothClass: ThegeneralcharacteristicsandcapabilitiesofaBluetoothdevice are described in this class. There are other classes and interfaces as well but is not required for the current work.

Permission required:

Bluetooth permission BLUETOOTH is needed to use the Bluetooth features in your application. This permission is required to perform any Bluetooth communication such as requesting a connection, acceptance of connection and data transfer. BLUETOOTH ADMIN permission is required in order to initiate device discovery or manipulate Bluetooth settings. Most application needs it to discover local Bluetooth devices.

Chapter 4 Detailed![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png) Design

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.012.png)

Figure 4.1: System Architecture

SYSTEM ARCHITECTURE

1. Device A and Device B can act as a Server and client.
1. If Device A Discovers Device B or vice versa then waits for communication.
1. If Device B initiates connections then it becomes client.
1. If Device A initiates connections then it becomes client.
1. Once the connection is established,the user of Device A and user of Device B can transfer Messages.
1. Once, the chatting is done the connection is closed. USE CASE DIAGRAM-1
1. Fill profile: The user (still new user) opens the application for the first time and fillsin his/her personal information.

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.013.jpeg)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 4.2: Use Case Diagram - 1

2. Searchforavailableusers: Theuserwillsearchforanotheruserusingtheapplication that is within his/her device’s Bluetooth adapter range.
2. Start chatting with available users: The user will start chatting and exchanging text messages with other users using the application that with in his/her device’s Bluetooth adapter range.
2. Exchange images: The user can share or exchange images with other users using the application that within in his/her device’s Bluetooth adapter range
2. Save other users’profiles: Other users’profileswill be saved on the user’sdevice USE CASE DIAGRAM-2
1. Fill profile: The user (still new user) opens the application for the first time and fillsin his/her personal information.
1. Accept chatting request: The other user may or may not accept a chatting request from another user using the application that is within his/her device’s Bluetooth adapter range.

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.014.jpeg)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 4.3: Use Case Diagram - 2

3. Chatwithavailableusers: Theuserwillstartchattingandexchangingtextmessages with other users using the application that within in his/her device’s Bluetooth adapter range.
3. Exchange images: The user can share or exchange images with other users using the application that within in his/her device’s Bluetooth adapter range.
3. Save other users’profiles: Other users’profileswill be saved on the user’s device.

SYSTEM ARCHITECTURE

1. If there are two devices one is sender and the other is receiver.
1. To communicate with each other, both the sender and receiver should be trusted.
1. Both the Sender and the receiver gets a unique UID.
1. The Messages exchanged between the sender and receiver is Encrypted.

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.015.png)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 4.4: System Architecture

Chapter 5![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Project SpecificRequirement

The BlueChat application’s specifications are not complex. First the software must be install-able on any device operated by the Android Operating System and support all screen sizes and resolutions to cover a wide range of users and devices. The application then must meet its main purpose or role of exchanging text messages and files among more than one user; this must be achieved or else the software would be useless or unusable. Then the most important criteria is to satisfy the customers’ needing by making the software easy to use, the extra features to be entertaining and usable for them and to implement the application with no errors and out of bugs to avoid continuous crashing with a satisfying performance whether speed or quality.

Assumptions and Dependencies

1. TheandroidoperatingsystemistheoperatingsystemofthedevicewhichtheBlue Chat application would be installed in. An Internet connection is needed in order to load extra functionality.
1. The android operating system is of version 2.0 or more.
1. The android operating system has to have a built-in Bluetooth adapter in order to connect to other Blue Chat application users and exchange text messages and files.
1. The profile of each Blue Chat application user should be filled and saved by the application’s user.

Constraints

1. The application should be installed on more than one device in order to operate or function with each other.
1. The android operating system has to be within the range of Bluetooth adapter of the device in order to scan, discover, exchange or send text messages or files.
1. The android operating system has to enable Bluetooth adapter (turn it on) to start the application.
4. The android operating has to enable Bluetooth adapter to be discover-able to be visible by other application’s users.![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Functional Requirements

1. Anapplicationtoshowprofiletobefilledbytheapplication’suserswhichincludes image view, buttons, text views, edit text views.
1. An application to show available users which will be made of a list of pre-paired Bluetooth Android devices and not paired ones, if the devices are within the range of the Bluetooth device’s adapter
1. An application to show current chat session with other users which will be made of buttons, text view and edit text view.
1. An application to show available directories and files on the device that Blue Chat application would be installed on.

Chapter 6 Implementation![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Implementation phase: Thecodingoftheapplicationwouldbeworkedupontoreachtheneededfunctionalities needed to be implemented in the software. Choosing the appropriate programming language is not difficult. Dart and Java are the best suited programming language for developing Android applications. Java is a well spread language with a lot of support and help documentation and resources. All the needed tools are free and easily installed. These tools are recommended by Google and are free. They include:

- JavaDevelopmentKit(JDK):itisthefoundationoftheAndroidsoftwaredevelopment kit (SDK).
- Androidsoftwaredevelopmentkit(SDK):ProvidesaccesstotheAndroid’slibraries and allowing developing for Android platforms.
- Android Development Tools (ADT): Do all background work for developer, such as creating the filesand structure required for an Android application.
- Eclipseintegrateddevelopmentenvironment(IDE):providestoolsorenvironment for writing Android programs and joins Java, the Android software development kit and the Android Development Tools (ADT) together.

Testing phase:

Testing the application through various conditions and use cases would take place to ensure the software quality. TheAndroidsoftwaredevelopmentkitcontainscohesivetestingframeworkthatfacilitates testing all components of an application and its functionalities using DDMS, AVD Emulator and the real physical device.

Testing phase test cases:

|Test Case|Functionality|
| - | - |
|Fill in profile|Adds a social touch to the application|
|Save Profile|savetheuser’sprofiletobethenexchangedwith other users|
|Scan for users|Determine if there are available BlueChat application users available for chatting|
|Accept chatting request|Accepts incoming chat request and start exchanging text messages|
|Exchange text messages|Send and exchange text messages among application’s users|
|Exchange images|SendandReceivefileamongapplication’susers|
Table 6.1: Test Case![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.016.png)

Chapter 7 Result![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.017.png) ![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.018.png)

Figure 7.1: Sign-up Page Figure 7.2: Sign-in Page

![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.019.png)![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

Figure 7.3: BlueChat App

Chapter 8 Conclusion![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

The goal of this paper is to create an Android application Blue Chat. This application would take the advantage of the wide spread of the Android operating system via varieties of devices. It is concerned with solving some problems of communicating freely, securely, silently and within small range. It is great for making new friends in library or chatting up someone in crowded places. There are areas which can be improved in the future are:

1. Attractive Graphic Features.
1. Extending the BlueChat App to WiFi and Internet.
1. Availing the App at play store.
1. Other mobile Operating system can be used other than android.
1. Adding the feature of group chat.
1. WecanexpectBluetoothchatcommunicationswithmultipledevicesinthefuture.

Chapter 9 References![](Aspose.Words.4d932032-e927-489b-a096-f28d105a820d.007.png)

1. S. Basagni, I. Chlamtac, V.R. Syrotiuk and B.A. Woodward. A Distance Routing EffectAlgorithmforMobility(DREAM),Proceedingsofthefourthannualmobile computing and networking, October 1998.
1. P.Krishna,M.Chatterjee,N.H.VaidyaandD.K.Pradhan. ACluster-basedApproach for Routing in Ad hoc Networks. In proceedings of Second USENIX Symposium on mobile and Location Independent Computing, pp. 1–10, January 1996.
1. S.MurthyandJ.J.Garcia–Luna–Aceves. AnEfficientRoutingProtocolforWire-Less Networks. ACM Mobile Networks and Applications, Special Issue on Routing in Mobile Communication Networks, 1(1):183– 197, October 1996.
1. C.E. Perkins. Ad hoc on-demand distance vector routing, Internet Draft, Internet Engineering Task Force, work in progress, December 1997.
1. C.E. Perkins. Ad hoc on-demand distance vector routing, Internet Draft, Internet Engineering Task Force, work in progress, December 1997.
1. Ayabe,B.S.,Chander,S.S.,Mizikovsky,S.B.(2000). U.S.PatentNo. 6,141,550. Washington, DC: U.S. Patent and Trademark Office.
1. Rittman, D.,Schnapp, M. (2004). U.S. Patent Application No. 10/974,989.
1. Wu, J., Huo, M., Cai, J., Wu, M., Wang, Y. (2012, June). Research on Bluetooth expansion of communication based on android systems. In World Automation Congress (WAC), 2012 (pp. 1-4). IEEE.
SDM College of Engineering and Technology, Dharwad Page 23
