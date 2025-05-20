Colonnes à conserver pour les prédictions
Pour un modèle de prédiction précis, je recommanderais de conserver ces colonnes:

Informations de base:

Date (utile pour capturer les tendances saisonnières)
HomeTeam et AwayTeam (essentielles)
Season (pour capturer l'effet de la saison)


Statistiques de match importantes:

H Shots & A Shots (indicateurs offensifs importants)
H SOT & A SOT (précision offensive - très prédictives)
H Corners & A Corners (reflètent la pression offensive)
H Fouls & A Fouls (style de jeu et intensité)
H Yellow, A Yellow, H Red, A Red (discipline, peut affecter les performances)


Variables à exclure pour la prédiction:

FTH Goals, FTA Goals et FT Result (ce sont nos variables cibles)
HTH Goals, HTA Goals et HT Result (résultats de mi-temps si on prédit le résultat final)
Display_Order (purement administratif)
Referee (pourrait introduire un biais sauf si vous créez des features sur l'historique de l'arbitre)



Colonnes à normaliser/standardiser
Pour la standardisation/normalisation:

Colonnes à standardiser (pour mettre toutes les variables à la même échelle):

H Shots & A Shots
H SOT & A SOT
H Corners & A Corners
H Fouls & A Fouls


Colonnes à encoder (transformation catégorielle en numérique):

HomeTeam et AwayTeam (one-hot encoding ou target encoding)
Season (encoding ordinal puisqu'il y a une progression temporelle)
League (si vous incluez plusieurs ligues, one-hot encoding)


Traitement spécial:

Date: à transformer en features temporelles (jour de la semaine, mois, jours depuis le début de la saison)
H Yellow, A Yellow, H Red, A Red: peuvent être gardées telles quelles car elles ont déjà une échelle limitée et comparable



Je vous recommande fortement de créer également des features dérivées comme:

Forme récente (résultats des 5 derniers matchs)
Historique des confrontations directes
Moyenne glissante des statistiques sur les derniers matchs
Écarts de classement entre les équipes

Ces variables dérivées seront probablement plus prédictives que les statistiques brutes d'un seul match.