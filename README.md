# Tokyo 2021 Olympics Data Engineering Project

## Project Overview
This project involves the extraction, transformation, and analysis of data from the 2021 Tokyo Olympics. The data is sourced from a GitHub repository, ingested using Azure Data Factory, stored in Azure Data Lake Gen2, transformed in Azure Databricks, and analyzed in Azure Synapse Analytics. The project leverages various Azure services for orchestration, storage, authentication, and secrets management.

## Architecture
![Blank diagram](https://github.com/user-attachments/assets/85bfd5f8-0abf-4134-84c9-e850b419c5a2)


## Technologies Used
- **Data Source**: Data Factory / GitHub
- **Orchestration**: Azure Data Factory
- **Ingestion**: Azure Data Lake Gen2
- **Storage**: Azure Synapse Analytics
- **Authentication and Secrets Management**: Azure Active Directory and Azure Key Vault

## Project Steps

### 1. Data Extraction
The data from the 2021 Tokyo Olympics is extracted from a GitHub repository using Azure Data Factory. The data is then ingested into Azure Data Lake Gen2 for storage.

#### Steps:
1. **Create a Linked Service in Azure Data Factory**:
   - Configure a Linked Service to connect to the GitHub repository.

![Screenshot 2024-10-18 162452](https://github.com/user-attachments/assets/3373af94-f475-446c-a255-aa0b3a638650)

2. **Create a Pipeline in Azure Data Factory**:
   - Create a pipeline to extract the data from the GitHub repository and load it into Azure Data Lake Gen2.
  
     ![Screenshot 2024-10-18 162617](https://github.com/user-attachments/assets/07ca15a3-a7e3-485d-9eb4-1140f3bbdde7)

3. **Data to Extract:
    - Athletes
    - Coaches
    - EntriesGender
    - Medals
    - Teams




### 2. Data Transformation
The ingested data is transformed using Azure Databricks. The transformation process includes cleaning, aggregating, and preparing the data for analysis.

#### Steps:
1. **Create a Databricks Workspace**:
   - Set up a Databricks workspace in Azure.
2. **Create a Notebook in Databricks**:
   - Develop a notebook to perform data transformation tasks.
3. **Load Data from Azure Data Lake Gen2**:
   - Read the data from Azure Data Lake Gen2 into Databricks.
4. **Transform the Data**:
   - Perform data cleaning, aggregation, and preparation.
5. **Save Transformed Data**:
   - Save the transformed data back to a different folder in Azure Data Lake Gen2.
  
![Screenshot 2024-10-18 164254](https://github.com/user-attachments/assets/fc93f8bc-6179-4716-80a2-faf68c5ab9a8)



### 3. Data Analysis
The transformed data is analyzed using Azure Synapse Analytics. SQL queries are used to generate insights and reports from the data.

#### Steps:
1. **Create a Synapse Workspace**:
   - Set up a Synapse workspace in Azure.
2. **Create a SQL Pool**:
   - Create a dedicated SQL pool for data analysis.
3. **Load Data into Synapse**:
   - Load the transformed data from Azure Data Lake Gen2 into Synapse.
4. **Perform Data Analysis**:
   - Use SQL queries to analyze the data and generate insights.
![Screenshot 2024-10-18 162851](https://github.com/user-attachments/assets/49e75ccc-95e6-405e-9197-6b84790d52e2)
![Screenshot 2024-10-18 162939](https://github.com/user-attachments/assets/f2ec5696-ba13-4eec-8b05-c654b6372962)
![Screenshot 2024-10-18 163018](https://github.com/user-attachments/assets/c1a24f52-de4a-4ef0-be31-c907cb3c0fc3)




## Security and Authentication
The project uses Azure Active Directory for authentication and Azure Key Vault for secrets management. This ensures secure access to resources and sensitive information.

#### Steps:
1. **Set Up Azure Active Directory**:
   - Configure Azure Active Directory for user authentication.
2. **Set Up Azure Key Vault**:
   - Store and manage secrets, such as connection strings and API keys, in Azure Key Vault.
3. **Integrate Key Vault with Data Factory and Databricks**:
   - Use Key Vault to securely access secrets in Data Factory and Databricks.

## Conclusion
This project demonstrates a comprehensive data engineering workflow using Azure services. By leveraging Azure Data Factory, Azure Data Lake Gen2, Azure Databricks, and Azure Synapse Analytics, we successfully extracted, transformed, and analyzed data from the 2021 Tokyo Olympics. The use of Azure Active Directory and Azure Key Vault ensures secure and efficient management of authentication and secrets.

## Credits
This Project is inspired by the video of the https://www.youtube.com/watch?v=IaA9YNlg5hM&t=0s
