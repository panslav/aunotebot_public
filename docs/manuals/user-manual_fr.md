# Guide utilisateur de Telenota

<!-- docs-toc:start -->
Sommaire

- [1. Objectif et fonctionnalités](#purpose)
- [2. Notions principales](#concepts)
- [3. Premiers pas](#start)
- [4. Commandes et navigation](#commands)
- [5. Capturer et enregistrer](#capture)
- [6. Consulter et rechercher](#find)
- [7. Gérer les notes et tâches](#items)
- [8. Définir des rappels](#reminders)
- [9. Exporter vers un calendrier](#calendar)
- [10. Partager et attribuer](#sharing)
- [11. Fusionner des éléments](#merge)
- [12. Commentaires et tâches terminées](#comments)
- [13. Tags et éléments épinglés](#tags)
- [14. Points et IA](#points)
- [15. Paramètres](#settings)
- [16. Confidentialité, limites et assistance](#help)
- [17. Historique des modifications](#history)
<!-- docs-toc:end -->

<a name="purpose"></a>

## 1. Objectif et fonctionnalités

Telenota transforme vos messages, idées et pièces jointes Telegram en notes et tâches organisées, pour les retrouver et agir plus tard. Tout se passe dans le chat du bot, sans autre application de notes.

- Capturez textes, transferts, liens, voix, vidéos, images et documents compatibles.
- Vérifiez les brouillons, enregistrez des notes ou tâches, ajoutez des commentaires et des tags.
- Recherchez vos informations, programmez des rappels, exportez des événements, partagez ou attribuez des éléments.
- Choisissez une analyse IA, une traduction ou une voix générée si nécessaire. Ces actions peuvent utiliser des points ; la capture et l’enregistrement manuels restent accessibles sans IA.


<a name="concepts"></a>

## 2. Notions principales

**Note** : information enregistrée à conserver.

**Tâche** : élément enregistré que vous pouvez terminer, attribuer ou programmer.

**Élément (Item)** : une note ou tâche enregistrée explicitement. Cet enregistrement ne la partage pas avec d’autres personnes.

**Brouillon** : contenu capturé qui attend un enregistrement explicite ; il n’est pas encore publié.

**Rappel** : tâche avec une date et une heure ; ce n’est pas un export de calendrier.

**Tag/thème** : étiquette pour classer et retrouver des éléments.

**Commentaire** : texte ou média ajouté à un élément.

**Archives** : éléments conservés mais masqués des listes actives ; archiver ne signifie pas supprimer.

<a name="start"></a>

## 3. Premiers pas

1. Ouvrez le chat du bot et envoyez `/start`.
2. Dans Paramètres, depuis Démarrage, vérifiez la langue et le fuseau horaire.
3. Envoyez un court texte ou transférez un message, puis vérifiez le brouillon.
4. Enregistrez-le comme note ou tâche. Choisissez une action IA uniquement si vous souhaitez une analyse payante.
5. Utilisez les raccourcis de confirmation pour ouvrir l’élément ou sa liste. Définissez un rappel si nécessaire.

L’accueil guidé accorde 10 points en trois actions utiles : +2, +3 et +5. Les 10 points ne sont pas versés en une seule fois au premier démarrage. Les boutons d’un brouillon restent disponibles jusqu’à votre intervention.

<a name="commands"></a>

## 4. Commandes et navigation

- `/start` — Ouvrir Démarrage et recharger les préférences
- `/find` — Rechercher notes et tâches
- `/notes` — Ouvrir les notes
- `/tasks` — Ouvrir les tâches
- `/drafts` — Ouvrir les brouillons
- `/reminders` — Ouvrir les rappels
- `/more` — Ouvrir Plus, avec Aide et Mentions légales
- `/settings` — Ouvrir les paramètres
- `/back` — Revenir à l’écran précédent

Le menu de commandes contient les raccourcis principaux ; Paramètres est aussi accessible depuis Démarrage. Plus → Aide ouvre ce guide dans votre langue. Le mode de recherche reste actif jusqu’à sa fermeture. Le texte envoyé pendant une recherche, un rappel ou un commentaire explicitement ouvert appartient à cette action. Revenez en arrière avant de capturer un texte indépendant.

<a name="capture"></a>

## 5. Capturer et enregistrer

Les liens traités en file utilisent la langue d’interface actuellement enregistrée. Le titre et la description publics de la page peuvent servir de solution de repli si l’analyse échoue ; les pages restreintes peuvent rester indisponibles. Le brouillon apparaît sans attendre un titre IA provisoire séparé.

### Créer une note

1. Envoyez du texte simple au bot.
2. Le bot affiche un aperçu de brouillon.
3. Appuyez sur `📝 Enregistrer comme note`.
4. Utilisez les raccourcis de confirmation pour ouvrir l’élément ou sa liste.

### Créer une tâche

Option A :
1. Envoyez du texte.
2. Dans l'aperçu du brouillon, appuyez sur `🟧 Enregistrer comme tâche`.
3. Utilisez les raccourcis de confirmation pour ouvrir l’élément ou sa liste.

Option B :
1. Ouvrez n'importe quelle note.
2. Appuyez sur `⬛ Créer une tâche`.

### Transférer des messages

1. Transférez un ou plusieurs messages au bot.
2. Le bot fusionne les messages transférés proches dans le temps en un seul brouillon.
   - Le délai de fusion par défaut est de `30` secondes.
   - Vous pouvez le modifier dans `Démarrage -> Paramètres -> Temps de fusion des messages`.
3. Si vous ajoutez du texte simple juste après le transfert, le bot l'ajoute ainsi :
   - `💬 Transféré avec le commentaire :`
   - `<votre texte>`
   avant la ligne de source/pied de page.
4. Dans la vue note/tâche, les sources publiques d’utilisateurs Telegram sont affichées comme liens cliquables `@handle` au lieu d’URL brutes `https://t.me/...`, une seule ligne vide est conservée avant le pied final `Enregistré via Telenota (...)`, et ce pied inclut aussi un lien cliquable `votre message` vers le message exact du bot à l’origine de l’élément quand Telegram l’expose encore.
5. Si un message transféré contient un ou plusieurs liens web, le bot utilise d'abord les métadonnées d'aperçu disponibles pour chaque page et, lorsqu'elles sont absentes, tente un fallback déterministe et sûr du titre à partir des métadonnées de la page.
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

### Voix et vidéo

1. Envoyez un message vocal, un fichier audio (y compris `.m4a` lorsque Telegram l'envoie comme audio ou document audio), une vidéo ou une note vidéo.
2. Pour les messages vocaux et les fichiers audio, le bot affiche immédiatement un message de traitement lorsque l'analyse démarre.
3. Pour les vidéos normales, notes vidéo et documents vidéo, le bot enregistre d'abord le média comme brouillon ; l'analyse IA démarre seulement quand vous choisissez `Note avec IA` ou `Tâche avec IA`.
4. Lors de l’analyse par IA, le bot transcrit le fichier et prépare le texte du brouillon ou de l’élément.
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

La reconnaissance vocale utilise GPT-Transcribe. La configuration actuelle ne fournit ni horodatage par paragraphe ni identification acoustique des interlocuteurs. La mise en forme peut conserver des tours de dialogue étayés par le contenu, sans déterminer l’identité à partir des voix. Les titres sont gratuits et une analyse commune peut être réutilisée pour le résumé, le titre et les métadonnées.

Avant l’analyse vidéo en plusieurs étapes, le bot réserve le coût total. Si le résultat complet ne peut pas être livré, la réservation est remboursée ; si la vidéo ne contient pas d’audio exploitable, la transcription inutilisée est remboursée. L’analyse visuelle peut aboutir. D’autres pièces jointes ou étapes prises en charge peuvent être facturées séparément.

### Images et captures d'écran

1. Envoyez ou transférez une image/capture d'écran.
2. Le bot exécute l'OCR et résume le texte/contenu visible important.
3. Un brouillon est créé ; enregistrez-le ensuite comme note ou tâche.
4. Si vous envoyez un document PDF textuel et choisissez une action d’enregistrement avec IA, le bot conserve le contenu d’origine du brouillon, ajoute le texte extrait du PDF, puis ajoute un bref résumé IA de `300` mots maximum dans la langue d’interface choisie.
5. Le texte extrait est conservé sous forme de paragraphes lisibles, et le résumé IA est rendu en trois courtes parties : introduction, partie principale et conclusion.
6. Les PDF scannés ou composés uniquement d’images peuvent échouer pendant l’analyse IA tant que la prise en charge OCR pour PDF n’a pas été ajoutée.
7. Si vous enregistrez un PDF sans IA, le brouillon/l’élément conserve une simple ligne `PDF <nom du fichier>`. Si vous ouvrez ensuite l’élément enregistré et appuyez sur `Analyse IA`, le même flux de résumé PDF est lancé.
8. Telegram Bot API ne transmet pas aux bots le fichier média d’une Story transférée. Le bot enregistre sa référence et vous demande d’envoyer ensuite une capture d’écran, une photo ou une vidéo téléchargée ; ce fichier est joint au même brouillon.
9. Lors de l’analyse IA d’une image, l’élément enregistré affiche d’abord le résumé IA, puis le texte OCR reconnu. Les listes numérotées et à puces de l’image conservent leur format.

### Démarrage guidé et brouillons avec IA

- Les actions de note et tâche avec IA analysent ensemble le texte original disponible et les pièces jointes compatibles. Titres des brouillons et résumés utilisent la langue de l’interface. Vérifiez le résultat.
- Si un bouton de traduction apparaît, le rouge conserve la langue d’origine et le vert traduit dans la langue de l’interface à l’enregistrement d’une note ou tâche ordinaire.
- Si un élément occupe plusieurs messages Telegram, ses boutons figurent sous le dernier.

<a name="find"></a>

## 6. Consulter et rechercher

La recherche locale donne davantage de poids aux mots distinctifs et écarte les mots grammaticaux courants. Ce classement n’appelle pas l’IA et n’ajoute aucun coût.

### Parcourir notes et tâches

- Utilisez le menu de commandes Telegram (hamburger) :
  - `🏠 Démarrer`
  - `🔎 Rechercher`
  - `📝 Mes notes`
  - `🗂️ Brouillons`
  - `🟧 Tâches`
  - `⏰ Rappels`
  - `📚 Plus`
- Si le menu inférieur est activé (`Démarrage -> Paramètres -> Afficher le menu inférieur`) :
  - ligne 1 : `📝 Mes notes` + nouvelle ligne + `(N)`, `⏰ Rappels` + nouvelle ligne + `(N)`, `🟧 Tâches` + nouvelle ligne + `(N)`
  - ligne 2 : `🗂️ Brouillons` + nouvelle ligne + `(N)`, `🔎 Rechercher`, `📚 Plus`
- Les en-têtes de liste comme `📝 Mes notes` et `🗂️ Brouillons` s’affichent sur une seule ligne visible, sans espacement invisible.
- Lorsque vous ouvrez une tâche depuis la page 2+ puis la marquez comme faite, la supprimez, la convertissez ou définissez un rappel, le bot revient à la même page de liste de tâches lorsqu'il réaffiche la liste.
  - lorsqu'il est activé, le menu inférieur reste visible jusqu'à ce que l'utilisateur le désactive dans les paramètres
  - ces boutons ouvrent les mêmes écrans que les actions du menu hamburger.
- Vous pouvez aussi utiliser les compteurs inline de l'écran de démarrage :
  - ligne 1 : `📝 Notes (N)`, `🟧 Tâches (N)`
  - ligne 2 : `🗂️ Brouillons (N)`, `⏰ Rappels (N)`
  - ligne 3 : `🔎 Rechercher`, `⚙️ Paramètres`
  - ligne 4 : `⬅️ Retour`, `📚 Plus`

### Rechercher (recherche fusionnée + Recall)

1. Ouvrez Rechercher depuis l’accueil ou envoyez `/find`, puis saisissez une requête.
2. La recherche locale, les variantes de mots, la navigation et la pagination sont gratuites. Les archives peuvent apparaître ; un numéro exact comme `219` ou `#219` place l’élément en tête s’il existe.
3. Ouvrez un résultat ou choisissez **Répondre avec l’IA** pour demander une réponse contextuelle à **5 points**. Le bouton n’affiche pas le prix. Saisir une requête ne demande pas de réponse payante.
4. Une réponse inchangée est réutilisée sans nouveau paiement dans la même session ; la pagination et le retour aux résultats n’appellent pas l’IA. Modifier la requête, le contexte, la langue ou le modèle peut nécessiter une nouvelle réponse.
5. Si la réponse échoue ou si votre solde est insuffisant, les résultats locaux restent disponibles et vous pouvez réessayer explicitement. Retour quitte la recherche et retrouve l’écran précédent.

<a name="items"></a>

## 7. Gérer les notes et tâches

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

### Créer une voix (texte vers parole)
1. Ouvrez n'importe quelle note ou tâche.
2. Appuyez sur `🔊 Créer une voix`.
3. Le bot affiche immédiatement une notification système indiquant que la génération texte-vers-voix a commencé.
4. Le bot génère un message vocal avec OpenAI (voix `onyx`), l'envoie dans le chat et l'attache à cet élément.

La lecture audio conserve les liens de l’auteur et de la source, y compris après conversion d’une note en tâche ou inversement. Les liens sans schéma, comme Tambur.pub, s’ouvrent en HTTPS au lieu de s’afficher en Markdown.

La durée de l’audio généré est mesurée et conservée à la réouverture de l’entrée. Relancer la lecture du même texte avec la même voix et le même modèle réutilise le fichier enregistré, sans nouvelle facturation de génération IA ni pièce jointe en double. Modifier le texte lu crée une nouvelle version. Les anciens fichiers audio d’origine indéterminée ne sont pas supprimés automatiquement.

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
   - La configuration actuelle ne fournit pas d’horodatage par paragraphe ; certaines anciennes configurations peuvent le faire.
7. Si l’analyse IA échoue, les points réservés sont libérés et l’élément reste inchangé.

### Modifier une note

1. Ouvrez une note/tâche.
2. Appuyez sur `✏️ Modifier`.
3. Copiez seulement le texte propre du corps affiché dans l'invite, modifiez-le, puis renvoyez le texte complet.
4. Les lignes de source, le type localisé de l'élément et le pied `Enregistré via Telenota` sont réappliqués par le modèle du bot et ne doivent pas être saisis manuellement.
5. Le bot enregistre la modification et ajoute l'horodatage `dernière modification` dans le pied de page.

### Supprimer ou archiver

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

La suggestion de personnes mentionnées utilise une seule action de retour : Ouvrir l’élément. Une mention ne partage ni n’attribue automatiquement.

<a name="reminders"></a>

## 8. Définir des rappels

Ouvrez une tâche, choisissez Rappel et indiquez une date et une heure dans votre fuseau enregistré. Les dates futures reconnues dans de nouvelles tâches peuvent aussi être programmées à l’enregistrement. Une date sans heure utilise celle du récapitulatif quotidien des tâches ; si elle n’est pas définie, précisez une heure.

Une suggestion sur une note ne la transforme pas automatiquement en tâche : acceptez le rappel pour la convertir et le programmer. Une heure seule correspond à aujourd’hui, sauf indication contraire. Vérifiez la confirmation. Les anciens éléments ne sont pas reprogrammés automatiquement.

Terminer une tâche annule ses rappels programmés. Un rappel avec seulement une date utilise l’heure du récapitulatif ; un export de calendrier avec seulement une date crée un événement sur toute la journée.

<a name="calendar"></a>

## 9. Exporter vers un calendrier

Le lien Google ouvre un formulaire : vérifiez les informations et enregistrez vous-même l’événement. ICS reste disponible ; le changement du point d’entrée Google ne refacture pas un export inchangé. Il n’ajoute ni création automatique ni connexion OAuth.

L’export calendrier apparaît dans la fiche si une date ou une heure est détectée, et reste toujours disponible dans Plus. Le libellé du bouton ne contient pas de prix ; l’export coûte 0,10 point. Un appui envoie directement un fichier d’événement .ics, sans aperçu intermédiaire dans le bot, ainsi qu’un lien Google Agenda de secours. Ouvrez le fichier dans votre calendrier et confirmez l’importation ; Telegram ou le système peut demander de choisir une application. L’ouverture automatique du calendrier par défaut n’est garantie ni sur iOS, ni sur Android, ni sur ordinateur.

Si Telegram ne confirme pas l’envoi de l’ICS, le bot envoie un message distinct avec le lien Google Agenda prérempli. La confirmation correspond à un identifiant de message et de fichier renvoyé par Telegram, pas au téléchargement ou à l’importation sur l’appareil. Le lien ne nécessite pas de connexion OAuth au bot.

Une date seule crée un événement sur toute la journée ; une heure seule utilise aujourd’hui dans votre fuseau enregistré, même si l’heure est passée. Une date et une heure utilisent le moment indiqué. La durée par défaut est de 60 minutes. Le titre commence par l’icône de note/tâche et reprend le titre de la fiche ; la description contient un lien vers celle-ci dans le bot, sans son texte privé. Si la date manque, est invalide ou ambiguë, Plus demande une seule date/heure de début ; Retour annule, les fichiers et transferts créent un nouveau brouillon.

Un seul envoi réussi du même événement est facturé par utilisateur. Le récupérer à nouveau est gratuit, même après un redémarrage du bot ; les échecs d’envoi sont remboursés. Changer le titre, la date ou l’heure produit un nouvel événement. Le bot ne confirme pas l’enregistrement dans le calendrier. Réimporter peut créer des doublons ; les modifications ultérieures ne sont pas synchronisées. Le fichier disparaît du chat à la fermeture des pièces jointes de la fiche. Aucun compte calendrier ni analyse IA payante n’est requis.

<a name="sharing"></a>

## 10. Partager et attribuer

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

### Partage public et liens sources

- `Plus -> Partager` fonctionne maintenant pour les notes et les tâches.
- Dans le sélecteur de partage, vous pouvez choisir un contact enregistré ou appuyer sur `Partager publiquement` pour créer un message transférable avec le lien de démarrage du bot.
- Les partages publics trop longs sont automatiquement découpés en plusieurs messages transférables ; chaque message se termine par le pied standard `Enregistré via Telenota (<date et heure locales>)`.
- Si quelqu’un démarre le bot pour la première fois via votre lien d’invitation ou votre lien privé de partage, vous recevez une notification persistante du bot indiquant qu’il a rejoint le service.
- Lorsque Telegram fournit suffisamment de métadonnées, `Source` ouvre le message Telegram d'origine exact.
- Les brouillons, les notes et les tâches affichent la date et l'heure d'enregistrement dans votre fuseau horaire.

### Gérer les contacts

La gestion des contacts est disponible dans `Plus -> Contacts` :
- voir tous les contacts enregistrés pour les assignations
- `➕ Ajouter un contact` (saisir `@handle` ou téléphone)
- `📱 Partager mon téléphone` (partager votre propre contact Telegram avec le bot)
- ouvrir un contact -> `Modifier` / `Supprimer`
- la modification met à jour la valeur de contact utilisée dans les suggestions d'assignation

<a name="merge"></a>

## 11. Fusionner des éléments

1. Ouvrez un élément et choisissez Plus → Fusionner.
2. Sélectionnez une destination proposée ou saisissez son numéro. Les candidats sont vos éléments actifs du même type ; les tags communs passent avant la pertinence du texte.
3. La destination conserve son numéro et son titre. Le texte intégral est ajouté sans réécriture IA ni troncature ; tags et pièces jointes distinctes sont conservés.
4. Les rappels différents sont préservés sans doubler une même échéance.
5. La source est archivée, pas supprimée. Ses commentaires restent dans cette archive.
6. La destination s’ouvre et les copies déjà attribuées sont mises à jour.

<a name="comments"></a>

## 12. Commentaires et tâches terminées

Les tâches terminées sont exclues de la liste active Tâches et de son compteur. Si votre réglage conserve l’élément à la fin, son enregistrement reste sauvegardé ; le masquer de la liste active ne le supprime pas.

### Tâche terminée et commentaires

1. Ouvrez une tâche.
2. Appuyez sur `✅ Fait`.
3. Saisissez un commentaire optionnel ou appuyez sur `✅ Sans commentaires`.
4. Tous les messages de pièces jointes actuellement affichés pour cette tâche sont supprimés du chat pendant que l'invite/la liste de fin est affichée ; les pièces jointes enregistrées restent dans l'élément.
5. Le résultat suit vos Paramètres :
   - Supprimer
   - Archiver
   - Garder

- Les notes et tâches prennent maintenant en charge les commentaires. Ouvrez un élément et touchez `Commentaires (N)` pour voir les commentaires existants comme des messages Telegram séparés avec `Commenter` / `Supprimer`.
- Quand le mode commentaire est actif, le texte/média envoyé ou transféré suivant s’affiche d’abord comme aperçu avec `Commenter`, `Créer un brouillon`, `Retour` et `Accueil` ; il n’est enregistré sous l’élément comme `Commentaire N` qu’après confirmation.

<a name="tags"></a>

## 13. Tags et éléments épinglés

### Tags

1. Ouvrez une note.
2. Appuyez sur `🏷️ Tags`.
3. Appuyez sur un tag pour ouvrir les notes avec ce tag.
4. Pour ajouter des tags, envoyez un message avec des hashtags (exemple : `#project #urgent`).
5. Les noms de personnes détectés dans le texte de la note sont automatiquement ajoutés comme tags avec majuscule initiale.

### Épingler des éléments

1. Ouvrez une note ou une tâche.
2. Appuyez sur `📚 Plus`.
3. Appuyez sur `📌 Épingler` pour garder l'élément en haut de sa liste.
4. Appuyez sur `📌 Désépingler` pour le remettre dans l'ordre chronologique normal.

<a name="points"></a>

## 14. Points et IA

Une journée locale avec activité admissible rapporte 0,50 point : créez un élément ou commentaire de plus de 100 caractères visibles, ou partagez/attribuez un élément à une autre personne. Consulter, modifier ou recevoir une copie ne compte pas. Les trois jours inactifs suivants rapportent 0,30, 0,15 puis 0,05 ; à partir du quatrième, les bonus cessent jusqu’à une nouvelle activité admissible.

Si un bonus d’inactivité a déjà été versé, l’activité complète le total du jour jusqu’à 0,50 sans ajouter encore 0,50. Aucun rattrapage des jours manqués ni recalcul des anciens soldes. Réessayer une notification ne crédite pas de nouveau le compte ; après une interruption, un même avis peut toutefois apparaître plusieurs fois.

L’export calendrier coûte `0,10 point` pour l’envoi réussi du fichier ou du lien de secours, une fois par utilisateur et événement inchangé. Un échec ICS suivi du lien Google constitue une seule opération. Si aucun n’est envoyé, la réservation est remboursée. Réexporter est gratuit, même après un redémarrage. Le bouton n’affiche pas le prix.

1. Les actions alimentées par l'IA utilisent votre solde de points.
2. Modèle de facturation par défaut :
   - `1 point = 1 Telegram Star`
   - L’accueil guidé accorde 10 points en trois actions utiles : +2, +3 et +5. Les 10 points ne sont pas versés en une seule fois au premier démarrage.
   - pas de récompense automatique en points pour la création de notes/tâches
   - `1.5 point / minute` pour le texte vers voix
   - `1.0 point / minute` pour l'analyse audio
   - `1.5 point / minute` pour convertir en texte l'audio/vidéo déjà joint à un élément enregistré
   - `0.5 point` par OCR d'image
   - Résumé et étiquettes : `0.20 point` ; traduction : `0.50 point` ; résumé audio, analyse des images vidéo et résumé PDF : `1 point` par étape. Les titres sont gratuits ; analyse de lien : `0.05 point`.
3. La durée réelle du fichier est mesurée avant la réservation des points ; elle n’est pas déduite de sa taille.
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
5. Lorsque vous achetez des points dans le bot, les recharges Telegram Stars sont facturées directement en `XTR`.
6. Si votre solde est insuffisant :
   - la fonctionnalité IA est bloquée pour cette action
   - le bot affiche une notification
   - les fonctionnalités sans IA continuent de fonctionner
7. Actions IA payantes typiques :
   - résumés et tags
   - génération de réponses Recall/Find
   - traduction
   - interprétation libre de rappels, fuseau horaire et heures de digest
   - transcription et texte vers voix

<a name="settings"></a>

## 15. Paramètres

**Masquer les messages système :** 5, 10 ou 30 secondes, 1 minute ou Jamais ; 30 secondes par défaut. Ce délai concerne les nouveaux avis temporaires. Les actions des brouillons en attente restent disponibles. Le nettoyage de navigation et les mises à jour techniques du clavier sont distincts.

### Langue

1. Au premier `/start`, le bot essaie de détecter votre langue à partir de la locale Telegram.
2. La langue de repli par défaut est l'anglais.
3. Pour changer de langue manuellement :
   - ouvrez `Démarrage -> Paramètres -> Langue`
   - choisissez l'une des langues, dans cet ordre : `English`, `Español`, `Français`, `Português`, `Русский`, `Українська`, `简体中文`, `العربية`
4. Toutes les principales étiquettes et tous les boutons de l'interface sont traduits après la sélection.

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

<a name="help"></a>

## 16. Confidentialité, limites et assistance

Les erreurs proposent Retour et Accueil. Si un lien échoue, conservez le code pour l’assistance et revenez à la navigation ; une page restreinte peut rester inaccessible. Le chargement intermittent des images reste à l’étude ; les photos gardent leur présentation et leur qualité.

`Démarrage -> Paramètres` contient aussi une zone dangereuse pour supprimer les données de votre compte Telenota.

Supprimer toutes les données efface définitivement vos notes, tâches, brouillons, rappels, contacts, paramètres, historique de points et enregistrements de compte liés appartenant au bot.

L’IA peut se tromper : vérifiez résumés, dates et traductions. Les fonctions IA transmettent le contenu pertinent au fournisseur. Le corps est chiffré au stockage ; titres, tags et autres métadonnées ne sont pas tous chiffrés.

Le transport Telegram utilisé limite les téléchargements à 20 Mo par fichier multimédia. L’acceptation de Telegram ne prouve pas la fin du téléchargement sur votre appareil. Les retards intermittents d’images restent non résolus. Importer un événement ne synchronise pas les calendriers ; Google OAuth n’est pas activé.

Pour un écran bloqué, essayez /start, Retour, puis relancez Telegram. Effacer le chat n’est pas un dépannage de routine : vous pouvez perdre un historique utile. Ne publiez pas de secrets ni de contenu privé dans un signalement.

### Comment bien signaler un bug

Lorsque vous signalez un bug, indiquez :
- le bouton/l'action exact que vous avez utilisé
- la date/heure et le fuseau horaire exacts
- une capture d'écran ou un court enregistrement d'écran
- la réponse exacte du bot, ou le fait qu'il n'y a pas eu de réponse
- si `/start` fonctionne encore alors que d'autres boutons ne fonctionnent pas

[Assistance et suggestions](https://t.me/telenota_chat) · [Conditions d’utilisation](https://raw.githubusercontent.com/panslav/aunotebot_public/main/docs/legal/terms-and-conditions_fr.md)

<a name="history"></a>

## 17. Historique des modifications

Les notes suivantes décrivent des versions antérieures. Pour le fonctionnement actuel, suivez les instructions ci-dessus ; certains comportements historiques ont changé.

### 0.25

Note de maintenance (clarification de la limite audio v0.25) : pour l'audio téléversé via Telegram, ce bot applique la limite de téléchargement de Telegram Bot API.

### Version 0.35.0.4

- Les titres IA utilisent le texte disponible, le résumé du lien et l'analyse des pièces jointes compatibles. Un brouillon ne contenant qu'une pièce jointe conserve un titre de type de média jusqu'à son analyse.
- L'analyse IA d'un élément enregistré combine son texte avec le texte extrait de toutes les pièces jointes compatibles avant d'ajouter le résultat.
- Dans les transferts regroupés, chaque segment affiche son auteur avant son texte. La suggestion de rappel disparaît après toute action ; `Ignorer` n'annule que le rappel.

### Version 0.35.0.5

- Dans un élément fusionné, chaque auteur apparaît avant le texte de son message transféré.
- Le résumé IA apparaît avant le texte OCR ou extrait des pièces jointes.
- Les réglages utilisent un titre localisé et court ; Telegram contrôle l'alignement du texte des boutons.
- Seule une réponse explicite à l’invite de réflexion du soir est enregistrée comme réflexion. Un texte, lien ou fichier envoyé séparément après le bilan crée un brouillon normal et n’est pas bloqué par un ancien mode de saisie.

### Version 0.35.0.9

La définition d’un rappel ramène à un seul écran de tâches, sans listes en double. Fermer un élément retire ses pièces jointes affichées du chat ; rouvrir le même élément réutilise les fichiers déjà affichés.

Les identifiants des résultats de recherche renvoient à l’élément correspondant et chaque ligne reprend l’icône de son en-tête.

Les messages transférés regroupés conservent l’expéditeur de chaque segment. L’IA produit une synthèse unique du texte, de l’OCR et du contenu des pièces jointes compatibles, y compris les informations visuelles. Les paragraphes et les listes sont préservés.

Telegram gère le téléchargement sur votre appareil ; l’aperçu peut rester flou pendant celui-ci. Les fichiers incompatibles ou trop volumineux ne peuvent pas être entièrement analysés.

Ce guide explique comment utiliser Telenota depuis Telegram.

### Dernières mises à jour (0.35.2)

- Les photos et vidéos consécutives d'un même lot capturé sont maintenant affichées comme album Telegram lorsque Telegram autorise ce format.
- L'aperçu du brouillon conserve plus fidèlement les compteurs groupés des pièces jointes ainsi que le texte d'origine, sans répéter plusieurs fois le même segment fusionné.
- Dans les notes, tâches et brouillons, le pied de page est maintenant plus compact : auteur et source sont affichés sur une seule ligne localisée, et l'heure d'enregistrement n'affiche que la date et l'heure locales.
- Lors de l'ouverture d'une note ou d'un brouillon lourd, il n'est plus nécessaire d'attendre le chargement complet de toutes les pièces jointes pour utiliser la carte principale ; les médias continuent de se charger en arrière-plan.
- Les écrans Contacts, Thèmes et Historique des points ont désormais une dernière ligne explicite `Retour` / `Accueil`, et les grands sélecteurs de pages naviguent par fenêtres plutôt que dans une seule grande grille.
- Les lignes de l’Historique des points peuvent maintenant afficher la note ou la tâche liée ainsi qu’un lien profond vers l’élément lorsque le mouvement est rattaché à un élément enregistré qui existe encore.

### Dernières mises à jour (0.36)

- Les notes et tâches prennent maintenant en charge les commentaires. Ouvrez un élément et touchez `Commentaires (N)` pour voir les commentaires existants comme des messages Telegram séparés avec `Commenter` / `Supprimer`.
- Quand le mode commentaire est actif, le texte/média envoyé ou transféré suivant s’affiche d’abord comme aperçu avec `Commenter`, `Créer un brouillon`, `Retour` et `Accueil` ; il n’est enregistré sous l’élément comme `Commentaire N` qu’après confirmation.
- Les brouillons et éléments enregistrés gardent les lignes techniques de transfert plus compactes : `Transféré sans commentaires`, auteur/source et heure d’enregistrement restent ensemble sans lignes vides inutiles.
- Les aperçus de brouillon affichent les compteurs de pièces jointes près de la fin de la carte, au-dessus des métadonnées de transfert/source, et conservent le format Telegram quand c’est possible.
- Lancer `Analyse IA` sur une note ou une tâche déjà enregistrée ajoute désormais le résultat sous le contenu existant, sous l’intitulé `Résultats de l’analyse IA :`, au lieu de remplacer votre contenu enregistré.
- Marquer une tâche comme terminée annule désormais ses rappels programmés, et les suggestions de rappel utilisent votre langue d’interface enregistrée pour reconnaître les mois et jours localisés.
- `Plus` ne contient plus de bouton `Paramètres` en double ; ouvrez les Paramètres depuis l’écran d’accueil.
- `Points` contient un lien direct vers la documentation publique des points.
- Les suggestions de `Fusionner` privilégient maintenant les éléments avec des étiquettes similaires sans IA ; le classement sémantique IA n’est pas activé par défaut, car il ajouterait du coût et de la latence.

### Version 0.36.0.0

Le bonus quotidien est crédité à la première action admissible, pas à minuit. Un nouvel élément ou commentaire, y compris à la clôture d’une tâche, doit dépasser 100 caractères visibles ; partager ou attribuer à autrui n’exige pas de longueur minimale. Pas de second bonus le même jour local ni de recalcul des anciens soldes. Les récompenses d’accueil et de partage restent distinctes.

La recherche affiche tous les résultats par pertinence avec pagination standard. Retour depuis un élément rétablit la requête et la page précédentes sans facturer une nouvelle synthèse IA.

Le son AAC est encapsulé localement en M4A sans réencodage avant transcription. La pièce jointe d’origine reste intacte. Un brouillon sans texte avec un fichier Markdown affiche une description claire et le nombre de documents.

Les boutons d’un brouillon en attente restent sur sa carte principale jusqu’à utilisation, même après l’ouverture d’un autre brouillon. Enregistrer, fermer ou supprimer un élément retire les copies des pièces jointes affichées par le bot, y compris en cours d’envoi ; les messages d’origine sont conservés.

Les sources de sites ne sont pas répétées et les liens du texte restent intacts. Chaque segment transféré affiche « auteur : message », avec un lien vers le message d’origine si Telegram le fournit ; les transferts privés ou masqués peuvent ne pas l’exposer. Les liens des paragraphes numérotés sont préservés. Les anciens brouillons ne sont pas réécrits en masse.

### Version 0.36.0.1

Les pièces jointes et messages transférés créent un nouveau brouillon au lieu d’être interprétés comme une date de rappel, même si le récapitulatif du soir attend une réponse. Une suggestion de rappel n’active pas la saisie d’une date ; ouvrez explicitement Rappel pour en saisir une.

Les actions Note avec IA et Tâche avec IA sont toujours affichées dans les brouillons nouveaux ou rouverts, y compris ceux contenant uniquement du texte. L’accès à l’IA et le solde sont vérifiés au clic ; l’enregistrement normal reste disponible.

Dans la suggestion d’envoyer ou d’attribuer une entrée aux personnes mentionnées, Retour ferme uniquement la suggestion et conserve l’écran, la page et les pièces jointes précédents. Revenir à l’entrée reste une action distincte.

### Dernières mises à jour (0.36.2.phase4-5)

- L’aperçu du brouillon peut afficher un interrupteur de traduction rouge/vert avant l’enregistrement. Rouge conserve la langue d’origine ; vert traduit le brouillon dans la langue de votre interface lors d’un enregistrement normal en note ou tâche.
- Les résumés IA des notes et tâches utilisent désormais la langue d’interface choisie, même si le texte source est dans une autre langue.
- Les messages transférés rapidement sont fusionnés dans leur ordre d’arrivée.
- Les écrans de fusion ouverts depuis des messages avec média utilisent maintenant un repli sûr au lieu d’afficher une erreur d’édition Telegram.
- Les albums transférés sont désormais enregistrés de manière sérialisée afin de conserver chaque image, vidéo et légende dans l’ordre d’origine. Les sondages transférés conservent un instantané textuel de leurs options et résultats disponibles ; sans résultat, une note demande de voter dans le sondage d’origine.
- Pour les lignes d’adresse explicites, le bot peut proposer des correspondances précises OpenStreetMap. Elles ne sont ajoutées comme commentaires de localisation qu’après confirmation lors de l’enregistrement d’une note ou tâche.

### Dernières mises à jour (0.36.4)

- Les commentaires conservent la mise en forme Telegram et utilisent `Enregistrer`, `❌ Supprimer` et `Retour` ; revenir ou supprimer efface aussi l’ancien écran des commentaires.
- Les instantanés de sondage affichent les votes par option et le total uniquement lorsque Telegram les fournit. Sinon, Telenota indique clairement que les résultats sont inconnus et n’invente jamais de votes à zéro.
- Les adresses explicites sont détectées dans les messages directs et transférés, y compris avec des abréviations de rue multilingues. Seule l’adresse candidate extraite est envoyée à OpenStreetMap et les correspondances ambiguës ne sont pas ajoutées.
- Dans un bloc de coordonnées, `Контакты: av. Aragon nº4-bis` devient l’adresse `Avenida Aragon, 4-bis`. Les abréviations de voie et les indicateurs de numéro espagnols sont normalisés sans perdre `-bis` ni les suffixes alphabétiques. Les téléphones, courriels et liens voisins sont exclus de la requête. La ville explicitement indiquée est conservée ; aucune ville ni position approximative n’est inventée.

### Version 0.37.0.0

L’export calendrier apparaît dans la fiche si une date ou une heure est détectée, et reste toujours disponible dans Plus. Le libellé du bouton ne contient pas de prix ; l’export coûte 0,10 point. Un appui envoie directement un fichier d’événement .ics, sans aperçu intermédiaire dans le bot, ainsi qu’un lien Google Agenda de secours. Ouvrez le fichier dans votre calendrier et confirmez l’importation ; Telegram ou le système peut demander de choisir une application. L’ouverture automatique du calendrier par défaut n’est garantie ni sur iOS, ni sur Android, ni sur ordinateur.

Si Telegram ne confirme pas l’envoi de l’ICS, le bot envoie un message distinct avec le lien Google Agenda prérempli. La confirmation correspond à un identifiant de message et de fichier renvoyé par Telegram, pas au téléchargement ou à l’importation sur l’appareil. Le lien ne nécessite pas de connexion OAuth au bot.

Une date seule crée un événement sur toute la journée ; une heure seule utilise aujourd’hui dans votre fuseau enregistré, même si l’heure est passée. Une date et une heure utilisent le moment indiqué. La durée par défaut est de 60 minutes. Le titre commence par l’icône de note/tâche et reprend le titre de la fiche ; la description contient un lien vers celle-ci dans le bot, sans son texte privé. Si la date manque, est invalide ou ambiguë, Plus demande une seule date/heure de début ; Retour annule, les fichiers et transferts créent un nouveau brouillon.

Un seul envoi réussi du même événement est facturé par utilisateur. Le récupérer à nouveau est gratuit, même après un redémarrage du bot ; les échecs d’envoi sont remboursés. Changer le titre, la date ou l’heure produit un nouvel événement. Le bot ne confirme pas l’enregistrement dans le calendrier. Réimporter peut créer des doublons ; les modifications ultérieures ne sont pas synchronisées. Le fichier disparaît du chat à la fermeture des pièces jointes de la fiche. Aucun compte calendrier ni analyse IA payante n’est requis.

La lecture audio conserve les liens de l’auteur et de la source, y compris après conversion d’une note en tâche ou inversement. Les liens sans schéma, comme Tambur.pub, s’ouvrent en HTTPS au lieu de s’afficher en Markdown.

La durée de l’audio généré est mesurée et conservée à la réouverture de l’entrée. Relancer la lecture du même texte avec la même voix et le même modèle réutilise le fichier enregistré, sans nouvelle facturation de génération IA ni pièce jointe en double. Modifier le texte lu crée une nouvelle version. Les anciens fichiers audio d’origine indéterminée ne sont pas supprimés automatiquement.

### Version 0.37.0.1

Les boutons du calendrier répondent désormais correctement, sans prix dans leur libellé. Si l’envoi ICS n’est pas confirmé, le bot fournit un lien Google Agenda distinct dans le cadre du même export à 0,10 point. Les adresses comme `av. Aragon nº4-bis` conservent le numéro du bâtiment ; téléphone et e-mail sont exclus de la recherche. Aucune connexion de compte Google n’est nécessaire.

### Version 0.37.0.3 — bonus et messages système

Une journée locale active rapporte 0,50 point ; les trois jours suivants sans activité admissible, 0,30, 0,15 et 0,05. Au quatrième jour, les bonus s’arrêtent avec une notification. Créer une note ou un commentaire de plus de 100 caractères visibles, partager ou attribuer une note à une autre personne constitue une activité ; consulter, modifier ou recevoir une copie ne compte pas. Après un bonus d’inactivité, l’activité complète seulement le total journalier à 0,50. Aucun rattrapage ni recalcul historique. Le traitement intervient pendant la première heure locale ; une panne peut retarder ou empêcher la notification du jour.

Paramètres → Masquer les messages système : 5, 10 ou 30 secondes, 1 minute ou Jamais ; 30 secondes par défaut. Cela concerne les nouveaux avis temporaires, pas le nettoyage de navigation ni la synchronisation technique du clavier. Les boutons des brouillons en attente restent jusqu’à une action. Google OAuth est reporté ; ICS et les liens Google restent à 0,10 point, sans prix sur le bouton.

### Corrections de la version 0.37.0.3

Les confirmations de création utilisent des espaces ordinaires, sans retour à la ligne forcé. Telegram et le système d’exploitation déterminent l’affichage final de la notification.

Dans la proposition de partage d’une note, Partager et Ouvrir la note figurent sur la même ligne ; Retour reste séparé et ferme uniquement la proposition. Commentaires et Calendrier partagent une ligne lorsque le calendrier est disponible.

Le brouillon conserve le lien d’origine avant la fin du résumé. L’enregistrement d’un résumé de secours conserve sa source. Les nouveaux débits d’enrichissement IA et reçus d’export gardent la référence de la note pour les liens de l’historique ; les anciennes références manquantes ne sont ni devinées ni réécrites.

Une expression telle que «сегодня в 19» contient une heure, pas seulement une date. Un lien de visioconférence pris en charge est exporté comme lieu dans ICS et Google. La convention régionale configurable CET/CEST utilise Europe/Madrid avec l’heure d’été, et non un décalage fixe UTC+01:00. Plusieurs lieux distincts nécessitent une précision.

### Version 0.38.0.0 — rappels et fusion fiables

Les dates comme « 28.10 » sont reconnues séparément du résumé ; un rappel facultatif est conservé en UTC. Les tâches dont la date et l’heure futures sont reconnues reçoivent un rappel. Une date seule utilise l’heure enregistrée du récapitulatif quotidien des tâches ; à défaut, choisissez une heure. Les anciens éléments ne sont pas reprogrammés automatiquement.

Les suggestions de fusion privilégient les thèmes communs, puis la pertinence du texte, sans éléments archivés. L’identifiant et le titre de la destination sont conservés et les textes complets sont concaténés sans réécriture par l’IA. Les pièces jointes distinctes et les rappels programmés sont conservés. L’original est archivé pour récupération ; ses commentaires y restent.

Les titres des résumés et du texte extrait sont en gras ; les sections d’analyse strictement identiques sont omises. Le titre de la note courte n’affiche plus la limite de mots. Les traits de soulignement des identifiants sont préservés. La proposition de partage présente une seule action pour ouvrir l’élément, sans commandes de retour en double. Les confirmations de création n’ajoutent plus d’espacement invisible ; l’appareil gère la mise en page des notifications natives.

Les montants des bonus restent inchangés. Les nouvelles tentatives de notification persistent sans recréditer le solde. Google OAuth reste reporté. L’acceptation d’une pièce jointe par Telegram ne confirme pas son téléchargement sur l’appareil ; les lenteurs des images restent à l’étude.

### 0.39.0.0

La recherche locale, la pagination et le retour aux résultats sont gratuits. Répondre avec l’IA demande explicitement une réponse payante, sans prix sur le bouton. Les réponses inchangées sont réutilisées dans la session.

GPT-Transcribe reconnaît la parole. Une étape de mise en forme conserve les tours de dialogue seulement avec des indices explicites ; elle n’identifie pas les personnes par leur voix. Résumé, titre et métadonnées réutilisent une analyse commune.

Avant une analyse vidéo en plusieurs étapes, le bot réserve le coût total. Si le résultat complet ne peut pas être fourni, la réservation est remboursée ; une vidéo sans son exploitable peut être analysée visuellement sans facturer la transcription échouée.

### 0.39.0.1

L’export ICS est conservé ; le lien Google utilise le point d’entrée testé sur mobile et ordinateur. Confirmez et enregistrez l’événement dans le calendrier. La recherche locale pondère les mots-clés sans IA ni frais supplémentaires. Les listes actives excluent les tâches terminées sans supprimer les fiches conservées. Les erreurs proposent Retour et Accueil. Les résultats de liens en attente utilisent la langue d’interface actuellement enregistrée ; le titre et la description disponibles servent de solution de repli, mais les pages restreintes peuvent rester inaccessibles. Les lenteurs de chargement des photos restent à l’étude ; les photos ne sont ni converties en fichiers ni recompressées.
