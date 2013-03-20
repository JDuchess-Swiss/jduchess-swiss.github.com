---
layout: post
title: "Soirée Hacking au GenevaJug"
date: 2013-03-20 20:52
author : Julia Mateo
comments: true
categories: 
sharing : true
---

Ce mois-ci le sujet du GenevaJug a été la sécurité. Sébastien Andrivet, cofonder de l'entreprise ADVTOOLS et membre jDuchess, nous a dévoilé les vulnérabilités en sécurité d'un MDM et une application mobile en direct. Voici l'interview que nous lui avons fait la veille du GenevaJug.

_Duchess Swiss : Bonjour Sébastien ! Pourrais-tu te présenter et nous expliquer un peu ton parcours ?_

Je m'appelle Sebastien Andrivet. J'ai 41 ans. J'ai commencé assez tôt à m'intéresser aux ordinateurs. En 1982, j'ai acheté et monté ma première machine (au fer à souder). C'était en kit pour être moins cher. J'ai assez vite détesté le BASIC qui était livré avec et j'ai surtout fait de l'assembleur (des jeux, un désassembler, …). Ensuite, j'ai suivi les différents stades de la microinformatique avec l'Apple IIe, Windows (version 2.0 !), un peu le Macintosh, etc. J'ai utilisé pas mal de langages et j'adorais Smalltalk. Dans les années 90, j'ai trouvé du travail pendant mes études universitaires: dans un laboratoire d'électronique et dans une société éditrice de logiciels. Je faisais principalement du C, du C++ et de l'assembleur sous Windows. J'ai surtout appris à travailler dans une équipe, avec des femmes et des hommes formidables. J'ai aussi découvert Windows NT et Solaris. Puis j'ai quitté la Suisse et je suis allé à Paris. Java est arrivé en 1995-96 à grand renfort de publicité. Je m'y suis intéressé mais, comment dire… je ne voyais pas comment on pouvait sérieusement travailler avec. C'était trop éloigné de ma culture "low-level". J'ai participé à pas mal de startups en France et en Suisse et j'ai oscillé entre le web/http/html/javascript et le C#. Sans oublier Linux, perl, bash, etc. Du monde Linux, c'est Debian, le Debian Manifesto et le Debian Social Contract que je retiens le plus.

J'ai lancé et cofondé ma propre société en 2002, à Genève: ADVTOOLS. Mon idée de départ était de proposer des services d'audits et de pentest, mais aussi des solutions. Hackers + développeurs. On est passé par plein de stades et de péripéties, mais l'idée est toujours la même: faire le lien entre le développement et la sécurité.

{% img left /images/soiree_hacking.png  %}
Coté plus privé, je suis proche de mouvements féminins comme JDuchess et je participe (modestement) à des projets cyberféministes.

_D. S. : Le domaine de la sécurité informatique est si vaste, quel est ton domaine d'expertise (applications web, systèmes d'information en général, mobilité...) ? Considères-tu qu'aujourd'hui on trouve suffisamment de professionnels sur le marché spécialisés en sécurité de domaines si diverses et parfois jeunes (p.e. dispositifs mobiles) ?_

Avec les années, j'ai accumulé pas mal de connaissances. Mais je fais surtout du test d'intrusion, du forensique et de la formation. Le test d'intrusion, c'est surtout des sites web, du réseau, mais ce sont les applications mobiles qui m'intéressent le plus (Android et iOS). Cela me permet de retrouver l'assembleur, le coté hardware qui m'a manqué pendant les années "web". Je suis aussi revenu vers le développement et le C++ en particulier. Il m'arrive même de ressortir le fer à souder !

La sécurité informatique, c'est un peu comme les tests ou l'ergonomie. Certaines entreprises ont conscience qu'elles devraient s'occuper de ces aspects, mais cela coute cher. Les produits d'aujourd'hui sont pleins de bugs, d'absurdités et de problèmes de sécurité. La majorité des entreprises s'en fiche et préfère investir leur argent dans le marketing. Je crois qu'avec ma présentation, vous aurez deux beaux exemples. Alors non, il n'y a pas suffisamment de professionnels et ceux ci ce sont pas toujours qualifiés… comme partout.

_D. S. : Dans le monde des applications mobiles il y a des personnes qui voient un avenir basé sur des applications natives et d'autres qui le voient plutôt sur des applications web. Quel type d'application est la plus vulnérable actuellement à ton avis? Quelles sont les attaques le plus habituelles sur ce type de dispositifs? Quelles techniques utilisez-vous pour les éviter ?_

C'est très dépendant de l'application. Une application publicitaire ou informative n'a en général pas d'impératif de sécurité et le HTML (WebKit) va très bien. Par contre quand une application bancaire utiliser une web view, cela peut poser de sérieux problèmes: des données confidentielles peuvent se retrouver dans le cache, en clair. C'est difficile à maitriser sur Android. Dans une application native, le développeur a un meilleur contrôle de ce qui se passe. Encore faut-il qu'elle ou il ait les connaissances suffisantes pour choisir les bons mécanismes.

Dans les faits, ce sont les applications natives qui aujourd'hui ont le plus de soucis de sécurité. Mais c'est surtout parce qu'elles sont généralement plus complexes, stockent plus de données localement ou communiquent avec des services web mal conçus. Le HTML 5 va probablement réduire cette différence. Je doute que cela soit dans le sens d'une meilleure sécurité.

Les meilleures techniques pour éviter les problèmes de sécurité ? La formation des développeurs et la modélisation de menaces. Mettre les bons moyens, très top dans le projet, là où il faut et pas ailleurs. La sécurité, c'est souvent une histoire de compromis et cela demande de la réflexion. La technologie seule n'est pas suffisante.


_D. S. : Dans la même ligne que la question précédente: quel est, selon ton expérience, l'OS le plus sécurisé dans le monde de la mobilité (iOS, android, blackberry, windows phone) ? Y a-t-il des gros écarts entre les différents systèmes ?_

On peut distinguer plusieurs aspects: la plate-forme (Android, iOS, …), les applications et les stores. Au niveau des plates-formes, Blackberry était devant (il faut encore attendre un peu pour voir si c'est le cas de la nouvelle génération). Ensuite vient iOS et assez loin derrière Android. Au niveau des applications, je constate les mêmes problèmes, les mêmes erreurs sur iOS et Android. Coté Windows Phone, je ne m'y suis pas intéressé assez pour l'instant, donc pas d'avis.

Le danger spécifique d'Android, c'est les malwares et on ne peut pas dire que Google fasse une chasse très efficace. La technologie elle même permet certaines choses plus difficiles sur les autres plates-formes: il est extrêmement facile de modifier et "repackager" une application Android existante et de la publier, avec un cheval de Troy.

{% img left /images/Sebastien.png  %}

_D. S. : Les applications en HTML 5 et javascript sont de plus en plus souvent utilisées pour le développement web. Sont-elles à ton avis plus vulnérables que les technologies "côté serveur" plus anciennes comme JSF, Struts... aux attaques des hackers? Quels sont les principaux avantages/vulnérabilités de ce type de technologie?_

Techniquement, le HTML 5 n'est pas encore un standard et devrait l'être en 2014. Comme toute nouvelle technologie, il faudra attendre un peu pour connaitre les faiblesses et les forces au niveau sécurité. Et chaque navigateur a sa propre interprétation ce qui complique les choses. Mais dans tous les cas, HTML 5 est une technologie coté client. On attaque le navigateur et la personne qui est devant l'écran. Le potentiel de dégât est bien plus important avec une technologie serveur. Là, dans le pire des cas, l'attaquant prend le contrôle du serveur. Dans les faits, les applications sont souvent un mélange de technologies clientes et serveurs.

Certains aspects du HTML 5 me laissent tout de même perplexe: il introduit un "localStorage". Très bien. Mais comment fait-on pour chiffrer les données ? Réponse: ce n'est pas prévu. Aux développeurs de se débrouiller. Le javascript est aussi très pauvre (pour ne pas dire autre chose) au niveau cryptographie.

Des organisations comme OWASP font un classement des principales vulnérabilités web. Le numéro 1, c'est l'injection (SQL, LDAP, …). Le numéro 2, c'est les mauvaises authentifications et la mauvaise gestion des sessions. En trois, c'est le Cross-Site Scripting. On a donc une bonne répartition entre problèmes coté serveur et coté client.

_D. S. : Penses-tu que les développeurs, chefs de projet informatique... sont assez sensibilisés aujourd'hui à la sécurité informatique? Quelle serait la meilleure manière selon toi de sensibiliser les développeur à ce type de problématique : présentations comme au JUG, intervention dans les entreprises ?_

Pour répondre, il faut regarder la ligne "sécurité" dans le budget des projets. C'est souvent zéro, à part les banques qui prennent cela en compte (par la force des choses). 

La sensibilisation, c'est bien mais pour le grand public ou les non-professionnels. Ce qu'il faut pour les développeurs et les chefs de projets, c'est de la formation. Mais il faudra des années et beaucoup de problèmes de sécurité avant que cela ne devienne habituel. La législation va aussi changer bientôt en Europe et en Suisse. Les entreprises vont être de plus en plus responsables des données personnelles qu'elles détiennent et manipulent.

_D. S. : Si tu devais travailler avec une équipe qui n'est pas du tout sensibilisée à la sécurité et que tu avais une complète latitude, comment procéderais-tu? Présentation et recommandations au début du projet, mise en place de tests de sécurité tout au long du développement, audit une fois le développement initial finalisé ?_

L'idéal, c'est de tenir compte des aspects sécurité dès le départ. D'abord, faire une évaluation des menaces très tôt (lors des spécifications): qui est susceptible d'attaquer, avec quels moyens, pour quel bénéfice et avec quelles conséquences. Cela permet de se focaliser sur ce qui est le plus critique. Il y a des méthodes pour faire cette évaluation comme OCTAVE Allegro. La formation des développeuses et des développeurs est un élément clef. Les audits de sécurité se marient mal avec les méthodes Agiles. Ils ont une logique et un rythme bien différent. Le mieux, c'est une bonne collaboration entre développeurs et un référent sécurité. L'idée est, là encore, de mettre les bons moyens sur ce qui est le plus critique. Quand cela n'est pas possible, il faut passer par des audits et des tests d'intrusion. Quand c'est vraiment sensible, il faut faire les deux. Microsoft a développé il y a quelques années une méthodologie "SDL-Agile" qui est intéressante.

_D. S. : Est-ce que la Content Security Policy est aujourd'hui suffisamment solide pour être un référent réel dans le monde du Web? Est-elle référencée dans les entreprises qui travaillent dans le monde de la sécurité, comme p.e. la tienne, ADVTOOLS ?_

Lors de ma présentation, je vais montrer un exemple de XSS (Cross-Site Scripting) et de CSRF (Cross-Site Request Forgery) puis la combinaison des deux. Toute initiative est donc bonne pour contrer ces attaques et le principal but du Content Security Policy est de lutter contre le XSS. Mais c'est encore très jeune. Ce qui compte, c'est qui va l'utiliser, comment et les différences d'interprétation de la norme. Et je constate que la version 1.0 (Novembre 2012) n'est pas encore adoptée qu'une version 1.1 (Mars 2013) est un développement.

De plus, on rencontre parfois des systèmes dont la sécurité … a été désactivée par les développeurs ou les sysadmins.

_D. S. : Suite à quelques épisodes récents de hacking de mots de passe (p.e. celui sur Linkedin où 6.4 millions de mots de passe ont été dévoilées) les générateurs de mots de passe sont devenus un sujet d'actualité. Recommandes-tu leur utilisation ? Penses tu qu'il y ait un vrai risque pour tous ceux qui comme nous utilisent les systèmes sociaux tels que facebook, twitter, Linkedin?_

Un grand nombre de personne utilise le même mot de passe pour différents sites. C'est ça le vrai danger. Et aussi les questions "de sécurité" qui permettent de récupérer son mot de passe. Elles sont souvent stupides. Il est donc préférable d'avoir un mot de passe différent (et aléatoire) pour chaque système et d'utiliser un porte-clef de mots de passe pour les gérer. On en trouve plein, plus ou moins bien, gratuit ou payant (1Password, Keepass, …) Certains protègent mal les mots de passe. Mais c'est quand même mieux que de ne rien avoir et d'utiliser le même mot de passe partout.

Concernant le problème que tu mentionnes (LinkedIn), je trouve qu'il y a une exagération ou on regarde à coté des vrais problèmes. Ce qui a été volé, ce n'est pas des mots de passe mais des haches SHA-1. Même si SHA-1 n'est pas le meilleur choix (SHA-2 est préférable, couplé avec des algorithmes comme PBKDF2), ce n'est pas évident de casser des mots de passe avec juste le SHA-1. Et si l'utilisateur a choisi un mot de passe stupide, ce n'est pas la technologie qui peut l'aider. LinkedIn n'a pas suivi les bonnes pratiques, c'est vrai mais la question que je me pose est: comment l'attaquant a t'il pu récupéré ces haches? Probablement avec une injection SQL. Cela, ça me laisse songeur.

_D. S. : En dehors de la sécurité, est-ce qu'il y a d'autres sujets techniques autour de la technologie java qui t'intéresse spécialement ? Lesquels?_

Dalvik et le problème de la décompilation. J'aimerai aussi bien faire un émulateur pour exécuter du bytecode dex. Mais il y a une arrière pensée du coté sécurité. Et je n'aurais probablement jamais le temps…
Mais en fait quasiment tout m'intéresse. Deployit pourquoi pas. Ce qui m'intéresse avant tout, c'est la démarche intellectuelle et les gens qui inventent ou manipulent les technologies.

Merci beaucoup à Sébastien pour cet entretien. Nous espérons que ses réponses vous aient semblé si intéressants qu'a nous.  A bientôt !
