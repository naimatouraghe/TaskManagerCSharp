# Task Manager

**Enoncé : Application complète de gestion des tâches**

**Description :** Vous devez créer une application de gestion des tâches qui permettra aux utilisateurs de créer, afficher, mettre à jour et supprimer des tâches. L'application devra être implémentée en utilisant du pseudo-code et JavaScript.

**Fonctionnalités attendues :**

1. Ajouter une nouvelle tâche avec un titre, une description et une date d'échéance.
2. Afficher la liste de toutes les tâches avec leurs détails.
3. Marquer une tâche comme terminée.
4. Mettre à jour les détails d'une tâche existante.
5. Supprimer une tâche de la liste.

**Pseud-code**

```
TANT QUE vrai
    AFFICHER "Menu Principal :"
    AFFICHER "1. Créer une nouvelle tâche"
    AFFICHER "2. Afficher la liste des tâches"
    AFFICHER "3. Mettre à jour une tâche"
    AFFICHER "4. Marquer une tâche comme terminée"
    AFFICHER "5. Supprimer une tâche"
    AFFICHER "6. Quitter"
    LIRE choixUtilisateur

    SI choixUtilisateur = 1 ALORS
        AFFICHER "Titre de la tâche :"
        LIRE titre
        AFFICHER "Description de la tâche :"
        LIRE description
        AFFICHER "Date d'échéance de la tâche :"
        LIRE dateEcheance
        CréerTache(titre, description, dateEcheance)

    SINON SI choixUtilisateur = 2 ALORS
        AfficherListeTaches()

    SINON SI choixUtilisateur = 3 ALORS
        AFFICHER "Indice de la tâche à mettre à jour :"
        LIRE indice
        AFFICHER "Nouveaux détails de la tâche :"
        LIRE nouveauxTitre, nouvelleDescription, nouvelleDateEcheance
        MettreAJourTache(indice, nouveauxTitre, nouvelleDescription, nouvelleDateEcheance)

    SINON SI choixUtilisateur = 4 ALORS
        AFFICHER "Indice de la tâche à marquer comme terminée :"
        LIRE indice
        MarquerTacheTerminee(indice)

    SINON SI choixUtilisateur = 5 ALORS
        AFFICHER "Indice de la tâche à supprimer :"
        LIRE indice
        SupprimerTache(indice)

    SINON SI choixUtilisateur = 6 ALORS
        QUITTER

    FIN SI

FIN TANT QUE

Fonction CréerTache(titre, description, dateEcheance)
    Créer une nouvelle tâche avec les détails fournis
    Ajouter la tâche à la liste des tâches

Fonction AfficherListeTaches()
    POUR CHAQUE tâche DANS listeDesTaches
        AFFICHER "Tâche : ", tâche.titre
        AFFICHER "Description : ", tâche.description
        AFFICHER "Date d'échéance : ", tâche.dateEcheance
        AFFICHER "Terminée : ", tâche.terminee
        AFFICHER "----------------------"
    FIN POUR

Fonction MettreAJourTache(indice, nouveauxTitre, nouvelleDescription, nouvelleDateEcheance)
    SI indice est un indice valide DANS listeDesTaches
        Mettre à jour les détails de la tâche à l'indice avec les nouveaux détails fournis
    FIN SI

Fonction MarquerTacheTerminee(indice)
    SI indice est un indice valide DANS listeDesTaches
        Marquer la tâche à l'indice comme terminée
    FIN SI

Fonction SupprimerTache(indice)
    SI indice est un indice valide DANS listeDesTaches
        Supprimer la tâche à l'indice de la liste des tâches
    FIN SI

```
