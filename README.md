# Telco Customer Churn Analysis

Analyse exploratoire du churn client dans un contexte télécom, avec identification d'un segment prioritaire de rétention.

## Objectif

Ce projet vise à comprendre pourquoi les clients abandonnent un opérateur et à repérer les profils les plus exposés au churn afin de guider des actions de fidélisation.

L'approche suit un parcours Data Analyst complet :

Python → SQL → Power BI → Business Insights

> L'analyse est descriptive et orientée business : elle met en évidence des associations entre caractéristiques clients et churn, sans établir de causalité.

---

## Contexte métier

Le secteur des télécommunications est très concurrentiel, et la fidélisation est un enjeu majeur pour la rentabilité. En analysant les données clients, il est possible d'identifier les signaux qui augmentent le risque de départ et de cibler les actions de rétention de manière plus efficace.

---

## Dataset

Le projet utilise le dataset Telco Customer Churn, accessible sur Kaggle :
https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data

Données principales :
- 7 043 clients
- 21 variables
- variable cible : Churn

Variables clés :
- customerID
- tenure
- MonthlyCharges
- TotalCharges
- Contract
- InternetService
- TechSupport
- PaymentMethod
- Churn

Le jeu de données brut n'est pas inclus dans le dépôt, mais la source est indiquée pour le récupérer facilement.

---

## Structure du repository

- Exploratory_data_analysis.ipynb : analyse exploratoire avec Python
- SQL_analysis : requêtes SQL et analyse métier
- Dashboard.pbix : tableau de bord Power BI
- README.md : documentation du projet

---

## Démarche analytique

### 1. Exploration Python

Le notebook comprend :
- contrôle de la qualité des données
- vérification des valeurs manquantes et doublons
- transformation des formats
- analyse descriptive des variables
- calcul du taux global de churn
- premiers indicateurs métier

### 2. Analyse SQL

L'analyse SQL approfondit les hypothèses issues de Python :
- churn par type de contrat
- churn par ancienneté
- churn selon les montants mensuels
- impact du service Internet
- impact du support technique
- identification d'un segment prioritaire

### 3. Visualisation Power BI

Le dashboard permet de présenter les résultats de manière claire et exploitable pour la prise de décision.

---

## Principaux résultats

Taux global de churn : 26,54 %

Les signaux les plus marquants sont :
- les clients en contrat Month-to-month présentent un churn de 42,71 %
- les clients avec 0 à 6 mois d'ancienneté affichent un churn proche de 53 %
- le support technique absent est fortement associé au churn
- le service Internet Fiber optic est plus exposé au départ

---

## Segment prioritaire identifé

Le profil le plus risqué est :
- contrat Month-to-month
- service Internet Fiber optic
- pas de TechSupport

Ce segment représente :
- 1 796 clients
- 1 033 churners
- taux de churn : 57,52 %
- 55,27 % de l'ensemble des churners

Ce segment concentre donc plus d'un churner sur deux dans le dataset.

---

## Impact business

Le segment prioritaire représente également une exposition mensuelle importante :
- environ 88 165,75 € de facturation mensuelle associée aux churners

Cette mesure est utile pour hiérarchiser les actions de rétention, même si elle ne représente pas une perte de CA directement démontrée.

---

## Pistes de rétention

Les actions les plus pertinentes à tester sont :
- encourager les contrats longue durée
- surveiller les nouveaux clients en contrat Month-to-month
- renforcer l'accompagnement des clients Fiber
- cibler les clients sans support technique

---

## Stack technique

- Python : pandas, NumPy, Matplotlib, Seaborn
- SQL : Microsoft SQL Server, CTE, agrégations, CASE WHEN, GROUP BY
- Power BI : visualisation, KPI, segmentation, storytelling analytique
- GitHub : gestion de version et documentation

---

## Limites

Cette analyse est utile pour identifier des profils et des tendances, mais elle ne doit pas être interprétée comme un modèle de prédiction complet. Les résultats montrent des associations, pas des causes directes, et les actions de rétention doivent être validées avec des données complémentaires et des tests métier.

---

## À propos

Projet réalisé dans le cadre d'une démarche de portfolio Data Analyst, combinant analyse exploratoire, SQL, segmentation client et visualisation business.

Compétences mobilisées :
- data cleaning
- analyse exploratoire
- SQL
- segmentation client
- KPI et reporting
- Power BI
- storytelling analytique

