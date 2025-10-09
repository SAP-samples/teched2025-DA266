# DA266 - Operationalizing AI with SAP Databricks in SAP Business Data Cloud

## Description

This repository contains the material for the [SAP TechEd 2025](https://www.sap.com/events/teched.html) session called DA266-Operationalizing AI with SAP Databricks in SAP Business Data Cloud. It covers end-to-end workflows and scripts for two main user case scenarios `Cashflow Prediction` and `Payment Delay Prediction`. The repository is organized to support both learning (Exercise) and reference (Solution) use cases, with each scenario broken down into modular notebooks that guide you through the data science lifecycle. 

## Overview
#### Use Case: Cashflow Prediction
This scenario demonstrates how to build a data product for forecasting cash liquidity. The workflow includes:

- 00_Data_Understanding.ipynb: Explore and understand the transactional cashflow data.
- 01_Cash_Liquidity_Data_Preparation.ipynb: Prepare and clean the data, including time series transformation.
- 02_Cash_Liquidity_Training.ipynb: Train time series forecasting models and log results.
- 03_Cash_Liqudity_Forecast.ipynb: Generate forecasts using the trained models.
- 04_Publish_Data_Product.ipynb: Publish the resulting data product to SAP Business Data Cloud (BDC) Catalog using Delta Sharing.

Time Series Forecast Notebook Schedule.ipynb: Provides a schedule and overview for running the notebooks in sequence.
Each notebook in the Exercise folder is designed for hands-on learning, while the Solution folder provides reference implementations.

#### Use Case: Payment Delay Prediction
This advanced scenario focuses on predicting payment delays using machine learning. 
Furthermore, the prediction results will be interpreted and explained along with their key drivers. The workflow includes:

- 01_Payment_Delay_Data_Preparation.ipynb: Data cleaning and feature engineering for payment delay prediction.
- 02_Payment_Delay_Training.ipynb: Model training and evaluation.
- 03_Payment_Delay_Inference.ipynb: Applying the trained model to new data for inference.
- 04_Payment_Delay_Explain.ipynb: Explaining the inferenced result and its key drivers.
- 05_Publish_Data_Product.ipynb: Publishing the prediction results as a data product to BDC.

As with the cashflow scenario, both Exercise and Solution folders are provided.


## Requirements
Before running the exercises, following items must be provided beforehand
- Access to SAP Business Data Cloud Cockpit
- Access to SAP Databricks: 
    - https://accounts.cloud.databricks.com/select-workspace?account_id=779c1dfb-54a0-4c0b-ab10-657b3ea0e70b
- Users and Password for SAP Databricks
    - should be provided by your workshop host
    - e.g. `ac229588u01@sapexperienceacademy.com`
- Access to the Unitity Catalog:
    - `uc_cash_liquidity_forecast`
    - `uc_delayed_payments`
- Appropriate permissions to create schema within the above mentioned catalogs
    - each user will have to create his own schema to run exercises
    - the schema name follows the pattern `<catalog_name>.grp.`+`<last_2_digits_of_user>`
    - e.g. user ac229588u**01** will create correspondingly the schemas
        - uc_cash_liquidity_forecast.grp**01** 
        - uc_delayed_payments.grp**01**
- Access to delta shared SAP Data Products
    - `Cashflow` 
    - `Entry View Journal Entry`
- Access to a configured SAP AI Core Service intance with corresponding service key
    - https://help.sap.com/docs/sap-ai-core/sap-ai-core-service-guide/initial-setup
- Access to required Python packages
    - `sap-bdc-connect-sdk` 
    - `sap-ai-sdk-gen` 
- Configured SECRET SCOPE
    - This step has already been done by the administrator to facilitate the sharing process. However, if you need to do it on you own you can follow the steps described here to create a secret scope: To create a secret scope you can either use the following URL `https://<databricks-instance>#secrets/createScope`. Replace `<databricks-instance>` with the workspace URL of your Databricks deployment.
    - Alternatively, you can run the following command in the terminal by clicking on the terminal icon on the lower right corner: `databricks secrets create-scope sap-bdc-connect-sdk`. 
    - The secret scope only has to be created once and can be made accessible to all workspace users by either toggling `manage principal` to `all workspace users` or via the terminal using the following command `databricks secrets put-acl sap-bdc-connect-sdk users READ`. To check whether the assignment worked, you can then use the command `databricks secrets list-acls sap-bdc-connect-sdk`.
    - A full explanation can be found here https://docs.databricks.com/aws/en/security/secrets/example-secret-workflow     


## Exercises
>[!TIP]
>1. **Start with the Exercise notebooks** to follow the guided workflow and implement each step yourself.
>2. **Refer to the Solution notebooks** for completed code and best practices.
>3. **Follow the notebook order** (as indicated by the numbering) for a logical progression from data understanding to publishing a data product.
>4. **Publishing to BDC**: The final notebook in each scenario demonstrates how to expose your results as a data product using Delta Sharing and the SAP BDC Connect SDK.


- Sharing Data Products to SAP Databricks
    - Exercise
        - 01 Share_Data_Product_to_SAP_Databricks
- Cashflow prediction
    - Exercise
        - [00_Data Understanding.ipynb](./Cashflow_prediction/Exercise/00_Data_Understanding.ipynb)
        - [01_Cash_Liquidity_Data_Preparation.ipynb](./Cashflow_prediction/Exercise/01_Cash_Liquidity_Data_Preparation.ipynb)
        - [02_Cash_Liquidity_Training.ipynb](./Cashflow_prediction/Exercise/02_Cash_Liquidity_Training.ipynb)
        - [03_Cash_Liqudity_Forecast.ipynb](./Cashflow_prediction/Exercise/03_Cash_Liqudity_Forecast.ipynb)
        - [04_Publish_Data_Product.ipynb](./Cashflow_prediction/Exercise/04_Publish_Data_Product.ipynb)
    - Solution
        - [00_Data Understanding.ipynb](./Cashflow_prediction/Solution/00_Data_Understanding.ipynb)
        - [01_Cash_Liquidity_Data_Preparation.ipynb](./Cashflow_prediction/Solution/01_Cash_Liquidity_Data_Preparation.ipynb)
        - [02_Cash_Liquidity_Training.ipynb](./Cashflow_prediction/Solution/02_Cash_Liquidity_Training.ipynb)
        - [03_Cash_Liqudity_Forecast.ipynb](./Cashflow_prediction/Solution/03_Cash_Liqudity_Forecast.ipynb)
        - [04_Publish_Data_Product.ipynb](./Cashflow_prediction/Solution/04_Publish_Data_Product.ipynb)
        - Time Series Forecast Notebook Schedule.ipynb
- Payment delay prediction
    - Exercise
        - [01_Payment_Delay_Data_Preparation.ipynb](./Payment_delay_prediction/Exercise/01_Payment_Delay_Data_Preparation.ipynb)
        - [02_Payment_Delay_Training.ipynb](./Payment_delay_prediction/Exercise/02_Payment_Delay_Training.ipynb)
        - [03_Payment_Delay_Inference.ipynb](./Payment_delay_prediction/Exercise/03_Payment_Delay_Inference.ipynb)
        - [04_Payment_Delay_Explain.ipynb](./Payment_delay_prediction/Exercise/04_Payment_Delay_Explain.ipynb)
        - [05_Publish_Data_Product.ipynb](./Payment_delay_prediction/Exercise/05_Publish_Data_Product.ipynb)
    - Solution
        - [01_Payment_Delay_Data_Preparation.ipynb](./Payment_delay_prediction/Solution/01_Payment_Delay_Data_Preparation.ipynb)
        - [02_Payment_Delay_Training.ipynb](./Payment_delay_prediction/Solution/02_Payment_Delay_Training.ipynb)
        - [03_Payment_Delay_Inference.ipynb](./Payment_delay_prediction/Solution/03_Payment_Delay_Inference.ipynb)
        - [04_Payment_Delay_Explain.ipynb](./Payment_delay_prediction/Solution/04_Payment_Delay_Explain.ipynb)
        - [05_Publish_Data_Product.ipynb](./Payment_delay_prediction/Solution/05_Publish_Data_Product.ipynb)







## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
