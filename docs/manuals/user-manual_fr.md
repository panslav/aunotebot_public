# Manuel utilisateur

## 0.39.0.1

L’export ICS est conservé ; le lien Google utilise le point d’entrée testé sur mobile et ordinateur. Confirmez et enregistrez l’événement dans le calendrier. La recherche locale pondère les mots-clés sans IA ni frais supplémentaires. Les listes actives excluent les tâches terminées sans supprimer les fiches conservées. Les erreurs proposent Retour et Accueil. Les résultats de liens en attente utilisent la langue d’interface actuellement enregistrée ; le titre et la description disponibles servent de solution de repli, mais les pages restreintes peuvent rester inaccessibles. Les lenteurs de chargement des photos restent à l’étude ; les photos ne sont ni converties en fichiers ni recompressées.

## 0.39.0.0

La recherche locale, la pagination et le retour aux résultats sont gratuits. Répondre avec l’IA demande explicitement une réponse payante, sans prix sur le bouton. Les réponses inchangées sont réutilisées dans la session.

GPT-Transcribe reconnaît la parole. Une étape de mise en forme conserve les tours de dialogue seulement avec des indices explicites ; elle n’identifie pas les personnes par leur voix. Résumé, titre et métadonnées réutilisent une analyse commune.

Avant une analyse vidéo en plusieurs étapes, le bot réserve le coût total. Si le résultat complet ne peut pas être fourni, la réservation est remboursée ; une vidéo sans son exploitable peut être analysée visuellement sans facturer la transcription échouée.

## Version 0.38.0.0 — rappels et fusion fiables

Les dates comme « 28.10 » sont reconnues séparément du résumé ; un rappel facultatif est conservé en UTC. Les tâches dont la date et l’heure futures sont reconnues reçoivent un rappel. Une date seule utilise l’heure enregistrée du récapitulatif quotidien des tâches ; à défaut, choisissez une heure. Les anciens éléments ne sont pas reprogrammés automatiquement.

Les suggestions de fusion privilégient les thèmes communs, puis la pertinence du texte, sans éléments archivés. L’identifiant et le titre de la destination sont conservés et les textes complets sont concaténés sans réécriture par l’IA. Les pièces jointes distinctes et les rappels programmés sont conservés. L’original est archivé pour récupération ; ses commentaires y restent.

Les titres des résumés et du texte extrait sont en gras ; les sections d’analyse strictement identiques sont omises. Le titre de la note courte n’affiche plus la limite de mots. Les traits de soulignement des identifiants sont préservés. La proposition de partage présente une seule action pour ouvrir l’élément, sans commandes de retour en double. Les confirmations de création n’ajoutent plus d’espacement invisible ; l’appareil gère la mise en page des notifications natives.

Les montants des bonus restent inchangés. Les nouvelles tentatives de notification persistent sans recréditer le solde. Google OAuth reste reporté. L’acceptation d’une pièce jointe par Telegram ne confirme pas son téléchargement sur l’appareil ; les lenteurs des images restent à l’étude.

## Version 0.37.0.3 — bonus et messages système

Une journée locale active rapporte 0,50 point ; les trois jours suivants sans activité admissible, 0,30, 0,15 et 0,05. Au quatrième jour, les bonus s’arrêtent avec une notification. Créer une note ou un commentaire de plus de 100 caractères visibles, partager ou attribuer une note à une autre personne constitue une activité ; consulter, modifier ou recevoir une copie ne compte pas. Après un bonus d’inactivité, l’activité complète seulement le total journalier à 0,50. Aucun rattrapage ni recalcul historique. Le traitement intervient pendant la première heure locale ; une panne peut retarder ou empêcher la notification du jour.

Paramètres → Masquer les messages système : 5, 10 ou 30 secondes, 1 minute ou Jamais ; 30 secondes par défaut. Cela concerne les nouveaux avis temporaires, pas le nettoyage de navigation ni la synchronisation technique du clavier. Les boutons des brouillons en attente restent jusqu’à une action. Google OAuth est reporté ; ICS et les liens Google restent à 0,10 point, sans prix sur le bouton.

## Corrections de la version 0.37.0.3

Les confirmations de création utilisent des espaces ordinaires, sans retour à la ligne forcé. Telegram et le système d’exploitation déterminent l’affichage final de la notification.

Dans la proposition de partage d’une note, Partager et Ouvrir la note figurent sur la même ligne ; Retour reste séparé et ferme uniquement la proposition. Commentaires et Calendrier partagent une ligne lorsque le calendrier est disponible.

Le brouillon conserve le lien d’origine avant la fin du résumé. L’enregistrement d’un résumé de secours conserve sa source. Les nouveaux débits d’enrichissement IA et reçus d’export gardent la référence de la note pour les liens de l’historique ; les anciennes références manquantes ne sont ni devinées ni réécrites.

Une expression telle que «сегодня в 19» contient une heure, pas seulement une date. Un lien de visioconférence pris en charge est exporté comme lieu dans ICS et Google. La convention régionale configurable CET/CEST utilise Europe/Madrid avec l’heure d’été, et non un décalage fixe UTC+01:00. Plusieurs lieux distincts nécessitent une précision.

## Version 0.37.0.1

Les boutons du calendrier répondent désormais correctement, sans prix dans leur libellé. Si l’envoi ICS n’est pas confirmé, le bot fournit un lien Google Agenda distinct dans le cadre du même export à 0,10 point. Les adresses comme `av. Aragon nº4-bis` conservent le numéro du bâtiment ; téléphone et e-mail sont exclus de la recherche. Aucune connexion de compte Google n’est nécessaire.

## Version 0.37.0.0

L’export calendrier apparaît dans la fiche si une date ou une heure est détectée, et reste toujours disponible dans Plus. Le libellé du bouton ne contient pas de prix ; l’export coûte 0,10 point. Un appui envoie directement un fichier d’événement .ics, sans aperçu intermédiaire dans le bot, ainsi qu’un lien Google Agenda de secours. Ouvrez le fichier dans votre calendrier et confirmez l’importation ; Telegram ou le système peut demander de choisir une application. L’ouverture automatique du calendrier par défaut n’est garantie ni sur iOS, ni sur Android, ni sur ordinateur.

Si Telegram ne confirme pas l’envoi de l’ICS, le bot envoie un message distinct avec le lien Google Agenda prérempli. La confirmation correspond à un identifiant de message et de fichier renvoyé par Telegram, pas au téléchargement ou à l’importation sur l’appareil. Le lien ne nécessite pas de connexion OAuth au bot.

Une date seule crée un événement sur toute la journée ; une heure seule utilise aujourd’hui dans votre fuseau enregistré, même si l’heure est passée. Une date et une heure utilisent le moment indiqué. La durée par défaut est de 60 minutes. Le titre commence par l’icône de note/tâche et reprend le titre de la fiche ; la description contient un lien vers celle-ci dans le bot, sans son texte privé. Si la date manque, est invalide ou ambiguë, Plus demande une seule date/heure de début ; Retour annule, les fichiers et transferts créent un nouveau brouillon.

Un seul envoi réussi du même événement est facturé par utilisateur. Le récupérer à nouveau est gratuit, même après un redémarrage du bot ; les échecs d’envoi sont remboursés. Changer le titre, la date ou l’heure produit un nouvel événement. Le bot ne confirme pas l’enregistrement dans le calendrier. Réimporter peut créer des doublons ; les modifications ultérieures ne sont pas synchronisées. Le fichier disparaît du chat à la fermeture des pièces jointes de la fiche. Aucun compte calendrier ni analyse IA payante n’est requis.

La lecture audio conserve les liens de l’auteur et de la source, y compris après conversion d’une note en tâche ou inversement. Les liens sans schéma, comme Tambur.pub, s’ouvrent en HTTPS au lieu de s’afficher en Markdown.

La durée de l’audio généré est mesurée et conservée à la réouverture de l’entrée. Relancer la lecture du même texte avec la même voix et le même modèle réutilise le fichier enregistré, sans nouvelle facturation de génération IA ni pièce jointe en double. Modifier le texte lu crée une nouvelle version. Les anciens fichiers audio d’origine indéterminée ne sont pas supprimés automatiquement.

## Version 0.36.0.1

Les pièces jointes et messages transférés créent un nouveau brouillon au lieu d’être interprétés comme une date de rappel, même si le récapitulatif du soir attend une réponse. Une suggestion de rappel n’active pas la saisie d’une date ; ouvrez explicitement Rappel pour en saisir une.

Les actions Note avec IA et Tâche avec IA sont toujours affichées dans les brouillons nouveaux ou rouverts, y compris ceux contenant uniquement du texte. L’accès à l’IA et le solde sont vérifiés au clic ; l’enregistrement normal reste disponible.

Dans la suggestion d’envoyer ou d’attribuer une entrée aux personnes mentionnées, Retour ferme uniquement la suggestion et conserve l’écran, la page et les pièces jointes précédents. Revenir à l’entrée reste une action distincte.

## Version 0.36.0.0

Le bonus quotidien est crédité à la première action admissible, pas à minuit. Un nouvel élément ou commentaire, y compris à la clôture d’une tâche, doit dépasser 100 caractères visibles ; partager ou attribuer à autrui n’exige pas de longueur minimale. Pas de second bonus le même jour local ni de recalcul des anciens soldes. Les récompenses d’accueil et de partage restent distinctes.

La recherche affiche tous les résultats par pertinence avec pagination standard. Retour depuis un élément rétablit la requête et la page précédentes sans facturer une nouvelle synthèse IA.

Le son AAC est encapsulé localement en M4A sans réencodage avant transcription. La pièce jointe d’origine reste intacte. Un brouillon sans texte avec un fichier Markdown affiche une description claire et le nombre de documents.

Les boutons d’un brouillon en attente restent sur sa carte principale jusqu’à utilisation, même après l’ouverture d’un autre brouillon. Enregistrer, fermer ou supprimer un élément retire les copies des pièces jointes affichées par le bot, y compris en cours d’envoi ; les messages d’origine sont conservés.

Les sources de sites ne sont pas répétées et les liens du texte restent intacts. Chaque segment transféré affiche « auteur : message », avec un lien vers le message d’origine si Telegram le fournit ; les transferts privés ou masqués peuvent ne pas l’exposer. Les liens des paragraphes numérotés sont préservés. Les anciens brouillons ne sont pas réécrits en masse.

## Version 0.35.0.9

La définition d’un rappel ramène à un seul écran de tâches, sans listes en double. Fermer un élément retire ses pièces jointes affichées du chat ; rouvrir le même élément réutilise les fichiers déjà affichés.

Les identifiants des résultats de recherche renvoient à l’élément correspondant et chaque ligne reprend l’icône de son en-tête.

Les messages transférés regroupés conservent l’expéditeur de chaque segment. L’IA produit une synthèse unique du texte, de l’OCR et du contenu des pièces jointes compatibles, y compris les informations visuelles. Les paragraphes et les listes sont préservés.

Telegram gère le téléchargement sur votre appareil ; l’aperçu peut rester flou pendant celui-ci. Les fichiers incompatibles ou trop volumineux ne peuvent pas être entièrement analysés.

Ce guide explique comment utiliser AUNotebot depuis Telegram.

Note de maintenance (clarification de la limite audio v1.0) : pour l'audio téléversé via Telegram, ce bot applique la limite de téléchargement de Telegram Bot API.

## 1. Démarrage
1. Ouvrez la conversation avec le bot.
2. Envoyez `/start`.
3. `/start` recharge et réapplique toujours vos paramètres enregistrés, surtout la langue et la visibilité du menu inférieur.
4. Vous verrez :
   - message de bienvenue :
     - `Bienvenue dans le bot Telenota.`
     -
     - `📝🗣️🎥🌃➡️🧠✅`
     - `Prenez des notes là où votre vie se déroule.`
     - `Capturez idées, pensées et tâches, et n'oubliez plus rien.`
     -
     - `1️⃣ Écrivez-moi, envoyez un message vocal, une image, une note vidéo ou une vidéo classique.`
     - `2️⃣ Je l'enregistrerai et créerai une note ou une tâche. Mon IA l'analysera et produira un bref résumé.`
     - `3️⃣ Gardez-la comme note ou transformez-la en tâche pour la partager ou définir un rappel.`
     -
     - `⚖️ En utilisant le bot, vous acceptez les Conditions d'utilisation (cliquez sur Plus -> Mentions légales).`
     - `❓ Cliquez sur Plus -> Aide pour ouvrir le guide utilisateur.`
     - `✉️ Idées ou retours : @telenota_chat.`
   - la version actuelle sur la dernière ligne du message de bienvenue
   - compteurs et raccourcis inline :
     - ligne 1 : `Mes notes`, `Tâches`
     - ligne 2 : `Brouillons`, `Rappels`
     - ligne 3 : `Rechercher`, `Plus`
     - ligne 5 : bouton facultatif `Suivre les actualités de Telenota` dans la langue actuelle de l’interface
   - menu de commandes Telegram (menu hamburger) avec raccourcis
5. Ouvrir `/start` ou n'importe quelle liste masque les anciennes listes/écrans d'accueil visibles afin que seul l'écran demandé reste visible.
6. Les listes ouvertes depuis les raccourcis affichent un titre compact au-dessus des boutons au lieu d'un message vide de remplacement.
7. Si une URL de canal d’actualités est configurée pour votre langue d’interface, `/start` affiche aussi un bouton facultatif avec les nouveautés, conseils et exemples Telenota dans cette langue. Le suivi du canal reste optionnel et n’affecte pas l’usage du bot.

Documents publics des conditions :
- [Dépôt des documents légaux](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Ouvrez `Plus -> Mentions légales` pour accéder à la page des conditions dans la langue actuelle de votre interface.
- Politiques d'utilisation d'OpenAI (base des fonctions IA) :
  - https://openai.com/en-GB/policies/usage-policies/
  - les fonctions IA peuvent être limitées ou désactivées si une demande enfreint ces politiques.
- Note de suivi administratif :
  - le bot stocke des entrées d'audit d'actions (`moment`, `action_type`) et des liens de partage (`source`, `target`, `action_type`) pour les opérations et l'analyse de graphe.

Manuels publics :
- [Dépôt des manuels publics](https://github.com/panslav/aunotebot_public/tree/main/docs/manuals)
- Ouvrez `Plus -> Aide` pour accéder au manuel dans la langue actuelle de votre interface.

## 2. Langue
1. Au premier `/start`, le bot essaie de détecter votre langue à partir de la locale Telegram.
2. La langue de repli par défaut est l'anglais.
3. Pour changer de langue manuellement :
   - ouvrez `Plus -> Paramètres -> Langue`
   - choisissez l'une des langues, dans cet ordre : `English`, `Español`, `Français`, `Português`, `Русский`, `Українська`, `简体中文`, `العربية`
4. Toutes les principales étiquettes et tous les boutons de l'interface sont traduits après la sélection.

## 2a. Points IA et Telegram Stars
L’export calendrier coûte `0,10 point` pour l’envoi réussi du fichier ou du lien de secours, une fois par utilisateur et événement inchangé. Un échec ICS suivi du lien Google constitue une seule opération. Si aucun n’est envoyé, la réservation est remboursée. Réexporter est gratuit, même après un redémarrage. Le bouton n’affiche pas le prix.

1. Les actions alimentées par l'IA utilisent votre solde de points.
2. Modèle de facturation par défaut :
   - `1 point = 1 Telegram Star`
   - `10 points gratuits` une seule fois lors de votre première utilisation du bot
   - `0,50 point` par journée locale active ; puis `0,30`, `0,15`, `0,05` pendant trois jours inactifs. Au quatrième jour, arrêt jusqu’à une nouvelle activité admissible. Consultation, modifications et copies reçues ne comptent pas.
   - pas de récompense automatique en points pour la création de notes/tâches
   - `1.5 point / minute` pour le texte vers voix
   - `1.0 point / minute` pour l'analyse audio
   - `1.5 point / minute` pour convertir en texte l'audio/vidéo déjà joint à un élément enregistré
   - `0.5 point` par OCR d'image
   - Résumé et étiquettes : `0.20 point` ; traduction : `0.50 point` ; résumé audio, analyse des images vidéo et résumé PDF : `1 point` par étape. Les titres sont gratuits ; analyse de lien : `0.05 point`.
3. La durée est mesurée dans le fichier réel avec ffprobe avant la réservation des points, sans estimation par taille ni durée fictive.
   - Exemple : `125 secondes` coûtent `3.13 points`.
   - Le montant est arrondi à la hausse au `0.01 point` le plus proche.
   - Si la durée ne peut pas être mesurée, l’opération s’arrête sans facturation.
   - Si votre solde est insuffisant, la transcription ne démarre pas et votre note/tâche existante reste inchangée.
4. Ouvrez `Plus -> Points` pour :
   - voir votre solde actuel
   - voir vos 5 dernières opérations de points
   - ouvrir l'historique complet des points
   - voir les tarifs IA actuels
   - recharger avec Telegram Stars
5. Vous pouvez partager votre propre numéro de téléphone dans `Plus -> Paramètres -> Contacts -> Partager mon téléphone`.
6. `Plus -> Paramètres` contient aussi une zone dangereuse pour supprimer les données de votre compte AUNotebot.
7. Supprimer toutes les données efface définitivement vos notes, tâches, brouillons, rappels, contacts, paramètres, historique de points et enregistrements de compte liés appartenant au bot.
8. Lorsque vous achetez des points dans le bot, les recharges Telegram Stars sont facturées directement en `XTR`.
9. Si votre solde est insuffisant :
   - la fonctionnalité IA est bloquée pour cette action
   - le bot affiche une notification
   - les fonctionnalités sans IA continuent de fonctionner
10. Actions IA payantes typiques :
   - résumés et tags
   - génération de réponses Recall/Find
   - traduction
   - interprétation libre de rappels, fuseau horaire et heures de digest
   - transcription et texte vers voix

## 3. Créer une note
1. Envoyez du texte simple au bot.
2. Le bot affiche un aperçu de brouillon.
3. Appuyez sur `📝 Enregistrer comme note`.
4. La liste des notes s'ouvre.

## 4. Créer une tâche
Option A :
1. Envoyez du texte.
2. Dans l'aperçu du brouillon, appuyez sur `🟧 Enregistrer comme tâche`.
3. La liste des tâches s'ouvre.

Option B :
1. Ouvrez n'importe quelle note.
2. Appuyez sur `⬛ Créer une tâche`.

## 5. Transférer des messages
1. Transférez un ou plusieurs messages au bot.
2. Le bot fusionne les messages transférés proches dans le temps en un seul brouillon.
   - Le délai de fusion par défaut est de `30` secondes.
   - Vous pouvez le modifier dans `Plus -> Paramètres -> Temps de fusion des messages`.
3. Si vous ajoutez du texte simple juste après le transfert, le bot l'ajoute ainsi :
   - `💬 Transféré avec le commentaire :`
   - `<votre texte>`
   avant la ligne de source/pied de page.
4. Dans la vue note/tâche, les sources publiques d’utilisateurs Telegram sont affichées comme liens cliquables `@handle` au lieu d’URL brutes `https://t.me/...`, une seule ligne vide est conservée avant le pied final `Enregistré via Telenota (...)`, et ce pied inclut aussi un lien cliquable `votre message` vers le message exact du bot à l’origine de l’élément quand Telegram l’expose encore.
5. Si un message transféré contient un ou plusieurs liens web, le bot utilise d'abord les métadonnées d'aperçu disponibles pour chaque page et, lorsqu'elles sont absentes, tente un fallback déterministe et sûr du titre à partir des métadonnées de la page (`og:title`, `twitter:title` ou HTML `<title>`).
   - Les liens Google Maps redirigés peuvent être résolus vers le titre final de la page lorsque la page de destination l'expose.
   - Si aucun titre sûr ne peut être extrait, le bot conserve le fallback existant avec lien source au lieu d'afficher une fausse source ou une erreur brute.
   - Dans les transferts fusionnés, la mise à jour en arrière-plan du résumé de lien remplace uniquement le bloc de lien en attente et conserve les autres messages transférés.
6. Le formatage Telegram du texte transféré est conservé dans les notes/tâches enregistrées lorsque Telegram l'expose au bot :
   - gras, italique de type Markdown, liens et blocs de citation sont rendus dans la vue finale de l'élément.
   - les liens conservent leur URL cible complète, y compris les paramètres de requête comme `?g_st=...` ou `&foo=...`.
7. Si aucun commentaire séparé n'est ajouté après le transfert, le bot enregistre le marqueur explicite `Transféré sans commentaires` ; si un commentaire est envoyé juste après le transfert, seul ce commentaire est enregistré dans le bloc de commentaire.
8. Les médias Telegram joints au message transféré sont enregistrés avec le brouillon et affichés avec la note/tâche enregistrée. Si plusieurs pièces jointes ont un lien source enregistré, la vue de l'élément les affiche comme des liens compacts séparés par des virgules et groupés par type de média :
   - les photos/images restent jointes lorsque Telegram les fournit comme médias téléchargeables par le bot.
   - les images d'aperçu de lien générées seulement par les clients Telegram peuvent ne pas être téléchargeables via Bot API ; envoyez/transférez la photo réelle si vous avez besoin d'une conservation garantie de l'image.
   - si Telegram expose une vidéo ou une animation transférée avec une photo d’aperçu côté client, le bot conserve la vraie vidéo ou animation et supprime l’image d’aperçu dupliquée.
   - si Telegram signale seulement un média transféré trop volumineux pendant l'enregistrement IA, le bot enregistre le brouillon original sans analyse IA du média au lieu d'afficher une erreur générique.
9. Optionnel : envoyez un texte contenant uniquement des hashtags (exemple : `#work #idea`) avant d'enregistrer pour ajouter des tags.
10. Ouvrez le brouillon et utilisez :
   - ligne 1 : `📝 Enregistrer comme note`, `🟧 Enregistrer comme tâche`
   - ligne supplémentaire facultative : `⏰ Enregistrer comme rappel` apparaît quand le texte du brouillon contient une date/heure reconnaissable
   - actions finales : `✏️ Modifier`, `❌ Annuler`
   - les actions IA sont toujours affichées, y compris pour les brouillons contenant uniquement du texte ; pour les images, l’élément conserve d’abord le contenu d’origine, puis affiche le résumé IA et le texte OCR en préservant les listes numérotées et à puces lisibles
   - le résumé IA est formaté en trois courtes parties : introduction, partie principale et conclusion
   - `Modifier` n’affiche que le texte propre de l’élément à copier manuellement ; la source, le type localisé et le pied du bot restent dans le modèle
11. Après l'appui sur enregistrer, le bot affiche immédiatement un état d'enregistrement, puis un message de succès avec quatre raccourcis inline : ouvrir l'élément créé et Notes sur la première ligne, puis Accueil et Brouillons sur la deuxième ligne.
12. Si tous les brouillons sont consommés/enregistrés, ouvrir `Brouillons` vous ramène au sélecteur Accueil.

Les nouveaux brouillons reçoivent un titre concis généré par IA dans la langue d’interface choisie. L’analyse IA des vidéos décrit d’abord l’image, y compris les dates lisibles, puis ajoute la transcription audio lorsqu’elle est disponible.

## 6. Voix et vidéo
1. Envoyez un message vocal, un fichier audio (y compris `.m4a` lorsque Telegram l'envoie comme audio ou document audio), une vidéo ou une note vidéo.
2. Pour les messages vocaux et les fichiers audio, le bot affiche immédiatement un message de traitement lorsque l'analyse démarre.
3. Pour les vidéos normales, notes vidéo et documents vidéo, le bot enregistre d'abord le média comme brouillon ; l'analyse IA démarre seulement quand vous choisissez `Note avec IA` ou `Tâche avec IA`.
4. Quand l'analyse IA démarre, le bot transcrit et prépare le texte du brouillon/de l'élément. Les transcriptions audio/vidéo incluent des horodatages à la fin de chaque paragraphe lorsque les données de timing sont disponibles.
   - Si la transcription échoue, le bot affiche `Réessayer` ; appuyez dessus pour relancer le même fichier Telegram sans le téléverser à nouveau.
5. Appuyez sur `📝 Enregistrer comme note` ou `🟧 Enregistrer comme tâche`.
   - Après l'enregistrement, le bot affiche un message de succès avec quatre raccourcis inline : ouvrir l'élément créé et la liste correspondante sur la première ligne, puis Accueil et Brouillons sur la deuxième ligne.
6. Si le brouillon contient une date/heure reconnaissable, vous pouvez appuyer sur `⏰ Enregistrer comme rappel`.
   - Cela enregistre le brouillon comme tâche et planifie immédiatement le rappel.
7. Si un brouillon combine plusieurs messages transférés/légendés ou une analyse IA de média, la note/tâche enregistrée sépare les sections par des séparateurs horizontaux visibles. Le formatage du texte original et du contenu généré est conservé lorsque Telegram l'expose au bot.
8. Les messages vocaux, fichiers audio et vidéos Telegram de plus de `20 MB` sont rejetés avant traitement, car Telegram Bot API ne permet pas à ce bot de télécharger des envois plus volumineux dans ce runtime.
9. Si votre enregistrement ou vidéo dépasse `20 MB`, divisez-le ou compressez-le manuellement et envoyez les parties plus petites une par une.
10. Les messages d’erreur temporaires sont supprimés automatiquement lorsque vous envoyez le message suivant, appuyez sur le prochain bouton du bot ou après 30 secondes.
11. Les échecs récupérables de Telegram, de l’IA ou de délai d’attente affichent un code stable, par exemple `E-TIMEOUT-001`. Transférez ce message à `@telenota_chat` lorsque vous demandez de l’aide ; le code n’expose pas votre contenu.

## 7. Images et captures d'écran
1. Envoyez ou transférez une image/capture d'écran.
2. Le bot exécute l'OCR et résume le texte/contenu visible important.
3. Un brouillon est créé ; enregistrez-le ensuite comme note ou tâche.
4. Si vous envoyez un document PDF textuel et choisissez une action d’enregistrement avec IA, le bot conserve le contenu d’origine du brouillon, ajoute le texte extrait du PDF, puis ajoute un bref résumé IA de `300` mots maximum dans la langue d’interface choisie.
5. Le texte extrait est conservé sous forme de paragraphes lisibles, et le résumé IA est rendu en trois courtes parties : introduction, partie principale et conclusion.
6. Les PDF scannés ou composés uniquement d’images peuvent échouer pendant l’analyse IA tant que la prise en charge OCR pour PDF n’a pas été ajoutée.
7. Si vous enregistrez un PDF sans IA, le brouillon/l’élément conserve une simple ligne `PDF <nom du fichier>`. Si vous ouvrez ensuite l’élément enregistré et appuyez sur `Analyse IA`, le même flux de résumé PDF est lancé.
8. Telegram Bot API ne transmet pas aux bots le fichier média d’une Story transférée. Le bot enregistre sa référence et vous demande d’envoyer ensuite une capture d’écran, une photo ou une vidéo téléchargée ; ce fichier est joint au même brouillon.
9. Lors de l’analyse IA d’une image, l’élément enregistré affiche d’abord le résumé IA, puis le texte OCR reconnu. Les listes numérotées et à puces de l’image conservent leur format.

## 8. Parcourir notes et tâches
- Utilisez le menu de commandes Telegram (hamburger) :
  - `🏠 Démarrer`
  - `🔎 Rechercher`
  - `📝 Mes notes`
  - `🗂️ Brouillons`
  - `🟧 Tâches`
  - `⏰ Rappels`
  - `📚 Plus`
- Si le menu inférieur est activé (`Plus -> Paramètres -> Afficher le menu inférieur`) :
  - ligne 1 : `📝 Mes notes` + nouvelle ligne + `(N)`, `⏰ Rappels` + nouvelle ligne + `(N)`, `🟧 Tâches` + nouvelle ligne + `(N)`
  - ligne 2 : `🗂️ Brouillons` + nouvelle ligne + `(N)`, `🔎 Rechercher`, `📚 Plus`
- Les en-têtes de liste comme `📝 Mes notes` et `🗂️ Brouillons` s’affichent sur une seule ligne visible, sans espacement invisible.
- Lorsque vous ouvrez une tâche depuis la page 2+ puis la marquez comme faite, la supprimez, la convertissez ou définissez un rappel, le bot revient à la même page de liste de tâches lorsqu'il réaffiche la liste.
  - lorsqu'il est activé, le menu inférieur reste visible jusqu'à ce que l'utilisateur le désactive dans les paramètres
  - ces boutons ouvrent les mêmes écrans que les actions du menu hamburger.
- Vous pouvez aussi utiliser les compteurs inline de l'écran de démarrage :
  - ligne 1 : `📝 Notes (N)`, `🟧 Tâches (N)`
  - ligne 2 : `🗂️ Brouillons (N)`, `⏰ Rappels (N)`
  - ligne 3 : `🔎 Rechercher`, `📚 Plus`

## 9. Rechercher (recherche fusionnée + Recall)
1. Appuyez sur `🔎 Rechercher` (écran de démarrage ou menu hamburger, ou `/find`).
2. Le bot entre en mode Rechercher interactif et affiche :
   - `🔎 Demandez-moi n'importe quoi ! Mon cerveau IA trouvera et résumera les informations pour vous.`
3. Envoyez n'importe quelle requête/question en format libre.
4. Le bot fait les deux :
   - classement déterministe sur les notes et tâches, y compris les éléments archivés
   - correspondance sensible aux flexions pour les variantes de mots de la requête (par exemple les terminaisons)
   - résumé IA sur les résultats pertinents
5. Format de réponse lorsque des éléments sont trouvés :
   - texte de résumé
   - `Voici les éléments les plus pertinents pour votre demande :`
   - boutons des éléments pertinents, les plus pertinents d'abord
   - `⬅️ Retour`
6. Si votre requête de recherche est un ID exact d'élément (par exemple `219` ou `#219`) et que cet élément existe, il est épinglé comme résultat #1.
7. Pour quitter le mode Rechercher, appuyez sur `⬅️ Retour`.
8. `⬅️ Retour` vous ramène à l'écran où vous étiez avant le mode Rechercher.
9. Si le résumé IA facultatif est indisponible, les correspondances locales et les boutons de résultat restent disponibles avec un résumé neutre de remplacement.

## 9a. Suggestions de rappel
1. Si une note ou tâche nouvellement créée contient une expression probable de date/heure, le bot propose automatiquement un rappel.
2. Si seule une date est détectée, le bot propose `Matin`, `Midi`, `Soir`, ainsi que `Définir un rappel` et `Ignorer`.
3. Tant que cet écran est ouvert, vous pouvez saisir directement votre propre date/heure ; il n'y a plus de bouton séparé de saisie manuelle.
4. Si seule une heure est détectée, le bot suppose la date du jour sauf si vous saisissez une autre date.
5. Si l'élément est encore une note normale et que vous choisissez `Définir un rappel`, le bot la convertit d'abord en tâche, puis planifie le rappel.
6. Après la création du rappel, le bot confirme l'heure dans votre langue.
7. Si vous ouvrez la configuration du rappel depuis un callback de média, le bot utilise une voie d'édition sûre et affiche quand même l'invite de rappel.

## 10. Actions sur les notes et tâches

### Actions de note
- `✏️ Modifier`
- `⬛ Tâche`
- `❌ Supprimer`
- `📚 Plus`
- `⬅️ Retour`
- `📚 Plus` ouvre :
  - ligne 1 : `🤖 Analyser avec l'IA`, `🔊 Créer une voix`
  - ligne 2 : `🔀 Fusionner`, `📤 Partager`
  - ligne 3 : `📌 Épingler` / `📌 Désépingler`, `🏷️ Tags`
  - ligne 4 : `⬅️ Retour`

### Actions de tâche
- `✏️ Modifier`
- `✅ Fait` ou `🔄 Refaire`
- `⏰ Rappel`
- `🔁 Convertir en note`
- `❌ Supprimer`
- `📚 Plus`
- `⬅️ Retour`
- `📚 Plus` ouvre :
  - ligne 1 : `🤖 Analyser avec l'IA`, `🔊 Créer une voix`
  - ligne 2 : `🔀 Fusionner`, `👥 Assigner` ou `👥 Réassigner`
  - ligne 3 : `📌 Épingler` / `📌 Désépingler`, `🏷️ Tags`
  - ligne 4 : `⬅️ Retour`

### Assignation de tâche avec Contacts
1. Ouvrez une tâche.
2. Appuyez sur `👥 Assigner` ou `👥 Réassigner`.
3. Le bot affiche :
   - vos contacts enregistrés sous forme de boutons
   - option de saisie manuelle (`@handle` ou téléphone)
4. Si vous tapez un nouveau `@handle`/téléphone valide, il est automatiquement enregistré dans vos Contacts.
5. Si le destinataire a déjà démarré le bot, l'assignation est envoyée et la tâche est liée à cet utilisateur.
6. Si le destinataire n'a pas encore démarré le bot et que vous avez sélectionné un `@handle`, le bot crée un message d'invitation séparé avec le lien caché sous « Telenota ». Envoyez ce message au destinataire : lorsqu'il démarre le bot avec ce lien, la tâche est livrée automatiquement si son handle Telegram correspond. Si un autre compte ouvre le lien, le bot vous demande d'approuver ou de refuser l'accès.
7. Vous pouvez utiliser `↩️ Désassigner` depuis le sélecteur d'assignation pour supprimer l'assignation actuelle.

### Partage de note avec Contacts
1. Ouvrez une note normale.
2. Appuyez sur `📤 Partager`.
3. Le bot affiche :
   - vos contacts enregistrés sous forme de boutons
   - option de saisie manuelle (`@handle` ou téléphone)
4. Si vous tapez un nouveau `@handle`/téléphone valide, il est automatiquement enregistré dans vos Contacts.
5. Si le destinataire a déjà démarré le bot, la note est partagée et livrée dans son chat, pièces jointes incluses.
6. Si le destinataire n'a pas encore démarré le bot et que vous avez sélectionné un `@handle`, le bot crée un message d’invitation séparé avec le lien caché sous « Telenota ». Envoyez-le au destinataire : lorsqu'il démarre le bot avec ce lien, la note est livrée automatiquement si son handle Telegram correspond. Si un autre compte ouvre le lien, le bot vous demande d'approuver ou de refuser l'accès.

### Créer une voix (texte vers parole)
1. Ouvrez n'importe quelle note ou tâche.
2. Appuyez sur `🔊 Créer une voix`.
3. Le bot affiche immédiatement une notification système indiquant que la génération texte-vers-voix a commencé.
4. Le bot génère un message vocal avec OpenAI (voix `onyx`), l'envoie dans le chat et l'attache à cet élément.

### Médias vers texte
1. Ouvrez n’importe quelle note ou tâche.
2. Ouvrez `📚 Plus`.
3. Appuyez sur `🤖 Analyser avec l'IA`.
4. Le même bouton fonctionne maintenant aussi pour les éléments texte ordinaires et pour les images jointes, pas seulement pour l’audio/vidéo/PDF.
5. Le bot calcule le coût selon le chemin d’analyse réellement utilisé :
   - l’enrichissement IA de texte/liens utilise le tarif d’analyse de texte
   - les images enregistrées utilisent le tarif d’analyse d’image
   - La durée est mesurée dans le fichier réel avec ffprobe avant la réservation des points, sans estimation par taille ni durée fictive.
6. Si votre solde est suffisant, le bot réserve les points requis, exécute l’analyse IA, met à jour l’élément et ne valide le débit qu’après un traitement réussi.
   - Les transcriptions audio/vidéo ajoutées incluent des horodatages à la fin de chaque paragraphe lorsque les données de timing sont disponibles.
7. Si l’analyse IA échoue, les points réservés sont libérés et l’élément reste inchangé.

## 11. Fusionner des éléments (note/tâche)
1. Ouvrez un élément.
2. Appuyez sur `🔗 Fusionner`.
3. Le bot affiche jusqu'à 5 éléments du même type ouverts récemment.
4. Sélectionnez l'élément cible ou envoyez l'ID de l'élément cible sous forme de texte.
5. Le texte de l'élément source est ajouté au texte de l'élément cible.
6. L'élément source est supprimé et l'élément cible est ouvert.
7. L'avis de fusion réussie apparaît dans l'écran de l'élément cible ouvert, pas comme message séparé dans le chat.

## 11.1 Épingler des éléments
1. Ouvrez une note ou une tâche.
2. Appuyez sur `📚 Plus`.
3. Appuyez sur `📌 Épingler` pour garder l'élément en haut de sa liste.
4. Appuyez sur `📌 Désépingler` pour le remettre dans l'ordre chronologique normal.

## 12. Tags
1. Ouvrez une note.
2. Appuyez sur `🏷️ Tags`.
3. Appuyez sur un tag pour ouvrir les notes avec ce tag.
4. Pour ajouter des tags, envoyez un message avec des hashtags (exemple : `#project #urgent`).
5. Les noms de personnes détectés dans le texte de la note sont automatiquement ajoutés comme tags avec majuscule initiale.

## 13. Modifier une note
1. Ouvrez une note/tâche.
2. Appuyez sur `✏️ Modifier`.
3. Copiez seulement le texte propre du corps affiché dans l'invite, modifiez-le, puis renvoyez le texte complet.
4. Les lignes de source, le type localisé de l'élément et le pied `Enregistré via Telenota` sont réappliqués par le modèle du bot et ne doivent pas être saisis manuellement.
5. Le bot enregistre la modification et ajoute l'horodatage `dernière modification` dans le pied de page.

## 14. Supprimer ou archiver
1. Ouvrez une note/tâche.
2. Appuyez sur `❌ Supprimer`.
3. Choisissez :
   - `🗑️ Supprimer`
   - `🗄️ Archiver`
   - `⬅️ Retour`
4. Si vous choisissez `🗄️ Archiver`, le bot demande un commentaire d'archivage optionnel.
5. Envoyez le commentaire ou appuyez sur `✅ Sans commentaires`.
6. Le bot ajoute la ligne `Commentaire d'archivage : <comment>` en bas de l'élément, puis l'archive.
7. Si la note/tâche avait des pièces jointes média affichées dans le chat, ces messages de pièces jointes sont retirés de l'écran après suppression/archivage.

## 15. Tâche terminée et commentaires
1. Ouvrez une tâche.
2. Appuyez sur `✅ Fait`.
3. Saisissez un commentaire optionnel ou appuyez sur `✅ Sans commentaires`.
4. Tous les messages de pièces jointes actuellement affichés pour cette tâche sont supprimés du chat pendant que l'invite/la liste de fin est affichée ; les pièces jointes enregistrées restent dans l'élément.
5. Le résultat suit vos Paramètres :
   - Supprimer
   - Archiver
   - Garder

## 16. Rappels
1. Ouvrez une tâche.
2. Appuyez sur `⏰ Rappel`.
3. Envoyez une date/heure en format libre :
   - `demain à la même heure`
   - `dans 2 heures`
   - `2026-02-20 14:30`

## 17. Paramètres
Ouvrez `⚙️ Paramètres` pour configurer :
- `🌐 Langue` (premier élément)
  - English / Español / Français / Português / Русский / Українська / 简体中文 / العربية
- `🕒 Fuseau horaire`
  - appuyez sur `Fuseau horaire`
  - répondez avec une ville, un code de fuseau horaire ou le texte de l'heure actuelle
  - le bot utilise OpenAI pour déduire et enregistrer votre fuseau horaire
  - le fuseau enregistré est affiché sous la forme `UTC±HH:MM · City`
- `Marquer comme fait`
  - Supprimer / Archiver / Garder
- `Copier le texte pour les modifications`
  - Copier le texte de la note / Ne rien faire
- `🗓️ Digest quotidien des tâches`
  - `Définir l'heure` en texte libre comme `tous les jours à 8h`, `21:30`, `demain 7`
  - enregistrer une heure active aussi automatiquement le digest quotidien
  - `Activer` / `Désactiver`
  - dans Paramètres, l'état est affiché uniquement avec un cercle vert/rouge
  - le résumé des Paramètres affiche l'heure locale sans suffixe de fuseau horaire
  - le digest est envoyé une fois par jour à l'heure locale configurée de l'utilisateur
  - le digest inclut les sections :
    - `Rappels` ou `Aucun rappel avant le prochain digest`
    - `Tâches`
    - `Notes ajoutées depuis le dernier digest`
  - les éléments de toutes les sections sont des liens ; appuyer dessus ouvre la note/tâche correspondante dans le bot
  - le message de digest contient des boutons rapides : `⏰ Rappels`, `🟧 Tâches`
  - l'état est synchronisé entre le résumé des Paramètres et l'écran de détail du digest
- `🌙 Résumé du soir`
  - `Définir l'heure` avec le même analyseur d'heure libre que le digest du matin
  - enregistrer une heure active aussi automatiquement le résumé du soir
  - `Activer` / `Désactiver`
  - dans Paramètres, l'état est affiché uniquement avec un cercle vert/rouge
  - le résumé des Paramètres affiche l'heure locale sans suffixe de fuseau horaire
  - le digest du soir inclut :
    - `Tâches -> Tâches que j'ai terminées aujourd'hui`
    - `Tâches -> Tâches que j'ai créées aujourd'hui`
    - `Notes que j'ai ajoutées aujourd'hui`
  - après le digest, le bot demande :
    - `Et VOUS, comment avez-vous ressenti votre journée aujourd'hui ?`
    - répondez à cette invite précise par texte/voix/vidéo
    - le bot enregistre votre réponse comme note avec le tag `daily`
- `⏱️ Temps de fusion des messages`
  - appuyez sur le bouton
  - envoyez un nombre de secondes, par exemple `30`, `45`, `120`
  - les messages envoyés dans cet intervalle sont fusionnés en un seul brouillon
  - si l'écart est de `30` secondes ou plus (avec le réglage par défaut), un nouveau brouillon est créé
- `📱 Afficher le menu inférieur`
  - l'état est affiché uniquement avec un cercle vert/rouge
  - valeur par défaut : activé
  - lorsqu'il est activé, le clavier inférieur persistant est affiché pour cet utilisateur
  - lorsqu'il est désactivé, le clavier inférieur persistant est masqué pour cet utilisateur
  - modifier ce réglage est silencieux (pas de messages système sur la visibilité)
- `📚 Nombre d'éléments`
  - contrôle le nombre d'éléments affichés par page dans les écrans de liste

La gestion des contacts est disponible dans `Plus -> Paramètres -> Contacts` :
- voir tous les contacts enregistrés pour les assignations
- `➕ Ajouter un contact` (saisir `@handle` ou téléphone)
- `📱 Partager mon téléphone` (partager votre propre contact Telegram avec le bot)
- ouvrir un contact -> `Modifier` / `Supprimer`
- la modification met à jour la valeur de contact utilisée dans les suggestions d'assignation

## 18. Conseils
- Si une liste est longue, utilisez les boutons de pagination.
- Utilisez le menu de commandes (`/start`, `Mes notes`, `Tâches`, etc.) pour naviguer rapidement.
- `Archiver` masque l'élément dans les listes normales de notes/tâches, mais conserve les données.

## 19. Si quelque chose semble cassé (côté client)
Si des actions semblent bloquées (par exemple, appuyer sur un bouton envoie votre message mais le bot ne répond pas), essayez :
- envoyer `/start`
- appuyer sur un bouton inline de l'écran de bienvenue
- appuyer/envoyer `⬅️ Retour` ou `/back`
- fermer puis rouvrir l'application Telegram
- si le problème persiste, effacer l'historique du chat et rouvrir la conversation avec le bot

## 20. Comment bien signaler un bug
Lorsque vous signalez un bug, indiquez :
- le bouton/l'action exact que vous avez utilisé
- la date/heure et le fuseau horaire exacts
- une capture d'écran ou un court enregistrement d'écran
- la réponse exacte du bot, ou le fait qu'il n'y a pas eu de réponse
- si `/start` fonctionne encore alors que d'autres boutons ne fonctionnent pas

## Documents associés
- Conditions d'utilisation : [dépôt des documents légaux](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Flux d'écrans : [Flux d'écrans](/docs/Screenflow.md)
- Installation : [Installation](/docs/installation.md)
- Index de la documentation : [Accueil de la documentation](/docs/README.md)

## 21. Mises à jour du partage et de la source
- `Plus -> Partager` fonctionne maintenant pour les notes et les tâches.
- Dans le sélecteur de partage, vous pouvez choisir un contact enregistré ou appuyer sur `Partager publiquement` pour créer un message transférable avec le lien de démarrage du bot.
- Les partages publics trop longs sont automatiquement découpés en plusieurs messages transférables ; chaque message se termine par le pied standard `Enregistré via Telenota (<date et heure locales>)`.
- Si quelqu’un démarre le bot pour la première fois via votre lien d’invitation ou votre lien privé de partage, vous recevez une notification persistante du bot indiquant qu’il a rejoint le service.
- Lorsque Telegram fournit suffisamment de métadonnées, `Source` ouvre le message Telegram d'origine exact.
- Les brouillons, les notes et les tâches affichent la date et l'heure d'enregistrement dans votre fuseau horaire.

## Démarrage guidé et brouillons avec IA
- Au premier démarrage, effectuez trois actions utiles et recevez le bonus de bienvenue en plusieurs fois : `+2`, `+3` et `+5` points.
- `Note avec IA` et `Tâche avec IA` conservent le texte d'origine, convertissent tous les fichiers compatibles en texte dans l'ordre et ajoutent un résumé lisible en trois paragraphes.
- Chaque pièce jointe extraite est identifiée par son type et son ordre d’origine ; le texte complet précède le résumé.
- Les mentions n’attribuent ni ne partagent jamais automatiquement : Telenota vous demande de choisir l’action.
- `Retour` remonte l'historique des écrans et `Accueil` revient directement à l'écran principal.
- Si un élément occupe plusieurs messages Telegram, ses boutons apparaissent sous le dernier message.

## Dernières mises à jour (0.35.2)
- Les photos et vidéos consécutives d'un même lot capturé sont maintenant affichées comme album Telegram lorsque Telegram autorise ce format.
- L'aperçu du brouillon conserve plus fidèlement les compteurs groupés des pièces jointes ainsi que le texte d'origine, sans répéter plusieurs fois le même segment fusionné.
- Dans les notes, tâches et brouillons, le pied de page est maintenant plus compact : auteur et source sont affichés sur une seule ligne localisée, et l'heure d'enregistrement n'affiche que la date et l'heure locales.
- Lors de l'ouverture d'une note ou d'un brouillon lourd, il n'est plus nécessaire d'attendre le chargement complet de toutes les pièces jointes pour utiliser la carte principale ; les médias continuent de se charger en arrière-plan.
- Les écrans Contacts, Thèmes et Historique des points ont désormais une dernière ligne explicite `Retour` / `Accueil`, et les grands sélecteurs de pages naviguent par fenêtres plutôt que dans une seule grande grille.
- Les lignes de l’Historique des points peuvent maintenant afficher la note ou la tâche liée ainsi qu’un lien profond vers l’élément lorsque le mouvement est rattaché à un élément enregistré qui existe encore.

## Dernières mises à jour (0.36)
- Les notes et tâches prennent maintenant en charge les commentaires. Ouvrez un élément et touchez `Commentaires (N)` pour voir les commentaires existants comme des messages Telegram séparés avec `Commenter` / `Supprimer`.
- Quand le mode commentaire est actif, le texte/média envoyé ou transféré suivant s’affiche d’abord comme aperçu avec `Commenter`, `Créer un brouillon`, `Retour` et `Accueil` ; il n’est enregistré sous l’élément comme `Commentaire N` qu’après confirmation.
- Les brouillons et éléments enregistrés gardent les lignes techniques de transfert plus compactes : `Transféré sans commentaires`, auteur/source et heure d’enregistrement restent ensemble sans lignes vides inutiles.
- Les aperçus de brouillon affichent les compteurs de pièces jointes près de la fin de la carte, au-dessus des métadonnées de transfert/source, et conservent le format Telegram quand c’est possible.
- Lancer `Analyse IA` sur une note ou une tâche déjà enregistrée ajoute désormais le résultat sous le contenu existant, sous l’intitulé `Résultats de l’analyse IA :`, au lieu de remplacer votre contenu enregistré.
- Marquer une tâche comme terminée annule désormais ses rappels programmés, et les suggestions de rappel utilisent votre langue d’interface enregistrée pour reconnaître les mois et jours localisés.
- `Plus` ne contient plus de bouton `Paramètres` en double ; ouvrez les Paramètres depuis l’écran d’accueil.
- `Points` contient un lien direct vers la documentation publique des points.
- Les suggestions de `Fusionner` privilégient maintenant les éléments avec des étiquettes similaires sans IA ; le classement sémantique IA n’est pas activé par défaut, car il ajouterait du coût et de la latence.

## Dernières mises à jour (0.36.2.phase4-5)
- L’aperçu du brouillon peut afficher un interrupteur de traduction rouge/vert avant l’enregistrement. Rouge conserve la langue d’origine ; vert traduit le brouillon dans la langue de votre interface lors d’un enregistrement normal en note ou tâche.
- Les résumés IA des notes et tâches utilisent désormais la langue d’interface choisie, même si le texte source est dans une autre langue.
- Les messages transférés rapidement sont fusionnés dans leur ordre d’arrivée.
- Les écrans de fusion ouverts depuis des messages avec média utilisent maintenant un repli sûr au lieu d’afficher une erreur d’édition Telegram.
- Les albums transférés sont désormais enregistrés de manière sérialisée afin de conserver chaque image, vidéo et légende dans l’ordre d’origine. Les sondages transférés conservent un instantané textuel de leurs options et résultats disponibles ; sans résultat, une note demande de voter dans le sondage d’origine.
- Pour les lignes d’adresse explicites, le bot peut proposer des correspondances précises OpenStreetMap. Elles ne sont ajoutées comme commentaires de localisation qu’après confirmation lors de l’enregistrement d’une note ou tâche.

## Dernières mises à jour (0.36.4)
- Les commentaires conservent la mise en forme Telegram et utilisent `Enregistrer`, `❌ Supprimer` et `Retour` ; revenir ou supprimer efface aussi l’ancien écran des commentaires.
- Les instantanés de sondage affichent les votes par option et le total uniquement lorsque Telegram les fournit. Sinon, Telenota indique clairement que les résultats sont inconnus et n’invente jamais de votes à zéro.
- Les adresses explicites sont détectées dans les messages directs et transférés, y compris avec des abréviations de rue multilingues. Seule l’adresse candidate extraite est envoyée à OpenStreetMap et les correspondances ambiguës ne sont pas ajoutées.
- Dans un bloc de coordonnées, `Контакты: av. Aragon nº4-bis` devient l’adresse `Avenida Aragon, 4-bis`. Les abréviations de voie et les indicateurs de numéro espagnols sont normalisés sans perdre `-bis` ni les suffixes alphabétiques. Les téléphones, courriels et liens voisins sont exclus de la requête. La ville explicitement indiquée est conservée ; aucune ville ni position approximative n’est inventée.

## Version 0.35.0.4
- Les titres IA utilisent le texte disponible, le résumé du lien et l'analyse des pièces jointes compatibles. Un brouillon ne contenant qu'une pièce jointe conserve un titre de type de média jusqu'à son analyse.
- L'analyse IA d'un élément enregistré combine son texte avec le texte extrait de toutes les pièces jointes compatibles avant d'ajouter le résultat.
- Dans les transferts regroupés, chaque segment affiche son auteur avant son texte. La suggestion de rappel disparaît après toute action ; `Ignorer` n'annule que le rappel.

## Version 0.35.0.5
- Dans un élément fusionné, chaque auteur apparaît avant le texte de son message transféré.
- Le résumé IA apparaît avant le texte OCR ou extrait des pièces jointes.
- Les réglages utilisent un titre localisé et court ; Telegram contrôle l'alignement du texte des boutons.
- Seule une réponse explicite à l’invite de réflexion du soir est enregistrée comme réflexion. Un texte, lien ou fichier envoyé séparément après le bilan crée un brouillon normal et n’est pas bloqué par un ancien mode de saisie.
