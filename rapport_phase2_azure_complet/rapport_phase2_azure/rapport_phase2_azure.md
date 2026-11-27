# Phase 2 — Mise en place du pipeline Azure

Captures d’écran des principales étapes réalisées durant la deuxième phase du projet de prévision de la consommation électrique.

## 1. Création du compte de stockage Azure `stbriefforecast2026` dans la région North Europe.

![01_creation_storage_account.png](images/01_creation_storage_account.png)

## 2. Création des conteneurs `source` et `datalake` pour organiser les données du projet.

![02_storage_containers.png](images/02_storage_containers.png)

## 3. Chargement du fichier source `PJME_hourly.csv` dans le conteneur `source`.

![03_upload_source_csv.png](images/03_upload_source_csv.png)

## 4. Ouverture d'Azure Data Factory Studio à partir de l'instance `adf-brief-forecast-2026`.

![04_open_data_factory_studio.png](images/04_open_data_factory_studio.png)

## 5. Création du service lié permettant à Data Factory d'accéder à Azure Data Lake Storage Gen2.

![05_create_adls_linked_service.png](images/05_create_adls_linked_service.png)

## 6. Configuration du dataset CSV `ds_raw_csv`, associé au conteneur de destination `datalake`.

![06_configure_raw_dataset.png](images/06_configure_raw_dataset.png)

## 7. Construction du pipeline `pl_ingest_raw` avec les activités de vérification et de copie du fichier.

![07_build_ingestion_pipeline.png](images/07_build_ingestion_pipeline.png)

## 8. Exécution du pipeline d'ingestion et consultation du statut des activités dans l'onglet Sortie.

![08_run_adf_pipeline.png](images/08_run_adf_pipeline.png)

## 9. Vérification de la présence de `PJME_hourly.csv` dans le dossier `datalake/raw`.

![09_verify_raw_csv_in_datalake.png](images/09_verify_raw_csv_in_datalake.png)

## 10. Création de l'espace de travail Azure Machine Learning `ml-brief-forecast-2026`.

![10_create_azure_ml_workspace.png](images/10_create_azure_ml_workspace.png)

## 11. Ajout des composants de préparation et d'analyse des données dans Azure ML Designer.

![11_add_ml_designer_components.png](images/11_add_ml_designer_components.png)

## 12. Organisation du workflow de séparation des données, d'entraînement et d'évaluation du modèle.

![12_configure_training_workflow.png](images/12_configure_training_workflow.png)

## 13. Consultation de l'exécution du pipeline Machine Learning dans la section Jobs.

![13_inspect_pipeline_execution.png](images/13_inspect_pipeline_execution.png)

## 14. Visualisation des composants du workflow.

![14_training_and_scoring_workflow.png](images/14_training_and_scoring_workflow.png)

## 15. métriques d'évaluation.

![15_evaluation.png](images/15_evaluation.png)