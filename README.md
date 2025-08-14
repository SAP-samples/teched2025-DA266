# DA266 - Operationalizing AI with SAP Databricks in SAP Business Data Cloud

## Description

This repository contains the material for the SAP TechEd 2025 session called DA266 - Operationalizing AI with SAP Databricks in SAP Business Data Cloud. It covers end-to-end workflows and scripts for two main data product scenarios: **Cashflow Prediction** and **Payment Delay Prediction**. The repository is organized to support both learning (Exercise) and reference (Solution) use cases, with each scenario broken down into modular notebooks that guide you through the data science lifecycle. 

## Overview

This session introduces attendees to...

## Requirements

- Access to SAP Business Data Cloud Cockpit
- Access to SAP Databricks with Unity Catalog enabled.
- Required Python packages (see the first cells in each notebook for installation commands).
- Appropriate permissions to create secret scopes and shares in SAP Databricks.

## Exercises

Provide the exercise content here directly in README.md using [markdown](https://guides.github.com/features/mastering-markdown/) and linking to the specific exercise pages, below is an example.

1. **Start with the Exercise notebooks** to follow the guided workflow and implement each step yourself.
2. **Refer to the Solution notebooks** for completed code and best practices.
3. **Follow the notebook order** (as indicated by the numbering) for a logical progression from data understanding to publishing a data product.
4. **Publishing to BDC**: The final notebook in each scenario demonstrates how to expose your results as a data product using Delta Sharing and the SAP BDC Connect SDK.


- Cashflow prediction
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
- Payment delay prediction
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
  
**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
