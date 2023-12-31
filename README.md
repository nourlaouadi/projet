# projet SE:
* Les Questions :
  
Q1 : Quelles sont les structures de données à utiliser ?
Pour représenter les données dans le programme, des structures de données spécifiques sont utilisées. Les matrices B, C et A, nécessaires pour effectuer la multiplication matricielle, sont stockées sous forme de tableaux bidimensionnels, En ce qui concerne la communication entre les fils, un tampon circulaire est employé. Ce tampon est implémenté sous la forme d'un tableau de structures.

Q2 : Comment allez-vous protéger l'accès à ces données ?
Pour garantir l'intégrité des données partagées entre les threads, l'accès aux sections critiques est sécurisé par l'utilisation de verrous, également connus sous le nom de mutex. Ces verrous permettent d'assurer une exécution atomique des opérations dans les sections où les threads accèdent et modifient les données partagées, telles que le tampon circulaire T. Les threads doivent adopter le verrou avant d'accéder aux données partagées et le relâcher une fois les opérations terminées.

Q3 : Quels sont les risques ?
il existe plusieurs points à considérer. Premièrement, des blocages peuvent se produire si les verrous ne sont pas acquis et relâchés correctement, entraînant un blocage des threads. Deuxièmement, des conditions de concurrence peuvent survenir si la synchronisation entre les threads n'est pas correctement gérée, entraînant des résultats incorrects. Enfin, des problèmes de performance peuvent apparaître si la taille du tampon n'est pas optimale ou si la répartition des tâches entre les threads est inadéquate, impactant ainsi les performances globales du programme.

