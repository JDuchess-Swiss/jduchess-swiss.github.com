---
layout: post
title: "Entretien avec Nicolas Rémond"
date: 2012-11-26 19:07
comments: true
categories: 
author: Julia Mateo
---
Bonjour à tous !

Pour vous préparer pour le prochain GenevaJug, nous vous offrons en apéritif un entretien avec Nicolas Rémond, committer du projet Gatling. Il nous présentera les avantages de cet outil de test de montée en charge, ce mardi 27 novembre à la salle HEPIA.

{% img left /images/nicolas_remond.jpg 250 250 #2 %}

_Duchess Swiss : Nicolas, pourrais-tu te présenter rapidement et nous expliquer ton parcours ?_

N.R :  J'ai commencé ma carrière à Singapour, puis je suis parti en Californie. Là, je me suis dit que le rêve américain n'était peut-être pas pour moi et maintenant, ça fait 6 ans que je vis à Genève. Je travaille pour la société Secutix, un spécialiste de la billetterie en Europe.

_D.S : Comment as-tu été amené à t'intéresser au projet Gatling et à t'y impliquer ?_

N.R : Pour de gros événements au Stade de France ou pour le Paléo, on a un nombre conséquent de personnes qui viennent en même temps sur notre site pour acheter leur place. C'est quelque chose de compliqué à simuler avec JMeter. J'avais entendu que Stéphane Landelle et Romain Sertelon avaient lancé un nouveau projet open-source. Comme le projet était très jeune, j'ai soumis quelques patchs afin de réussir à exécuter mes tests … et voilà. 

_D.S : Combien de temps consacres-tu en dehors de ton temps de travail à ce projet ?_

N.R : Dur de dire, c'est vraiment très variable et je ne compte pas vraiment. 

{% img right /images/gatling_tool.png  #2 %}

_D.S : Selon toi, quelle serait la "super fonctionnalité" de Gatling ?_

N.R : La performance brute et le fait que les scénarios soient écrits à l'aide d'un DSL. Dur de choisir entre ces deux points. 

_D.S : Pourrais-tu nous expliquer le fonctionnement asynchrone de Gatling? En quoi est-il plus intéressant que le système classique "un thread / un user" ?_

N.R : A partir de 500 users/threads en parallèles, le coût du changement de contextes devient très important et du coup, on perd en précision et la simulation n'est plus vraiment correct. Gatling repose sur deux briques essentielles : Async-Http-Client (Netty) et Akka. C'est grâce à elles qu'il a été possible d'implémenter un système asynchrone. 

_D.S : Quelle est l'avantage d'utiliser Akka ?_

N.R : C'est ce qui nous permet d'avoir une tel montée en charge possible. 

_D.S : Quelles sont les motivations qui ont amené ses créateurs à l'implémenter en Scala plutôt qu'en un autre langage (java...)? Quels en sont les avantages et les inconvénients ?_

N.R : Comme Akka est écrit en Scala, ils leur a paru naturel d'essayer ce langage. De plus, c'est plus simple d'écrire un DSL en Scala qu'en Java. 

_D.S : A quoi ressemble un scénario  Gatling? Pourrais-tu nous en montrer un exemple?_

{% gist 4149815 %}

_D.S : Le fait que les scénarios soient écrit en Scala n'est-il pas pénalisant pour des ingénieurs qualité qui ne seraient pas développeurs ?_

N.R : Pas vraiment. Le DSL est simple à comprendre et on peut écrire beaucoup de chose en ce limitant à ce DSL. 

_D.S : Quelles sont les évolutions possibles de Gatling, les points qui restent à améliorer?_

N.R : Clustering, Websocket..

Merci beaucoup à Nicolas d'avoir répondu à toutes nos questions et pour le reste, n'oubliez pas... soyez nombreux ce Mardi 27 au GenevaJug !
