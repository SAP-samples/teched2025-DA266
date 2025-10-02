# DA266 - Operationalizing AI with SAP Databricks in SAP Business Data Cloud

## Description

This repository contains the material for the SAP TechEd 2025 session called DA266 - Operationalizing AI with SAP Databricks in SAP Business Data Cloud. It covers end-to-end workflows and scripts for two main data product scenarios: **Cashflow Prediction** and **Payment Delay Prediction**. The repository is organized to support both learning (Exercise) and reference (Solution) use cases, with each scenario broken down into modular notebooks that guide you through the data science lifecycle. 

## Overview

This session introduces attendees to...

## Requirements
Before running the exercises, following items must be provided beforehand
- **Access to SAP Business Data Cloud Cockpit**
- **Access to SAP Databricks**: 
    - https://accounts.cloud.databricks.com/select-workspace?account_id=779c1dfb-54a0-4c0b-ab10-657b3ea0e70b
- **Users and Password for SAP Databricks**
    - e.g. `AC229588U01@sapexperienceacademy.com`
- **Access to the Unitity Catalogs**:
    - `uc_cash_liquidity_forecast`
    - `uc_delayed_payment`
- **Appropriate permissions to create schema within the above mentioned catalogs**
    - each user will have to create his own schema to run exercises
    - the schema name follows the pattern `<catalog_name>.grp.`+`<last_2_digits_of_user>`
    - e.g. user AC229588U**01** will create correspondingly the schemas
        - uc_cash_liquidity_forecast.grp**01** 
        - uc_delayed_payment.grp**01**
- **Access to required Python packages**
    - `sap-bdc-connect-sdk` 
- **Configured SECRET SCOPE** 
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


- A. Sharing Data Products to SAP Databricks
    - Exercise
        - 01 Share_Data_Product_to_SAP_Databricks
- B. Cashflow prediction
    - Exercise
        - [00_Data Understanding.ipynb](exercises/ex0/)
        - 01_Cash_Liquidity_Data_Preparation.ipynb
        - 02_Cash_Liquidity_Training.ipynb
        - 03_Cash_Liqudity_Forecast.ipynb
        - 04_Publish_Data_Product.ipynb
        - Time Series Forecast Notebook Schedule.ipynb
    - Solution
        - 01_Cash_Liquidity_Data_Preparation.ipynb
        - 02_Cash_Liquidity_Training.ipynb
        - 03_Cash_Liqudity_Forecast.ipynb
        - 04_Publish_Data_Product.ipynb
        - Time Series Forecast Notebook Schedule.ipynb
- C. Payment delay prediction
    - Exercise
        - 01_Payment Delay Data Preparation.ipynb
        - 02_Payment Delay Training.ipynb
        - 03_Payment Delay Inference.ipynb
        - 04_Publish_Data_Product.ipynb
    - Solution
        - 01_Payment Delay Data Preparation.ipynb
        - 02_Payment Delay Training.ipynb
        - 03_Payment Delay Inference.ipynb
        - 04_Publish_Data_Product.ipynb







## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
