# 🚀 ADF Copy Activity Project

### Excel to Parquet using Azure Data Factory

---

## 📌 Project Overview

This project demonstrates how to build an **end-to-end data pipeline** using Azure services. The pipeline reads an Excel file from Azure Blob Storage, processes it using Azure Data Factory, and stores the output in **Parquet format** in Azure Data Lake Storage Gen2.

---

## 🏗️ Architecture

```
Excel File (Local)
        ↓
Azure Blob Storage (Source)
        ↓
Azure Data Factory (Copy Activity)
        ↓
Azure Data Lake Storage Gen2 (Sink - Parquet)
```

---

## 🛠️ Azure Services Used

* Azure Resource Group
* Azure Data Factory (ADF)
* Azure Blob Storage
* Azure Data Lake Storage Gen2 (ADLS Gen2)

---

## 📂 Implementation Steps

### 1️⃣ Create Resource Group

* Go to Azure Portal
* Click on "Resource Groups" → Create
* Enter:

  * Resource Group Name
  * Region

---

### 2️⃣ Create Azure Data Factory

* Search for **Data Factory** in Azure Portal
* Click **Create**
* Configure:

  * Resource Group
  * Name
  * Region

---

### 3️⃣ Create Azure Blob Storage

* Go to Storage Accounts → Create
* Select:

  * Standard Performance
  * Hot Access Tier
* Create a container (e.g., `input-data`)

---

### 4️⃣ Create ADLS Gen2

* Create another Storage Account
* Enable:

  * **Hierarchical Namespace (IMPORTANT)**
* Create a container (e.g., `output-data`)

---

### 5️⃣ Upload Excel File

* Open Blob Storage container
* Upload `.xlsx` file

---

### 6️⃣ Azure Data Factory Pipeline

#### 🔹 Create Linked Services

* Blob Storage (Source)
* ADLS Gen2 (Sink)

#### 🔹 Create Datasets

* Source Dataset → Excel file
* Sink Dataset → Parquet format

---

### 7️⃣ Configure Copy Activity

#### Source:

* File Type: Excel
* Select Sheet

#### Sink:

* File Type: Parquet
* Output path in ADLS Gen2

---

### 8️⃣ Run Pipeline

* Click **Debug**
* Trigger Pipeline
* Validate output in ADLS

---

## 📊 Output

* Excel file successfully converted into **Parquet format**
* Stored in ADLS Gen2 container

---

## 🎯 Key Learnings

* Building ETL pipelines using Azure Data Factory
* Working with Azure Blob Storage and ADLS Gen2
* Data format conversion (Excel → Parquet)
* Understanding cloud-based data engineering workflows

---

## 📁 Repository Structure

```
ADF-COPY-ACTIVITY/
│── README.md
│── screenshots/
│   ├── resource-group.png
│   ├── storage-account.png
│   ├── adf-pipeline.png
│   ├── copy-activity.png
│   └── output.png
│── sample-data/
│   └── input.xlsx
```

---

## 📸 Screenshots

*(Add screenshots here for better understanding)*

* Resource Group Creation
* Storage Account Setup
* ADF Pipeline
* Copy Activity Configuration
* Output in ADLS

---

## 🚀 Future Enhancements

* Parameterized pipelines
* Scheduled triggers
* Data validation checks
* Integration with Azure Synapse

---

## 🤝 Contribution

Feel free to fork this repository and enhance the project.

---

## ⭐ Support

If you found this helpful, give it a ⭐ on GitHub!

---

