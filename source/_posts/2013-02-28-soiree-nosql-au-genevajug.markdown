---
layout: post
title: "Soirée NoSQL au GenevaJug. Interview à Katia Aresti"
date: 2013-02-28 22:13
sharing: true
comments: true
author: Julia Mateo
categories: 
---

Bonjour à tous ! Nous sommes de retour suite au GenevaJug du mois de Février qui a été dédié au monde du NoSql. Dans cette soirée nous avons eu une introduction aux bases de données non relationnelles de la main de Cyril Lapinte (développeur agile chez Serial SA). En suite Benoit Perroud, développeur au sein de l'équipe de BigData chez Verisign, nous a présentée Cassandra. Katia Aresti lui a suivi pour parler sur MongoDB et sa mise en place et application chez un de ses clients, Mappy. Nous avons eu l'opportunité de lui faire une interview.

_Duchess swiss : Salut Katia ! Pourrais-tu te présenter et nous raconter un peu ton parcours ?_

Je fais mes études à Bilbao d'ingénieur en informatique, puis je suis partie à Madrid avec l'idée de partir ensuite à l'étranger. J'ai commencé à travailler chez Sopra Group. Après 3 ans à Madrid, puis 2 ans à Paris, la découverte de la communauté Paris JUG via Duchess m'a fait rejoindre Xebia. Après deux ans chez Xebia, je suis passée freelance en septembre 2012. Professionnellement j'ai surtout travaillé autour des technologies Java, mais récemment je m'attaque aussi au PHP pour des sites web plus petits et/ou personnels. De plus, depuis 3 ans je suis pro-agile, et je pratique sur mes missions SCRUM, Kanban et XP.

_Duchess swiss : Quand est-ce que tu as commencé à travailler avec MongoDB et comment es-tu devenue référent ?_

C'était sur mon ancienne mission, avec Xebia. J'ai eu l'énorme chance de tomber sur le projet UrbanDive - le nouveau Mappy. La bas, nous avons développé le système de recherche et le contenu des Point d'intérêt (POI). Nous avons choisi Mongo comme base de données, et cela a perduré jusqu'à aujourd'hui.

{% img left /images/katia_aresti.png  %}

_Duchess Swiss : Quelles sont pour toi les avantages que MongoDB présente par rapport à d'autres bases de données non relationnelles et orientées à documents (comme couchDB ou ravenDB)?_ 

Je ne peux pas trop m'aventurer à en parler côté performance ou technique, ni même au niveau de la prise en main car je n'ai pas encore eu l'occasion (ni le temps) de travailler avec d'autres bases de données du type document. Je peux parler par contre de la communauté MongoDB qui est énorme, et qui touche tous les langages de programmation (on le voit lors des rencontres au Paris MongoDB User Group). Et je peux aussi parler du plaisir que l'on prend en tant que développeur quand on découvre la base de données, et aussi de la road-map et 10Gen qui sont vraiment très fortement investis dans leur produit pour satisfaire la communauté. 

_D.S : Quelle est la meilleure façon de monter en compétence sur MongoDB? Dans quel cas peut-on l'exploiter au mieux?_


La meilleure façon est de participer à un workshop sur le sujet. Il y a des workshops gratuits online disponibles sur le web de 10Gen (sur https://education.10gen.com/). Sinon il y a aussi des soirées
organisées par la communauté Java (JUGs, Duchess...)



_D.S : Quels sont les problèmes que l'on peut rencontrer lorsque l'on utilise cette nouvelle façon de stocker des données? comment peut-on les surmonter? La synchronisation des données est-elle toujours fiable, qu'est-ce qui se passe si un serveur tombe?_

Mongo offre la possibilité de créer un environnement replica-set. En plus c'est possible de rajouter la fonctionnalité « journaling ».
Si un serveur tombe dans un replica-set, Mongo choisira le nouveau master de façon automatique. L’existence d’un bon system de monitoring devient nécessaire afin de 
détecter ce type de problèmes en plus d’analyser tout ce qui se surveille normalement en production

{% img right /images/katia_aresti_jug.jpg 324 432 #3 %}

_D.S : Comment se passe les backups? Y-a-t-il des contraintes?_

Mongo fournit une grande quantité d'outils pour faire dumps, restores, exports... etc. Je dirais que les mêmes possibilités qui existent pour les bases de données relationnelles sont aussi disponibles sur Mongo.

_D.S : Quelles sont les nouvelles features que MongoDB va présenter à court terme ?_

Lors de la conférence à San Francisco, plusieurs fonctionnalités ont été évoquées. L'un de points critiques de MongoDB est la mise en production, et surtout, son suivi et la maintenance lorsque la base de données monte en charge. Donc, il y a des fonctionnalités qui vont arriver pour améliorer la vie des Ops, côté replication, sharding, index, et le monitoring. Un service de monitoring est déjà en place, et ils continuent à y travailler pour l'améliorer encore.
D'autre part il y aura l'amélioration des APIs, notamment celui du driver Java. Aujourd’hui le driver java reste très verbeux et il s'agit du driver le plus utilisé maintenant. Côté fonctionnalité, le souhait est de permettre la recherche full-text intégré à la base de donnes. L'idée serait d'intégrer les fonctionnalités le plus courantes au driver. 

_D.S : Nous avons su que tu que tu as participé à la conférence MongoSV 2012 à Santa Clara le dernier mois de décembre. Comment ça a été cette expérience ? Quel sujet as-tu abordé ?_

J'étais ravie d'y aller, 10Gen nous a accueilli de façon extraordinaire. Cela a été génial d'y être. La veille de la conférence, nous avons eu une journée entre les "masters" de MongoDB venus de partout dans le monde, et beaucoup travaillent dans des startups innovantes, donc cela a été très enrichissant d'échanger avec eux. Il n'y a pas beaucoup de javaistes, mais beaucoup de python, scala et ruby. Nous avons fait un open-space et nous avons abordé beaucoup des sujet différents. Le lendemain, lors de la conférence, je n'ai pas pu suivre grand ‘chose pendant la matinée car j'avais mon quicky avant la pause déjeuner et je ne pouvais pas penser à autre chose avec le stress du moment :) Sinon, l'après-midi j'ai assisté aux speech d'autres masters, que j'aimerais qui viennent parler à Paris (de masters de Londres).

_D.S : En dehors de Mongo, est-ce qu'il y a un sujet technique qui t'intéressent particulièrement en ce moment ?_

Je suis très intéressée par le développement côté client (HTML5, CSS3) et par la nouvelle génération des frameworks javascript côté client et côté serveur. En dehors de la technologie, je suis très intéressée par les pratiques de développement agile et par son évangélisation chez mes clients.

_D.S : Tu fais partie de la team jduchess paris depuis Avril 2010. Qu'est-ce que duchess t'a apporté pendant ce temps ? Et, réciproquement, quels sont, selon toi, le points principaux que jDuchess offre par rapport à d'autres organisations autour de java comme les jugs?_

Déjà, grâce à Duchess j'ai découvert l'univers des communautés, et des SSII plus petites et plus axées sur les valeurs que je considère nécessaires pour bien faire notre travail, comme Xebia. Grâce aux ex-collègues de Sopra, j'ai rencontré Duchess. A cette époque, connaître Mathilde, Ellène, Audrey, Laure et Claude a été une révélation pour moi. Je me sentais disons un peu "seule". Par moment, toujours entourée de mecs, tu peux ressentir des difficultés et des doutes. Une majorité des femmes, au bout d'une certaine expérience, quittent la filière technique pour devenir "chef de projet" ou business analystes, voire product owner. Ces rencontres et Duchess France m'ont aidé pour évoluer, et pour me rassurer sur mes choix. Duchess étant un Jug plus petit, offre un espace pour créer des liens entre hommes et femmes, et offre un cadre de vie pour partager ses connaissances à l'importe qui. Enfin, le fait que Duchess ait été lancé par des femmes permet de faire évoluer l'image du monde de l'IT, encore très stéréotypé.

_D.S : Katia, j'ai lu que tu étais en FreeLance depuis septembre 2012. Qu'est-ce qui t'a motivé à passer le cap?_

Ce qui m'a poussé à devenir freelance c’est surtout le fait de pouvoir gérer mon temps différemment et la liberté que ceci suppose.

Merci beaucoup, Katia ! On espère te revoir bientôt sur Genève pour présenter un workshop Duchess les mains sur le code ! ;)


