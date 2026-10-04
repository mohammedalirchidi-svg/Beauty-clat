# L’Institut Éclat — site web

Site de L’Institut Éclat (institut de beauté à Orléans), conçu avec Claude Design.
C’est un site statique : il s’héberge tel quel, sans installation ni étape de construction.

**En ligne :** https://mohammedalirchidi-svg.github.io/Beauty-clat/

## Publier sur Netlify à l’adresse institut-eclat.netlify.app

1. Créez un compte gratuit sur <https://app.netlify.com/signup> avec **« Sign up with GitHub »**.
2. Cliquez sur **Add new project** (ou « Add new site ») **→ Import an existing project → GitHub**, puis
   choisissez le dépôt **Beauty-clat**.
3. Ne changez aucun réglage et cliquez sur **Deploy**.
4. Dans **Project configuration → Change project name** (ou « Site configuration → Change site name »),
   tapez `institut-eclat` et enregistrez. Si ce nom est déjà pris, essayez par exemple `institut-eclat-orleans`.

Le site est alors en ligne sur **https://institut-eclat.netlify.app**. Il se met à jour tout seul
à chaque modification de ce dépôt.

## Contenu

| Fichier | Rôle |
| --- | --- |
| `index.html` | la page : textes, soins, tarifs, avis, horaires, coordonnées et réservation |
| `assets/img/` | les photos |
| `assets/fonts/`, `assets/js/` | polices et scripts du site |
| `og-image.jpg` | l’aperçu affiché quand le lien est partagé (WhatsApp, Instagram, SMS…) |
| `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` | icônes de l’onglet et de l’écran d’accueil |

## Réception des demandes de rendez-vous

Quand un client envoie le formulaire « Choisissez votre moment », sa demande (soins, date, heure,
nom, téléphone) s’ouvre toute prête dans son application e-mail, adressée à l’institut. Ce réglage
se trouve dans `index.html` :

```js
static CONTACT = { whatsapp: '', email: 'contact@institut-eclat.fr' };
```

Si un numéro WhatsApp est renseigné (format international sans « + » ni espaces, par exemple
`33612345678`), la demande s’ouvre dans WhatsApp à la place de l’e-mail.
