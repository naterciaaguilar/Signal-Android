Signal Private Messenger for Android
===================

Authors: [Gabriela Brant Alves](https://github.com/gabibrant), [Guilherme Rangel da Silva Moura](https://github.com/guirangel17), [Paulo Henrique de Carvalho](https://github.com/paulo-carvalho)

*Universidade Federal de Minas Gerais - Brazil*

Abstract
---------
This chapter aims to thoroughly describe the architecture of the Signal Private Messenger for Android software, covering general aspects such as its stakeholders, context, development and deployment views, and evolution perspective. The stakeholder analysis section details the types of influencer's who have any impact with the Signal's architecture, like developers, enterprises and final users. The context view explains the interactions between the software and its environment. The development view and deployment views describe the software development process and the runtime environment respectively. And finally, the evolution perspective relates the evolution, variability, performance & scaling the user community acceptance and perspectives of Signal Private Messenger.


<img src="https://lh3.googleusercontent.com/l2UcWONe0L_UWIIuD3zTgwNRaW9n6cmJdofaEV2LD6U4Ngg8YiUs2wUD9EU8xo2ne9w=w300" width="150">

*Figure 01 - Signal Private Messenger for Android Logo. Source: Google Play*

Summary
---------
* Introduction
* Stakeholders
* Context
* Development View
* Evolution Perspective
* Conclusion
* References

Introduction
------------

Adopted by more than 2.5 billion people in the first 20 years of its existence, the Internet permeates through every aspect of our corporate, personal and government lives. The Internet is easily one of the most democratic and disruptive inventions of the last century; it is the epitome of free speech. Only two decades old, the Internet was unchartered legal territory, lacking firm regulatory standards and protection by international law. Further, the unprecedented demand for mobile devices (more people in the world have access to cell phones than toilets, according to the U.N.), further convolutes legal issues when it comes to Internet use and what is private and public information. This is disturbing since 90% of the world’s data was created in the last two years alone. 

The term “Internet revolution” refers to the birth of a new information era that has transformed the way we create and share content. To make our societies, nations, and people more secure and allow for the Internet to drive the benefits of improving every aspect of life that it permeates through today, it is necessary to face the challenge of protecting our data.

In this decade we have a cenary of emerging technologhy that don't always worry about privacy and security. These topics are being more and more discussed through society and governments. Big incidents as data leaks, hackers attacks and government control alert the world to the importance of developing technology that can guarantee privacy and security for its users. In this context, appears an software that address these issues: Signal Private Mesasger.

### What is Signal Private Messenger?

Signal Private Messenger is an **encrypted communications app** for secure and private communication with friends. It uses the Internet to send one-to-one and group messages, which can include images and video messages, and make one-to-one voice and video calls. Signal uses standard cellular mobile numbers as identifiers, and uses end-to-end encryption to secure all communications to other Signal users. The applications include mechanisms by which users can independently verify the identity of their messaging correspondents and the integrity of the data channel. In addition, a Chrome app that can link with a Signal client has been released.

Signal is maintained and run by Open Whisper Systems, a small team of dedicated grant-funded developers, along with a large community of volunteer Open Source contributors that surround the project. All of the source code and files for this project are publicly hosted on GitHub, and anyone can get involved and contribute.

Open Whisper Systems is a non-profit, grant-funded group of free software developers whose mission is to “advance the state of the art for secure communication, while simultaneously making it easy for everyone to use”.

Information | Description
------------ | -------------
Developer | Open Whisper Systems and contributors
Initial release| July 29, 2014
Stable release | Android 4.5.3 (May 1, 2017)
Repository | github.com/WhisperSystems
Development Status | Active
Platform | Android 2.3 or later
Available in | 31 languages
Type | 	Encrypted voice calling, video calling and instant messaging
Website | signal.org

*Table 01 - Signal Private Messenger app Information*

According to GitTrends.io, the repository was created in the end of 2011 and has a moderated growing rate with more than 7.5k stars, considered one of the 700 most popular repositories in the Github platform.

Stakeholders
------------
Stakeholders are the people, groups and/or organizations that have interest or concern in an organization. Stakeholders can affect or be affected by the organization's actions, objectives and policies. Rozanski and Woods discuss 10 types of stakeholders in their book and we are going to describe the most important for our project. 

**Developers**: consists mainly of the team Open Whisper Systems, which is a project that unites a select group of developers driven by the same goal: make private communication simple. Also, they accept volunteer contribution through their GitHub account where the Signal Private Messager is hosted. 

**Users**: Consist of people who wants their message to be cryptographed during a conversation. Any person in the world who worries about privacy and security is eligible to be an user of this app.  

**System administrators**: Signal is administred by the Open Whisper Systems team, which is responsible orient and guide developers to keep building the project. 

**Support staff**:  Consists mainly of a lot of volunteers and core developers. This is done by responding to issues, triaging issues and pull requests, closing bugs as duplicate or filed on the wrong repository, and much more. 

**Testers**: 
<!-- The main users test the system and report bugs to the issue tracker on GitHub. There is no special test team available although the core developers test most pull requests before merging. -->

**Production Engineers**: 
<!-- All tools like GitHub, the Forum, Slack and the build servers are maintained by the GitHub team. They make sure it is running and invest time in updates or setting up new tools. -->

**Assessors**: 
<!-- The core development team of Atom oversees the conformance of the programming standards. They check each pull request with multiple people and also check if it is still in line with the future planning. -->

Signal is developed by *Open Whisper Systems*, a software organization founded by Moxie Marlinspike in 2013. The organization is funded by a combination of donations and grants, and all of its products are published as free and open-source software.

<img src="https://upload.wikimedia.org/wikipedia/en/4/4f/Open_WhisperSystems_logo.png" width="150">

*Figure 2 - Open Whisper Systems Logo. Source: Github*

Context
------------

The context view of a system defines the relationships, dependencies and interactions between the system and its environment. This environment includes the people, systems and external entities with which it interacts. It defines what the system does and what the system does not do.

The Open Whisper Systems community is working to advance the state of the art for secure communication, while simultaneously making it easy for everyone to use. They aim to make mass surveillance of private messaging a thing of the past, and to do that their biggest focus is currently user adoption; we want Signal (or something as secure as Signal) to be as ubiquitous as other messaging applications such as WhatsApp or Facebook Messenger.

It’s important to note that while the Signal protocol encrypts the content of our communications, it does not encrypt metadata – information about information - such as who we contact, when and from where. Unlike content data, which is harder and more expensive to process and retain, metadata is ideally suited to automated analysis by a computer. It can be stored in large quantities and reveals information (such as who you contacted, when and where) that is very difficult – if not impossible – to deny. Using metadata, analysts can map out an individual’s political affiliation, interests, economic background, location and habits, as well as the network of people with whom that individual communicates. This information can be used to create group and individual profiles that are in great demand by an advertising industry desperate to know its audience.

Advertising might seem harmless, but it's important to remember that we are rarely in control of the profiles being created about us. As a result, these profiles may or may not be accurate. And regardless of the accuracy of our profiles, research has shown that profiling can lead to various forms of discrimination. As Open Whisper Systems is not in the data business, we believe Signal is more likely to protect our metadata.  The Signal protocol can be used independently from Google Play Services via LibreSignal, a fork of Signal, which can be installed from F-Droid, a free and open source Android app repository.

<!-- https://securityinabox.org/en/blog/2016-05-23/why-we-still-recommend-signal-over-whatsapp-even-though-they-both-use-end-to-end-encryption/ -->

### Competitors

<!-- https://theintercept.com/2016/06/22/battle-of-the-secure-messaging-apps-how-signal-beats-whatsapp/ -->

The first thing that sets Signal apart from WhatsApp and Allo is that it is open source. The app’s code is freely available for experts to inspect for flaws or back doors in its security. Another thing that makes Signal unique is its business model: There is none. In stark contrast to Facebook and Google, which make their money selling ads, Open Whisper Systems is entirely supported by grants and donations. With no advertising to target, the company intentionally stores as little user data as possible.

Like WhatsApp, all messages sent over Signal are end-to-end encrypted, and Open Whisper Systems doesn’t have the keys to decrypt them. What about message metadata, your phone’s contact list, and cloud backups?

Signal’s privacy policy is short and concise. Unlike WhatsApp, Signal doesn’t store any message metadata. Cryptographer and Open Whisper Systems founder Moxie Marlinspike told me that the closest piece of information to metadata that the Signal server stores is the last time each user connected to the server, and the precision of this information is reduced to the day, rather than the hour, minute, and second.

Signal users must share their contact list with the app in order to find other users — in WhatsApp, this is optional but recommended. But Signal doesn’t directly send your contact list to the server. Instead, it uses what’s known as a cryptographic hash function to obfuscate phone numbers before sending them to the server. (It also truncates the hashed phone numbers, if we’re being precise about things.) The server responds with the contacts that you have in common and then immediately discards the query, according to Marlinspike.

If you back up your phone to your Google or iCloud account, Signal doesn’t include any of your messages in this backup. WhatsApp’s gaping backup issue simply doesn’t exist with Signal, and there’s no risk of accidentally handing over your private messages to any third-party company. In short, if a government demands that Open Whisper Systems hand over the content or metadata of a Signal message or a user’s contact list, it has nothing to hand over. And that government will have just as little luck requesting backups of Signal messages from Google or Apple.

### Downsides
<!-- https://theintercept.com/2016/06/22/battle-of-the-secure-messaging-apps-how-signal-beats-whatsapp/ --> 
Compared to WhatsApp’s 1 billion users, Signal’s user base is minuscule. Marlinspike said that they don’t publish statistics about how many users they have, but Android’s Google Play store reports that Signal has been downloaded between 1 and 5 million times. The iPhone App Store does not publish this data.

This means that if you install the Signal app, chances are you’ll have to convince your friends, family, and colleagues to install it as well before you can benefit from Signal’s top-grade privacy protection. If you install WhatsApp, chances are a lot of your contacts are already using it, and you can begin having encrypted conversations with minimal effort.

Signal also has fewer features and gets improved at a slower pace than its corporate competitors. For example, an early version of Signal Desktop has been available since the end of 2015, but it’s only available for Android users — iPhone support has not yet been developed, and it’s unclear when it will be finished. WhatsApp has a desktop version that works regardless of the type of phone you use.


Development View 
----------------
According to Rozanski and Woods, the development view concerns "code structure and dependencies, build and configuration management of deliverables, systemwide design constraints, and system-wide standards to ensure technical integrity". 

According to GitTrends.io, the Signal Private Messenger has only one user as truck factor (truck factor is the minimal number of developers that have to quit before a project is incapacitated. It reveals the concentration of knowledge in individual developers): Moxie Marlinspike (moxie0), responsible for more than 94% of the files in the master branch.

### Implementation details

<!--https://www.bestvpn.com/blog/30980/signal-private-messenger-review/ -->
<!-- Text secure com ibageeens [falta adicionar] : https://whispersystems.org/blog/private-groups/ --> 

Signal encrypts and decrypts all messages client-side (i.e. on the user’s phone before transmission and upon receipt), so they cannot be intercepted in transit. Messages can also be stored encrypted on the phone.

Each text is encrypted using perfect forward secrecy (using an ephemeral Curve25519 key), so that if any keys are compromised, the attacker will only have access to one small part of the conversation. The text body itself is encrypted using 256-bit AES in CTR mode, with Curve25519 Diffie-Hellman handshake/key protection, and SHA256 hash authentication (for more information on these terms please see here.)

Signal VoIP conversations are likewise encrypted client-side, with all voice communications between the app and servers encrypted using TLS, while the contents of communications are encrypted using 128-bit AES-CBC, with SHA1 hash authentication. This is not as strong as the encryption used by Signal for text messaging, probably due the fact that encrypting and decrypting data uses processing power, so stronger encryption would negatively impact the quality of calls. For most purposes this level of encryption should be more than sufficient, but if very high levels of privacy are required then you should probably stick to text messaging.

### Features

**Group messaging**
It is possible to name the group and add multiple people. 

**Signal on desktop**
Signal is availble on desktop version as well. But it's importante to notice that if users are having highly sensitive conversations and may have malicious software on their personal computer, encryption won’t protect messages. For example, if users are infected with malicious software designed to log keystrokes or send screenshots to a remote attacker.

**Attachments**
It is possible to send media files and also sennd GIFs here.

**Make messages disappear**
It is possible to delete a specific message. Because Signal stores all of your messages locally and not on a remote server, users only delete the message on their personal device while it may be availbe to its partner.

**Clear History Logs**
Even when phone is locked, someone with physical access can still read the message and sender name on your lock screen. But it's possible to avoid that with Signal, making sure messages aren’t readable on your lock screen.

**Session verification**
On most messengers, there is no way to know that your message isn’t intercepted by a third party. With Signal, it's possible to verify that the current conversation is secure for both messages and calls. 

### BitHub Rewards
Since Signal is a Open Source software, they have a method to reward people who volunteer to contribute to the project though BitHub, which is a service that will automatically pay a percentage of Bitcoin funds for every submission to a GitHub repository. It is possible to find all details [here](https://github.com/WhisperSystems/Signal-Android/wiki/BitHub-Rewards).

### Code Guidelines
Moxie Marlinspike has provided standards for developing flexible, durable, and sustainable code style where contributors of the project must adhere to. This code guide can be found [here](https://github.com/WhisperSystems/Signal-Android/wiki/Code-Style-Guidelines). 


Evolution Perspective
---------------------
Signal Private Messenger is the successor of an encrypted voice calling app called RedPhone and an encrypted texting program called TextSecure. The beta versions of RedPhone and TextSecure were first launched in May 2010 by Whisper Systems, a startup company co-founded by security researcher Moxie Marlinspike and roboticist Stuart Anderson. The company also produced a firewall and tools for encrypting other forms of data. All of these were proprietary enterprise mobile security software and were only available for Android.

In November 2011, Whisper Systems announced that it had been acquired by Twitter. Twitter released TextSecure as free and open-source software under the GPLv3 license in December 2011. RedPhone was also released under the same license in July 2012. Marlinspike later left Twitter and founded Open Whisper Systems as a collaborative Open Source project for the continued development of TextSecure and RedPhone.

In February 2014, Open Whisper Systems introduced the second version of their TextSecure Protocol (now Signal Protocol), which added end-to-end encrypted group chat and instant messaging capabilities to TextSecure. Toward the end of July 2014, Open Whisper Systems announced plans to unify its RedPhone and TextSecure applications as Signal. In November 2015, the TextSecure and RedPhone applications on Android were merged to become Signal for Android.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Signal_timeline.svg/653px-Signal_timeline.svg.png" width="550">

*Figure 3 - Timeline of the development of Signal Private Messenger. Source: Wikipedia*

The graph of inclusions and exclusions in the code, can be observed in the Figure 4 below.
<img src="https://github.com/gabibrant/Signal-Android/blob/master/Capturar2.PNG?raw=true">

*Figure 4 - Code frequency (lines of code added and deleted) throughout the years of development. Source: Github*

The next graph shows the number of contributors over the years, since 2012
<img src="https://github.com/gabibrant/Signal-Android/blob/master/Capturar.PNG?raw=true" >

*Figure 5 - Contributions based on commits over the years for Singal Private Messenger, since 2012. Source: Github*

Number of stars over the years:

<img src="https://github.com/gabibrant/Signal-Android/blob/master/Capturar3.PNG?raw=true" width="500">

*Figure 6 - Number of stars and unstars over the years, since November 2011, and its predction for next year. Source: GitTrends.io*

Most of the bug fixes contributions come from casual users, i.e., people who is not the main developer from any file.
According to instructions listed on Signal's README, they use GitHub itself for bug tracking. It is instructed to search the existing issues for your bug and create a new one if the issue is not yet tracked.

In order to keep Signal Private Messenger updated and maintain its user-friendly interface, they track string translation activity using Transifex. By May 2017, they have translated 95 languages and 25 of them are completely translated.

### Versions

<!-- Referências
 https://www.apk4fun.com/history/56556/ 
 https://github.com/WhisperSystems/Signal-Android/milestones?state=closed -->

Signal Private Messenger App Version History and Changelog:

Latest Version: Signal Private Messenger 4.5.3 APK (Updated: May 2, 2017)
Changes in 4.5.3:
* Support for sending arbitrary file types.
* Support for jumbomoji!
* Bug fixes and performance improvements.
Changes in 4.3.2:
* Fix for crash in some settings screens on devices running KitKat and below.
Changes in 4.3.1:
* Eliminate echo on more devices.
* Include preference for message font size.
* Improve video playback.
* Bug fixes and performance improvements.

Old Version: Signal Private Messenger 4.3.2 APK (Updated: April 19, 2017)

Changes in 4.3.2:
* Fix for crash in some settings screens on devices running KitKat and below.

Changes in 4.3.1:
* Eliminate echo on more devices.
* Include preference for message font size.
* Improve video playback.
* Bug fixes and performance improvements.

Changes in 4.2.5:
* Eliminate echo for some devices.
* Bug fixes and performance improvements.

Old Version: Signal Private Messenger 4.3.1 APK (Updated: April 18, 2017)

Changes in 4.3.1:
* Eliminate echo on more devices.
* Include preference for message font size.
* Improve video playback.
* Bug fixes and performance improvements.

Changes in 4.2.5:
* Eliminate echo for some devices.
* Bug fixes and performance improvements.

Changes in 4.2.4:
* Screen is now disabled when device is raised to ear during voice note playback.
* Raised the GIF size limit to 25MB.
* Bug fixes and performance improvements.

Old Version: Signal Private Messenger 4.2.4 APK (Updated: April 5, 2017)

Old Version: Signal Private Messenger 4.1.0 APK (Updated: April 4, 2017)

Old Version: Signal Private Messenger 4.0.1 APK (Updated: March 24, 2017)

Old Version: Signal Private Messenger 4.0.0 APK (Updated: March 22, 2017)

Old Version: Signal Private Messenger 3.31.4 APK (Updated: March 13, 2017)

Old Version: Signal Private Messenger 3.30.4 APK (Updated: February 28, 2017)

Old Version: Signal Private Messenger 3.29.6 APK (Updated: February 14, 2017)

Old Version: Signal Private Messenger 3.28.4 APK (Updated: February 1, 2017)

Old Version: Signal Private Messenger 3.27.1 APK (Updated: January 19, 2017)

Old Version: Signal Private Messenger 3.26.2 APK (Updated: January 10, 2017)

Old Version: Signal Private Messenger 3.25.4 APK (Updated: December 30, 2016)

Old Version: Signal Private Messenger 3.25.3 APK (Updated: December 21, 2016)

Old Version: Signal Private Messenger 3.24.1 APK (Updated: December 7, 2016)

Old Version: Signal Private Messenger 3.23.0 APK (Updated: November 28, 2016)

Old Version: Signal Private Messenger 3.22.2 APK (Updated: November 17, 2016)

Old Version: Signal Private Messenger 3.21.3 APK (Updated: November 1, 2016)

Old Version: Signal Private Messenger 3.20.4 APK (Updated: October 11, 2016)

Old Version: Signal Private Messenger 3.19.1 APK (Updated: September 20, 2016)

Old Version: Signal Private Messenger 3.19.0 APK (Updated: September 17, 2016)

Old Version: Signal Private Messenger 3.17.0 APK (Updated: August 23, 2016)

Old Version: Signal Private Messenger 3.16.1 APK (Updated: August 8, 2016)

Old Version: Signal Private Messenger 3.16.0 APK (Updated: May 29, 2016)

Old Version: Signal Private Messenger 3.15.2 APK (Updated: March 31, 2016)

Old Version: Signal Private Messenger 3.13.1 APK (Updated: March 7, 2016)

Old Version: Signal Private Messenger 3.12.0 APK (Updated: February 23, 2016)

Old Version: Signal Private Messenger 3.11.1 APK (Updated: February 17, 2016)

Old Version: Signal Private Messenger 3.10.0 APK (Updated: February 3, 2016)

Old Version: Signal Private Messenger 3.9.1 APK (Updated: January 6, 2016)

Old Version: Signal Private Messenger 3.8.1 APK (Updated: December 23, 2015)

Old Version: Signal Private Messenger 3.7.2 APK (Updated: December 9, 2015)

Old Version: Signal Private Messenger 3.6.1 APK (Updated: December 1, 2015)

Old Version: Signal Private Messenger 3.5.2 APK (Updated: November 25, 2015)

Old Version: Signal Private Messenger 3.4.2 APK (Updated: November 18, 2015)

Old Version: Signal Private Messenger 3.3.3 APK (Updated: November 13, 2015)

Old Version: Signal Private Messenger 3.3.2 APK (Updated: November 12, 2015)

Old Version: Signal Private Messenger 3.1.1 APK (Updated: November 2, 2015)

Old Version: Signal Private Messenger 2.28.1 APK (Updated: September 29, 2015)

Old Version: Signal Private Messenger 2.27.2 APK (Updated: September 24, 2015)

Old Version: Signal Private Messenger 2.26.5 APK (Updated: September 15, 2015)

Old Version: Signal Private Messenger 2.26.4 APK (Updated: September 9, 2015)

Old Version: Signal Private Messenger 2.25.3 APK (Updated: August 13, 2015)

Old Version: Signal Private Messenger 2.24.1 APK (Updated: August 4, 2015)

Old Version: Signal Private Messenger 2.23.3 APK (Updated: July 24, 2015)

Old Version: Signal Private Messenger 2.23.2 APK (Updated: July 23, 2015)

Old Version: Signal Private Messenger 2.22.2 APK (Updated: July 16, 2015)

Old Version: Signal Private Messenger 2.21.0 APK (Updated: July 7, 2015)


Reception
----------
Signal Private Messenger was well recepted by the security community. In October 2014, the Electronic Frontier Foundation (EFF) included Signal in their updated surveillance self-defense guide and afterwards, in November of the same year, Signal received a perfect score of the EFF's messaging scorecard. 

Edward Sowden has endorsed Signal on multiple occasions. In his keynote speech at SXSW in March 2014, he praised Signal's predecessors (TextSecure and RedPhone) for their ease-of-use. During an interview with The New Yorker in October 2014, he recommended using "anything from Moxie Marlinspike and Open Whisper Systems." During a remote appearance at an event hosted by Ryerson University and Canadian Journalists for Free Expression in March 2015, Snowden said that Signal is "very good" and that he knew the security model. Asked about encrypted messaging apps during a Reddit AMA in May 2015, he recommended Signal. In November 2015, Snowden tweeted that he used Signal "every day."

Signal is incorporated as the default messenger app in CyanogenMod, the very popular alternative OS or Android phones, and the TextSecure protocol on which Signal is based has also been adopted by the world’s most popular instant messaging app, WhatsApp

Conclusion
-----------
Even without taking its privacy and security advantages into consideration, Signal makes an excellent SMS/MMS client that does a good job of replacing the stock one that came with your phone. As far as security is concerned, it is probably the best option currently available for keeping your text and voice conversations private.


References
-----------

[1] - Rozanski, Nick, and Eóin Woods. Software systems architecture: working with stakeholders using viewpoints and perspectives. Addison-Wesley, 2012. 

[2] - https://whispersystems.org. Accessed on May 15 2017

[3] - http://gittrends.io/#/repos/WhisperSystems/Signal-Android. Accessed on May 15 2017






