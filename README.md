# Guide-Bambu-Robot
Guide d'utilisation de la Bambu H2D Pro du laboratoire de robotique.

# Table des matières
* [Station d'impression](#station-dimpression)
    * [Imprimante H2D Pro](#imprimante-h2d-pro)
    * [AMS 2 Pro](#ams-2-pro)
    * [AMS HT](#ams-ht)
    * [Chute et panier de déchets](#chute-et-panier-de-déchet)
    * [Bouton d'arrêt d'urgence](#bouton-darrêt-durgence)
    * [Poste GMC-ROBOT-BAMBU](#poste-gmc-robot-bambu)
* [Procédure d'impression](#procédure-dimpression)
    * [Ouverture et configuration de l'environnemment](#ouverture-et-configuration-de-lenvironnemment)
    * [Changer les filaments](#changer-les-filaments)
    * [Préparer le plateau d'impression](#préparer-le-plateau-dimpression)
    * [Paramètres d'impression importants](#paramètres-dimpression-importants)

# Station d'impression
La station d'impression se trouve à l'entrée du local **_PLT-3702_** et contient les éléments suivants.

1) Imprimante **_Bambu-Labs H2D Pro_**
2) **_AMS 2 Pro_**
3) **_AMS HT_**
4) Chute et panier de déchets
5) Bouton d'arrêt d'urgence
6) Poste **_GMC-ROBOT-BAMBU_**

//TODO : Ajouter une image avec les différents éléments

## Imprimante H2D Pro
L'imprimante H2D Pro se distingue des imprimantes du Fablab sur deux caractéristiques.

1) Tête d'impression à deux buses
2) Volume d'impression plus large (325mm * 320mm * 325mm)

La tête d'impression à deux buses permet d'imprimer plusieurs matériaux et couleurs de manière plus efficace et rapide. Dans la majorité des cas, la buse secondaire sera utilisée pour l'utilisation de matériaux de support. Cependant, d'autres possibilité incluent l'impression de pièces composées de plusieurs types de plastique (TPU+PLA par exemple) ou l'impression de surfaces à plusieurs couleurs.

L'utilisation des deux buses à toutefois un impact sur la surface d'impression. En effet, comme le montre l'image ci-dessous, certaines zones ne sont pas accessibles à l'une ou l'autre des buses, dû à leur positionnement sur la tête d'outils. La surface accessible change donc en fonction de l'utilisation des buses.

> [!TIP]
> Le volume d'impression minimal accessible aux 2 buses est 300mm * 320mm * 320mm

<p align="middle">
    <img src="img/plateau_vide.png" alt="plateau_vide" style="width:600px;"/>
</p>

## AMS 2 Pro

L'AMS (Automatic Material System) est un outils de gestion des filaments d'impression. Le boîtier peut contenir jusqu'à 4 bobines de filaments et permet d'automatiquement alimenter l'une des buses avec l'une des quatres bobines à la fois.

> [!IMPORTANT]
> L'AMS 2 Pro est connecté à la buse de droite de l'imprimante.

En plus de pouvoir maintenir la qualité du plastique en contrôlant l'humidité et la température de l'enclos, l'AMS 2 Pro permet de la changement automatique du filament utilisé par la buse droite lors de l'impression.

> [!NOTE]
> L'AMS 2 Pro permet à la buse droite d'imprimer un maximum de 4 filaments différents de manière automatique. Plus que cela et le filament devra être changé manuellement durant l'impression. Il est aussi important de noter que chaque changement de filament demande une purge de la buse et donc des déchets supplémentaires.

//TODO : Ajout d'un guide de remplacement des bobines

## AMS HT
Tout comme l'AMS 2 Pro, l'AMS HT (High Temperature) permet de la gestion de l'humidité et de la température du filament sur la bobine. Cepedant cet appareil ne permet de contenir qu'une seule bobine. En échange, il permet un séchage plus performant du filament qu'il contient. Cette fonctionnalité est surtout intéressante pour les matériaux plus difficiles à imprimer tels que le TPU et l'ABS.

> [!IMPORTANT]
> L'AMS HT est connecté à la buse de gauche de l'imprimante.

//TODO : Ajout d'un guide de remplacement de la bobine

## Chute et panier de déchet
La chute à déchets sert à récupérer les petits amats de plastiques produits par l'imprimante lors de calibration de la buse ou lors de la purge d'un type de plastique de la buse. Le panier doit être vidé occasionnellement pour éviter qu'il ne déborde.

## Bouton d'arrêt d'urgence
Le bouton d'arrêt d'urgence se trouve à droite de l'imprimante et permet l'arrêt de la machine.

> [!CAUTION]
> Le bouton d'urgence coupe directement l'alimentation de la machine. Il est donc fortement déconseillé d'arrêter une impression de cette manière, car ce dernier sera perdu.

## Poste GMC-ROBOT-BAMBU
Tout comme les imprimantes du Fablab, l'imprimante H2D Pro est uniquement accessible au travers du poste informatique associé. Tout étudiant du laboratoire de robotique peut se connecter au poste. Il est possible de la faire physiquement ou en connexion à distance comme tout autre poste du laboratoire. La connexion a distance sur le poste permet de lancer des impressions à distance.

> [!IMPORTANT]
> Le nom du poste est : **_GMC-ROBOT-BAMBU_**

> [!CAUTION]
> Avant de partir une impression s'assurer qu'un plateau d'impression est bien installé et qu'aucune pièce n'est présente sur le plateau.

Pour vérifier l'état du plateau, il faut soit se déplacer physiquement pour inspecter l'imprimante, ou soit utiliser la caméra interne de l'imprimante accessible dans l'onglet **_Device_** de **_Bambu Studio_**. Il faut se connecter à l'imprimante avant d'activer la caméra.

<p align="middle">
    <img src="img/cam_plateau.gif" alt="cam_plateau" style="width:1280px;"/>
</p>

# Procédure d'impression
La procédure pour partir une impression est la même lorsque physiquement au poste ou en connexion à distance. Cependant, certaines opérations requièrent des opération manuelles sur la machine.

## Ouverture et configuration de l'environnemment
La première étape est de se connecter au poste GMC-ROBOT-BAMBU. Pour avoir accès à vos fichiers d'impression sur ce poste, vous pouvez les placer sur une clé USB (si sur poste physique) ou aller les chercher directement sur votre espace réseau ROBOT. Il est aussi possible de copier des fichier d'un poste à l'autre en connexion à distance.

> [!IMPORTANT]
> Lors de l'ouverture d'une session sur GMC-ROBOT-BAMBU, il est important de **_NE PAS_** lancer Bambu Studio immédiatement. Plutôt, attendre que la console CMD termine de rouler son script et quelle se ferme par elle même. Le script sert à copier des fichier de configuration notamment nécessaire pour se connecter à l'imprimante.

Une fois la console CMD fermée, ouvrir **_Bambu Studio_**. La première étape est de se connecter à l'imprimante pour pouvoir synchroniser Bambu Studio avec notre configuration d'AMS. Dirigez vous vers l'onglet **_Device_** et cliquez sur en haut à gauche sur **_No printer_**. Une liste devrait apparaitre et sous **_My Device_**, cliquez sur l'imprimante **_H2D-PRO-ROBOT(LAN)_**. Après une seconde ou deux, la connexion devrait s'établir. Lorsque la connexion est effectuée, retournez dans l'onglet **_Prepare_** et cliquez sur la bouton **_Sync info_**. Une fois la synchronisation des buses et AMS effectuée. le logiciel va demander de continuer vers la synchronisation des filaments. Si les filaments du projet ne sont pas les mêmes que sur les AMS, le logiciel va vous demander d'associée les filaments réels dans les AMS à ceux du projet.

<p align="middle">
    <img src="img/connect_sync.gif" alt="cam_plateau" style="width:1280px;"/>
</p>

## Changer les filaments
Si les filaments nécessaire à votre impression ne sont pas déjà dans les AMS, alors il faudra les changer. La démarche pour le changement du filament pour chaque AMS se trouve aux sections respectives [AMS 2 Pro](#ams-2-pro) et [AMS HT](#ams-ht).

Vous pouvez placer les filaments dans les emplacements qui vous semblent bons. Cependant, lorsque vous allez cliquer sur **_Slice part_** et que vous sélectionner **_Filament-saving mode_**. le logiciel va vous indiquer comment positionner les filaments dans les AMS pour diminuer les pertes (et accélérer l'impression !). Si on prend l'exemple de la carte de tolérancement ci-dessous, il m'est indiqué de positionner le filament orange dans l'AMS HT (buse de gauche) et le bleu et cyan dans l'AMS 2 Pro (buse de droite). Ce choix est fait, car une fois la base de la pièce terminée (en bleu), la buse de droite peut passer au cyan pour terminer le texte sur le dessus de la pièce qui est en orange et cyan.

<p align="middle">
    <img src="img/filament_placement.png" alt="filament_placement" style="width:600px;"/>
</p>

> [!IMPORTANT]
> Une fois les filaments repositionnés ou changés dans les AMS, il est important de re-synchoniser les informations de l'imprimante avec le logiciel.

## Préparer le plateau d'impression
Avant de commencer, prenons le temps de se familiariser avec l'environnement de prépration du plateau. Nous avons trois sections sur la gauche, soit.

1) Printer
2) Project Filaments
3) Process

La section **_Printer_** devrait être complétée après s'être connecté à l'imprimante et avoir synchronisé les informations de l'imprimante.

La section **_Project Filaments_** sert à indiquer les filaments qui seront utilisés pour l'impression.

> [!NOTE]
> Après la synmchronisation des informations de l'imprimante, le logiciel va automatiquement créer un filament pour chaque filament réel détecté dans les AMS.

<p align="middle">
    <img src="img/printer_filaments.png" alt="printer_filament" style="width:300px;"/>
</p>

Dans l'exemple ci-dessus, on voit que j'ai le matériau de support de l'AMS HT ainsi que les trois couleurs de PLA de mon AMS 2 Pro, pour un total de 4 filaments.

Avant de continuer à la section **_Process_**. placez vos pièces sur le plateau. La barre d'outils se trouvant au dessus du rendu du plateau permet notamment d'ajouter des modèles et de repositionner les pièces. D'autres options incluent la modification légère des modèles ainsi que l'ajout manuel de support et la coloration manuelle.

<p align="middle">
    <img src="img/print_plate.png" alt="print_plate" style="width:600px;"/>
</p>

Dans process, on peut remarquer qu'il y a un slider pouvant alterner entre **_Global_** et **_Objects_**. Dans Global, il est posible de modifier les paramètres globaux de l'impression. C'est généralement dans cette sections que la majorités des utilisateurs vont modifier leurs paramètres. Juste sous la banière, on peut voir un menu déroulant. Celui-ci contient des profils de paramètres pré-enregistrées. À noter que les profils peuvent être ajustés au besoin. Pour ce faire, visiter les sous-menus pour modifier les paramètres voulus. Dans l'image présentée ci-dessous, on a **_Quality_**, **_Strength_**, **_Support_** et **_Others_**.

<p align="middle">
    <img src="img/process_global.png" alt="process_global" style="width:600px;"/>
</p>

> [!NOTE]
> Certain paramètres sont cachés par défaut. Pour avoir accès à tout les paramètres, cliquez sur le slider **_Advanced_** pour afficher les paramètres avancés.

Si on passe aux paramètres des objets, on peut voir notre plateau ainsi que nos modèles. Comme on peut le voir sur l'image ci-dessous, le logiciel a choisi le filament 1 pour imprimer mes 3 pièces, ce qui n'est pas idéal considérant que celui-ci est mon matériel de support. Pour changer le filament d'impression des pièces, soit cliquer droit sur la pièce et allez dans **_Change Filament_**, ou soit cliquez directement sur le numréro du filament à côté du modèle. À noter que cette dernière option prend quelques clics.

<p align="middle">
    <img src="img/process_objects.png" alt="process_objects" style="width:600px;"/>
</p>

Lorsqu'une pièce est sélectionnée, on peut voir que les sous-menus de paramètres d'impression sont affichés plus bas. Ceci permet de modifier les paramètres d'impression pour les différents modèles. Par exemple, je pourrais augmenter le pourcentage de remplaçage à 30% pour une pièce tout en gardant les autres à 15%.

Il est aussi possible de sélectionner le plateau dans la liste pour accéder à des paramètres d'impression comme le type de plateau et la séquence d'impression.

<p align="middle">
    <img src="img/process_objects_plate.png" alt="process_objects_plate" style="width:600px;"/>
</p>

## Paramètres d'impression importants