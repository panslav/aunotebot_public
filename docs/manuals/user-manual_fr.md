# Guide utilisateur AUNotebot

## 1. Démarrage
1. Ouvrez le chat du bot.
2. Envoyez `/start`.
3. Écran d’accueil: `Trouver`, `Tâches`, `Notes`, `Rappels`, `Brouillons`, `Plus`.

## 2. Langue
- Menu: `More -> Settings -> Langue`.
- Langues prises en charge: English, Русский, Українська, Español, Português, Français.

## 2a. Points IA et Telegram Stars
- Les actions IA utilisent votre solde de points.
- Modèle par défaut :
  - `1 point = 1 Telegram Star`
  - `50 points gratuits` au premier lancement
  - `5 points gratuits` chaque jour à `00:00` dans votre fuseau horaire local
  - `0,1 point = 1 action IA`
- Ouvrez `More -> Points` pour voir votre solde, vérifier le coût actuel, consulter vos 5 dernières opérations de points, ouvrir l’`Historique complet des points` et recharger avec Telegram Stars.
- Si le solde est insuffisant, l’action IA est bloquée, mais les fonctions non-IA continuent de fonctionner.

## 3. Créer une note
1. Envoyez texte/voix/vidéo/image.
2. Le bot crée un brouillon.
3. Appuyez sur `📝 Enregistrer comme note`.

## 4. Créer une tâche
- Depuis un brouillon: `🟧 Save as Task`.
- Ou depuis une note: `⬛ Make Task`.

## 5. Transférer des messages
- Plusieurs messages transférés en une seule action sont fusionnés dans un brouillon.
- Le délai de fusion se règle dans `More -> Settings -> Délai de fusion des messages multiples`.
- Des hashtags envoyés séparément sont ajoutés aux tags du brouillon.

## 6. Recherche et Rappel
- `🔎 Find` active le mode interactif.
- Envoyez votre demande en texte libre.
- Le bot renvoie un résumé et des boutons d’éléments pertinents.

## 7. Actions sur un élément
### Note
- `✏️ Edit`, `🏷️ Tags`, `⬛ Make Task`, `❌ Remove`, `⬅️ Back`

### Tâche
- `✏️ Edit`, `✅ Done/🔄 Re-do`, `⏰ Reminder`, `🏷️ Tags`, `🔁 Make Note`, `🔀 Merge`, `👥 Assign`, `❌ Remove`, `⬅️ Back`

## 8. Tags et sujets
- `Tags` ouvre les tags de l’élément.
- En cliquant sur un tag, vous ouvrez la liste des éléments liés.
- Menu sujet: `Edit` et `Delete`.

## 9. Rappels
- Dans une tâche, cliquez `⏰ Reminder`.
- Saisissez date/heure en format libre (ex.: «demain 9:00»).

## 10. Paramètres
`More -> Settings`:
- Langue
- Fuseau horaire
- Marquer comme fait
- Copier le texte pour édition
- Résumé quotidien des tâches
- Résumé du soir
- Délai de fusion des messages multiples
- Nombre d'éléments
- Afficher le menu du bas

## 11. Aide et légal
- `More -> Help` ouvre ce guide sur le web.
- `More -> Legal` ouvre les Terms & Conditions dans votre langue courante.

## 12. Contact
- Idées et retours: `@aunotebot_support`

## Documents liés
- Conditions générales : [Legal docs repository](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Flux d'écrans : [Screenflow](/docs/Screenflow.md)
- Installation : [Installation](/docs/installation.md)
