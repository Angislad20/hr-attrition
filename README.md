## Présentation

Ce dataset contient des informations relatives aux employés d'une organisation et vise à permettre l'analyse des facteurs associés à la **rétention ou au départ des employés** (*Employee Attrition*).

Le dataset contient **1 470 observations et 35 variables**. Chaque ligne correspond à un employé.

L'objectif principal de notre analyse est d'étudier les caractéristiques des employés et leur relation avec la variable cible `Attrition`, afin d'identifier les facteurs potentiellement associés au départ des employés et, par la suite, de construire un modèle de prédiction.

## Variable cible

La variable cible est :

* `Attrition` : indique si l'employé a quitté l'organisation (`Yes`) ou non (`No`).

Il s'agit donc d'un problème de **classification binaire**.

## Types de variables

Les 35 variables ne doivent pas être classées uniquement selon leur type technique (`int64`, `object`, etc.).

Certaines variables stockées sous forme numérique représentent en réalité des **catégories ordonnées**, par exemple :

* `Education`
* `EnvironmentSatisfaction`
* `JobInvolvement`
* `JobLevel`
* `JobSatisfaction`
* `PerformanceRating`
* `RelationshipSatisfaction`
* `StockOptionLevel`
* `WorkLifeBalance`

À l'inverse, certaines variables numériques représentent réellement des quantités, notamment des âges, revenus, distances ou nombres de formations.

Cette distinction sera donc effectuée à partir de la **signification des variables** et non uniquement de leur type Python.

## Structure générale des variables

Les variables couvrent plusieurs dimensions du profil des employés :

### Informations personnelles

* `Age`
* `Gender`
* `MaritalStatus`
* `Education`
* `EducationField`

### Informations professionnelles

* `Department`
* `JobRole`
* `JobLevel`
* `BusinessTravel`
* `OverTime`
* `YearsAtCompany`
* `YearsInCurrentRole`
* `YearsWithCurrManager`

### Rémunération et carrière

* `DailyRate`
* `HourlyRate`
* `MonthlyIncome`
* `MonthlyRate`
* `PercentSalaryHike`
* `StockOptionLevel`
* `TotalWorkingYears`
* `NumCompaniesWorked`

### Satisfaction et environnement de travail

* `EnvironmentSatisfaction`
* `JobInvolvement`
* `JobSatisfaction`
* `RelationshipSatisfaction`
* `WorkLifeBalance`
* `PerformanceRating`

### Formation

* `TrainingTimesLastYear`

### Variables techniques / administratives

* `EmployeeNumber`
* `EmployeeCount`
* `StandardHours`
* `Over18`

## Limites de la documentation

La documentation fournie avec le dataset étant relativement limitée, certaines variables codées numériquement ne peuvent pas être interprétées correctement à partir du fichier CSV seul.

Par exemple, une colonne contenant les valeurs `1, 2, 3, 4` peut représenter :

* une véritable mesure numérique ;
* des catégories nominales codées par des nombres ;
* des catégories ordinales représentant différents niveaux.

L'interprétation de ces variables nécessite donc de s'appuyer sur la description disponible du dataset et sur leur signification métier.

Cette étape de documentation et de classification des variables constitue une étape préalable à l'analyse exploratoire des données (EDA).

## Approche retenue

L'analyse suivra donc les étapes suivantes :

1. Inspection générale du dataset ;
2. Documentation et classification des variables ;
3. Identification des identifiants et variables constantes ;
4. Analyse univariée ;
5. Analyse bivariée avec `Attrition` ;
6. Identification des variables potentiellement informatives ;
7. Préparation des données pour la modélisation.

