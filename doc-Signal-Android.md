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



Signal Android
===================

Authors: [Gabriela Brant Alves](https://github.com/gabibrant), [Guilherme Rangel da Silva Moura](https://github.com/guirangel17), [Paulo Henrique de Carvalho](https://github.com/paulo-carvalho)

*Universidade Federal de Minas Gerais - Brazil*


Abstract
---------

Summary
---------
* Table of Contents
* Introduction
* Stakeholders
* Context View
* Development View
* Evolution Perspective
* Conclusion
* References

Table of Contents
------------------



Introduction
------------

Signal is an **encrypted communications app** for secure and private communication with friends. It uses the Internet to send one-to-one and group messages, which can include images and video messages, and make one-to-one voice and video calls. Signal uses standard cellular mobile numbers as identifiers, and uses end-to-end encryption to secure all communications to other Signal users. The applications include mechanisms by which users can independently verify the identity of their messaging correspondents and the integrity of the data channel. In addition, a Chrome app that can link with a Signal client has been released.

This chapter aims to thoroughly describe the architecture of the system, covering general aspects such as its main functionalities and its objective, also covering technical aspects, like its programming language, information about its development team, releases, frameworks, project patterns, among others.

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

<img src="https://lh3.googleusercontent.com/l2UcWONe0L_UWIIuD3zTgwNRaW9n6cmJdofaEV2LD6U4Ngg8YiUs2wUD9EU8xo2ne9w=w300-rw" width="150">

*Figure 01 - Signal Logo*

Stakeholders
------------
Signal is developed by *Open Whisper Systems*, a software organization founded by Moxie Marlinspike in 2013. The organization is funded by a combination of donations and grants, and all of its products are published as free and open-source software.

<img src="https://upload.wikimedia.org/wikipedia/en/4/4f/Open_WhisperSystems_logo.png" width="150">

*Figure 2 - Open Whisper Systems Logo*

Context View
------------


Development View 
----------------


Evolution Perspective
---------------------

![](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Signal_timeline.svg/653px-Signal_timeline.svg.png)



Conclusion
-----------


References
-----------

https://en.wikipedia.org/wiki/Open_Whisper_Systems
https://whispersystems.org/



