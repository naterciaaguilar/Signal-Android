Organização esperada para cada capítulo (sistema):
- Descrição do sistema, incluindo principais features, objetivo, linguagem de programação.
- Informações da equipe de desenvolvimento: principais desenvolvedores, funções na equipe (?)
- Breve descrição da evolução do sistema: principais releases e novidades de cada uma.
- Principais frameworks, ferramentas e linguagens usadas no desenvolvimento.
- Documentação da arquitetura, na visão de "desenvolvimento" (modular), isto é, principais módulos e suas responsabilidades, principais padrões de projeto usados, justificativas para adoção dessa arquitetura etc. Se relevante, documentar também visões de processo e física.

Nessa descrição, não ser muito superficial; exemplos de código sempre são úteis em uma descrição arquitetural. Diagramas de sequencia também podem ser interessantes. Evidentemente, não vale copiar (ou meramente traduzir) texto de uma eventual documentação existente do projeto. Mas vale expandir, detalhar, melhorar e tornar mais didática e amigável uma documentação existente.

Procure escrever a documentação imaginando que seu cliente seja um desenvolvedor, que queira contribuir com esse projeto e que precise ter uma primeira visão das principais decisões tomadas durante o projeto do sistema que escolheu para documentar.
Idealmente, não é interessante copiar figuras e tabelas. Mas se for inevitável, citar a fonte original.

Outras informações:
- Tamanho dos capítulos: cerca de 6 mil palavras, sendo que cada figura/tabela conta como 200 palavras.
- Os capítulos podem ser escritos em Português, mas capítulos escritos em Inglês são muito bem vindos.



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
* Context View
* Development View
* Evolution Perspective
* Conclusion
* References

Introduction
------------

Signal Private Messenger is an **encrypted communications app** for secure and private communication with friends. It uses the Internet to send one-to-one and group messages, which can include images and video messages, and make one-to-one voice and video calls. Signal uses standard cellular mobile numbers as identifiers, and uses end-to-end encryption to secure all communications to other Signal users. The applications include mechanisms by which users can independently verify the identity of their messaging correspondents and the integrity of the data channel. In addition, a Chrome app that can link with a Signal client has been released.

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

*Table 01 - Signal app Information*

According to GitTrends.io, the repository was created in the end of 2011 and has a moderated growing rate with more than 7.5k stars, considered one of the 700 most popular repositories in the Github platform.

Stakeholders
------------
Signal is developed by *Open Whisper Systems*, a software organization founded by Moxie Marlinspike in 2013. The organization is funded by a combination of donations and grants, and all of its products are published as free and open-source software.

<img src="https://upload.wikimedia.org/wikipedia/en/4/4f/Open_WhisperSystems_logo.png" width="150">

*Figure 2 - Open Whisper Systems Logo. Source: Github*

Context View
------------


Development View 
----------------

According to GitTrends.io, the Signal Private Messenger has only one user as truck factor: Moxie Marlinspike, responsible for more than 94% of the files in the master branch.






Evolution Perspective
---------------------
Signal Private Messenger is the successor of an encrypted voice calling app called RedPhone and an encrypted texting program called TextSecure. The beta versions of RedPhone and TextSecure were first launched in May 2010 by Whisper Systems, a startup company co-founded by security researcher Moxie Marlinspike and roboticist Stuart Anderson. The company also produced a firewall and tools for encrypting other forms of data. All of these were proprietary enterprise mobile security software and were only available for Android.

In November 2011, Whisper Systems announced that it had been acquired by Twitter. Twitter released TextSecure as free and open-source software under the GPLv3 license in December 2011. RedPhone was also released under the same license in July 2012. Marlinspike later left Twitter and founded Open Whisper Systems as a collaborative Open Source project for the continued development of TextSecure and RedPhone.

In February 2014, Open Whisper Systems introduced the second version of their TextSecure Protocol (now Signal Protocol), which added end-to-end encrypted group chat and instant messaging capabilities to TextSecure. Toward the end of July 2014, Open Whisper Systems announced plans to unify its RedPhone and TextSecure applications as Signal. In November 2015, the TextSecure and RedPhone applications on Android were merged to become Signal for Android.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Signal_timeline.svg/653px-Signal_timeline.svg.png" width="550">

*Figure 3 - Timeline of the development of Signal Private Messenger. Source: Wikipedia*

The graph of inclusions and exclusions in the code, can be observed in the Figure 4 below.
<img src="https://github.com/gabibrant/Signal-Android/blob/master/Capturar2.PNG?raw=true">

The next graph shows the number of contributors over the years, since 2012
<img src="https://github.com/gabibrant/Signal-Android/blob/master/Capturar.PNG?raw=true" >


Number of stars over the years:

<img src="https://github.com/gabibrant/Signal-Android/blob/master/Capturar3.PNG?raw=true" width="500">




Reception
----------
Signal was well recepted by the security community. In October 2014, the Electronic Frontier Foundation (EFF) included Signal in their updated surveillance self-defense guide and afterwards, in November of the same year, Signal received a perfect score of the EFF's messaging scorecard. 

Edward Sowden has endorsed Signal on multiple occasions. In his keynote speech at SXSW in March 2014, he praised Signal's predecessors (TextSecure and RedPhone) for their ease-of-use. During an interview with The New Yorker in October 2014, he recommended using "anything from Moxie Marlinspike and Open Whisper Systems." During a remote appearance at an event hosted by Ryerson University and Canadian Journalists for Free Expression in March 2015, Snowden said that Signal is "very good" and that he knew the security model. Asked about encrypted messaging apps during a Reddit AMA in May 2015, he recommended Signal. In November 2015, Snowden tweeted that he used Signal "every day."

Conclusion
-----------


References
-----------

[1] - Rozanski, Nick, and Eóin Woods. Software systems architecture: working with stakeholders using viewpoints and perspectives. Addison-Wesley, 2012. 

[2] - https://whispersystems.org. Accessed on May 15 2017






