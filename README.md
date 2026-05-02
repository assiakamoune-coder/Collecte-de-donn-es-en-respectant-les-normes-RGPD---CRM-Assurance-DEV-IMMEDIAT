# Collecte-de-donn-es-en-respectant-les-normes-RGPD---CRM-Assurance-DEV-IMMEDIAT
Ce projet documente les démarches entreprises pour assurer la conformité du système CRM avec le Règlement Général sur la Protection des Données (RGPD). Il répond spécifiquement à une sanction de la CNIL imposant une limitation temporaire des traitements en garantissant l'anonymisation des données personnelles pour l'analyse commerciale.

# 🛡️ Projet de Mise en Conformité RGPD & Business Intelligence
**Optimisation d'un CRM Assurance : de la donnée brute à l'insight sécurisé**

## 📖 Contexte & Problématique
Dans le cadre d'une mise en demeure de la CNIL, l'entreprise a dû suspendre l'exploitation de son CRM pour non-conformité. Mon rôle a été de concevoir et d'exécuter une stratégie de **Data Cleaning** et d'**Anonymisation** permettant de lever les restrictions légales tout en conservant la valeur statistique des données pour la direction commerciale.

## Objectifs et enjeux:
Ce projetprésente les démarches pour assurer la conformité du système CRM avec le Règlement Général sur la Protection des Données (RGPD) et pour répondre à la sanction de la CNIL imposant une limitation temporaire des traitements. L’objectif est de documenter le processus d’anonymisation des données personnelles, tout en garantissant la continuité d’exploitation à des fins d’analyse statistique et commerciale.
Les enjeux sont à la fois juridiques (éviter toute nouvelle sanction), techniques (sécurisation des données) et organisationnels (instauration d’une culture de conformité). Ce rapport s’adresse à la Direction, au DPO, aux responsables de traitement, ainsi qu’à la CNIL dans le cadre d’une demande de levée de sanction.

## 🚀 Compétences Clés Mobilisées
### ⚖️ Gouvernance et Juridique
* **Analyse d'Impact (PIA) :** Identification des données à caractère personnel (DCP) et des risques associés.
* **Privacy by Design :** Intégration des contraintes légales dès l'amont du traitement technique.
* **Définition de Politiques de Rétention :** Établissement de règles de purge automatique (3 ans prospects / 5 ans clients).

### ⚙️ Expertise Technique (Stack : SQL & Power Query)
* **Ingénierie de la donnée :** Extraction ciblée en SQL pour limiter le volume de données traitées (Minimisation).
* **Data Transformation :** Maîtrise avancée des fonctions de regroupement, de calcul de tranches et de masquage sous Power Query.
* **Gestion de l'Intégrité :** Création de clés d'indexation anonymes pour préserver les relations entre tables sans identifier les individus.

## 🛠️ Détail du Workflow Technique

### 1. Phase d'Extraction (Filtrage SQL)
Plutôt que d'extraire toute la base, j'ai conçu une requête optimisée :
- **Exclusion native** des colonnes sensibles (noms, téléphones, adresses IP).
- **Filtrage temporel** sur l'exercice 2022 pour répondre au périmètre exact de l'audit.

### 2. Phase de Transformation (Anonymisation irréversible)
| Donnée Initiale | Risque | Solution Appliquée | Valeur Métier Conservée |
| :--- | :--- | :--- | :--- |
| `Date_Naissance` | Identifiant indirect | Conversion en `Tranche_Age` | Segmentation marketing (Senior/Junior) |
| `Nombre_Enfants` | Donnée sensible | Pivot vers `Profil_Familial` (Oui/Non) | Ciblage des offres "Famille" |
| `Revenus_Exacts` | Vie privée | Création de `Clusters_Revenus` | Analyse du pouvoir d'achat |
| `Adresse_Postale` | Localisation exacte | Extraction du `Code_Departement` | Analyse géographique des sinistres |

## 📂 Livrables Stratégiques
Cliquez sur les liens pour accéder aux détails de mon travail :

* [📄 **Rapport de Conformité (PDF)**](./Kamoune_Assia_3_rapport_102025.pdf) : Analyse complète de la méthodologie et justification des choix techniques face aux exigences CNIL.
* [📋 **Audit & Préconisations (PDF)**](./Kamoune_Assia_1_recommandations_102025.pdf) : Plan d'action pour la direction (rôles d'accès, registre de traitements, sécurité SI).
* [📊 **Base de Données Cleanée (Excel)**](./Kamoune_Assia_2_donnees_102025.xlsx) : Le résultat final. Une base 100% anonyme, prête pour Power BI ou Tableau.
* [🖥️ **Présentation (PPTX)**](./Collecte%20de%20donn閖es%20en%20respectant%20les%20normes%20RGPD.pptx) : Synthèse visuelle des résultats pour le comité de direction.

## 💡 Ma Valeur Ajoutée sur ce Projet
Au-delà de l'aspect technique, j'ai apporté une vision **orientée solution** :
1. **Zéro perte de valeur** : Malgré l'anonymisation, les indicateurs de performance (KPI) restent calculables à 100%.
2. **Sécurisation juridique** : Le protocole mis en place permet de lever la sanction CNIL et de reprendre les activités marketing immédiatement.
3. **Pérennité** : Les scripts SQL et les étapes Power Query sont documentés pour être réutilisés lors des prochains audits.

