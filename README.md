# Azure_Airport_ADF_Azure_DevOps_CI_CD_Project
This repo contains details around Sample Airport data sourced in ADLS and leveraging ADF to transform the data and loading into ADLS and implementing ADF Pipeline in Dev and leveraging Azure DevOps CI/CD to deploy the pipeline to PROD using DevOps Release/Pipeline using ARM template method. Thanks



### **Data Flow Architecture Diagram**

The project follows a standard data engineering and DevOps pattern where data is transformed within Azure and deployed across environments using automation.

**1. Data Processing Flow:**
**ADLS (Source Data)** → **ADF (Dataflow/Transformation)** → **ADLS (Target/Transformed Data)**

**2. CI/CD Deployment Flow:**
**ADF Dev Environment** → **Azure DevOps (Git Repo)** → **ARM Template Generation** → **Azure DevOps Release Pipeline** → **ADF PROD Environment**

---

### **Step-by-Step Execution Guide**

The following steps outline how to implement and deploy the airport data transformation pipeline as described in the sources.

#### **Step 1: Data Sourcing and Initial Setup**
*   **Source the Sample Airport data** into an **Azure Data Lake Storage (ADLS)** account.
*   Configure the **Azure Data Factory (ADF)** environment in the **Dev** region to access this storage.

#### **Step 2: Develop Transformation Pipelines**
*   Create an **ADF Pipeline** in the Dev environment.
*   Leverage **ADF Dataflows** to perform the necessary transformations on the airport data.
*   Configure the pipeline to load the finalized, transformed data back into **ADLS**.

#### **Step 3: Version Control Integration**
*   Connect the ADF Dev environment to an **Azure DevOps Git Repository**.
*   Manage changes through **branches** and **commits** to track the development of the pipeline and dataflow components.

#### **Step 4: Generate Deployment Artifacts**
*   Utilize the **ARM template method** for deployment.
*   Ensure the repository includes the necessary template files, specifically `ARMTemplateForFactory.json` and `ARMTemplateParametersForFactory.json`, which define the infrastructure and configuration for the factory.

#### **Step 5: Configure CI/CD Pipelines**
*   Set up an **Azure DevOps Release/Pipeline** to automate the movement of code from Dev to PROD.
*   Configure **Agent Jobs** within Azure DevOps to execute the deployment tasks.
*   (Optional but recommended based on repository files) Set up **Email Notifications** in Azure DevOps to alert the team of success or failure of the deployment.

#### **Step 6: Deploy to PROD and Validate**
*   Execute the DevOps pipeline to deploy the **ARM templates** into the **PROD environment**.
*   Verify the **successful deployment** of both the ADF Pipelines and Dataflows in the PROD instance.
*   Confirm the **final execution** of the pipeline in PROD to ensure airport data is being transformed and stored correctly in the production ADLS.

***
