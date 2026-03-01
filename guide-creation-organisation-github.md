# Guide : Créer une Organisation GitHub

## Étapes de création

### 1. Créer l'organisation

1. Connectez-vous à GitHub
2. Cliquez sur votre avatar en haut à droite
3. Sélectionnez "Your organizations" / "Vos organisations"
4. Cliquez sur "New organization" / "Nouvelle organisation"
5. Choisissez le plan (Free suffit)
6. Remplissez les informations :
   - Nom de l'organisation (unique, visible publiquement)
   - Email de contact
   - Appartenance (Personal account)

### 2. Configuration initiale

**Paramètres de base** (Settings / Paramètres > General / Général)

- Description de l'organisation
- URL du site web
- Avatar de l'organisation

**Permissions des membres** (Settings / Paramètres > Member privileges / Privilèges des membres)

- Base permissions : définir les droits par défaut (Read / Lecture, Write / Écriture, Admin / Administrateur)
- Repository creation : autoriser ou non les membres à créer des repos
- Repository forking : autoriser le fork de repos privés

### 3. Gérer les membres

**Inviter des membres** (People / Personnes > Invite member / Inviter un membre)

- Entrez le username ou email GitHub
- Assignez un rôle : Member / Membre ou Owner / Propriétaire

**Rôles disponibles**

- Owner / Propriétaire : contrôle total sur l'organisation
- Member / Membre : accès selon les permissions définies
- Billing manager / Gestionnaire de facturation : gestion de la facturation uniquement

### 4. Créer des équipes (optionnel mais recommandé)

1. Allez dans Teams / Équipes > New team / Nouvelle équipe
2. Nommez l'équipe (ex: "Frontend", "Backend", "DevOps")
3. Définissez la visibilité (Visible ou Secret)
4. Ajoutez des membres à l'équipe
5. Assignez l'équipe à des repositories avec des permissions spécifiques

### 5. Créer ou transférer des repositories

**Nouveau repository**

- Cliquez sur "New" / "Nouveau" depuis la page de l'organisation
- Le processus est identique à un repo personnel

**Transférer un repo existant**

1. Allez dans le repo personnel > Settings / Paramètres
2. Scrollez jusqu'à "Danger Zone" / "Zone de danger"
3. Cliquez sur "Transfer ownership" / "Transférer la propriété"
4. Entrez le nom de l'organisation

## Bonnes pratiques

**Structure des équipes**

- Créez des équipes par projet ou par compétence
- Utilisez des équipes imbriquées pour les grandes structures

**Gestion des permissions**

- Principe du moindre privilège : donnez le minimum de droits nécessaires
- Utilisez les équipes plutôt que d'assigner les permissions individuellement

**Documentation**

- Créez un repository .github avec des templates (ISSUE_TEMPLATE, PULL_REQUEST_TEMPLATE)
- Ajoutez un README.md dans le profil de l'organisation (repo nommé `.github` avec un `profile/README.md`)

**Naming conventions**

- Établissez des conventions de nommage pour les repos
- Utilisez des topics pour catégoriser vos repositories

## Commandes utiles

```bash
# Cloner un repo d'organisation
git clone https://github.com/nom-organisation/nom-repo.git

# Ajouter l'organisation comme remote
git remote add org https://github.com/nom-organisation/nom-repo.git

# Configurer l'email pour commits d'organisation
git config user.email "votre-email@organisation.com"
```

## Points d'attention

- Une fois le nom choisi, il est difficile de le changer (possible mais peut casser des liens)
- Les repositories transférés conservent leur historique git complet
- Les members ne peuvent pas voir les repos privés sauf si explicitement ajoutés
