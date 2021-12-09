# Time_series_Unsupervised_Learning

Realiser par :
- Mohamed Erifai MAAMIR
- Ahmed Seyfeddine GOUMEIDA
# Objectifs
L’objectif de ce projet est d’utiliser la classification non supervis´ee pour aider `a reconnaˆıtre, `a partir
de donn´ees issues de smartphones, diff´erentes classes d’activit´es physiques de personnes : (1) marcher,
(2) monter les escaliers, (3) descendre les escaliers, (4) s’asseoir, (5) se lever, (6) s’allonger.

# 2 Acquisition des donn´ees:
Pour effectuer la collecte des donn´ees, une personne a suivi un parcours contenant les diff´erentes activit´es list´ees ci-dessus. Lors du parcours, 9 variables ont ´et´e enregistr´ees toutes les 0.02 seconde : 3
acc´el´erations r´eelles (suivant les axes x, y, z), 3 acc´el´erations estim´ees (suivant les axes x, y, z) et 3
vitesses (suivant les axes x, y, z). Les donn´ees utilis´ees sont issues des travaux [1] et [2]. Un extrait video
des exp´eriences r´ealis´ees peut ˆetre visualis´e via le lien http://www.youtube.com/watch?v=XOEN9W05_4A.


# 3 Description des donn´ees
Pour faciliter l’analyse, les donn´ees ont ´et´e d´ecoup´ees en fenˆetres temporelles glissantes de 128 observations (chaque fenˆetre correspond `a un extrait de 2.5 secondes). En effet, il semble plus raisonnable
de d´etecter les activit´es sur des intervalles de temps plutˆot que sur des instants ponctuels.
Ces donn´ees ont ´et´e rang´ees dans 9 tableaux de taille identique (347 × 128) dont chaque ligne
correspond `a une mˆeme fenˆetre temporelle de 128 observations.
accm_x acc´el´eration mesur´ee suivant l’axe x (appel´ee acc´el´eration totale)
accm_y acc´el´eration mesur´ee suivant l’axe y
accm_z acc´el´eration mesur´ee suivant l’axe z
acce_x acc´el´eration estim´ee suivant l’axe x (avec suppression des effets li´es `a la gravit´e)
acce_y acc´el´eration estim´ee suivant l’axe y
acce_z acc´el´eration estim´ee suivant l’axe z
vit_x vitesse suivant l’axe x
vit_y vitesse suivant l’axe y
vit_z vitesse suivant l’axe z
On dispose ´egalement des vraies classes (lab) qui pourront servir `a ´evaluer les m´ethodes propos´ees.
Au total, il y a donc 10 fichiers de donn´ees `a t´el´echarger (http://allousame.free.fr/mlds).


# 4 Travail `a effectuer
R´ealiser une classification automatique des 347 individus (fenˆetres temporelles) pour d´etecter diff´erentes
phases d’activit´e : ex. phases dynamiques (marcher, descendre escalier), phases statiques (s’asseoir,
se lever, s’allonger), phases d’ascension (monter escalier). Pour cela, vous utiliserez au moins trois
m´ethodes ´etudi´ees en cours. Si cela vous semble n´ecessaire, vous pourrez effectuer une transformation
pr´ealable des donn´ees.
Apr`es avoir r´ealis´e la classification, analyser les r´esultats obtenus et les comparer aux vraies classes.
