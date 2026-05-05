# Earthquake Data-Driven Spatial System

This project explores the translation of earthquake-related data into spatial and interactive systems through a multi-modal computational workflow. By combining image-based analysis, textual interpretation, and geophysical data, the project establishes a data-driven design process that moves from data collection and fusion to spatial generation and real-time interaction.

This repository documents **Part 1: Data Collection, Analysis, and Fusion**, which forms the foundation for subsequent spatial and interactive stages.

---

## Access to Full Project Files

Full project materials, including Blender files, Processing scripts, datasets, and supporting documents, are available via OneDrive:

https://liveuclac-my.sharepoint.com/:f:/g/personal/ucbvz94_ucl_ac_uk/IgBhQGdm-1IfSqVe3db81iSOASuGqH7bbghzayAqKxJ76Cw?e=2NrSCx

---

## Project Structure

The overall workflow is organised into three stages:

1. Data Collection and Analysis (Jupyter Notebooks)  
2. Spatial Generation (Blender + Python)  
3. Real-Time Interaction (Processing)  

This repository focuses on the first stage, while subsequent spatial modelling and interactive visualisation are developed using Blender and Processing.

---

## Jupyter Notebooks

### 1. earthquake photos scraping.ipynb

This notebook is responsible for collecting and analysing earthquake-related images.

**Function:**
- Scrapes images using earthquake-related keywords  
- Cleans and filters the dataset  
- Extracts visual features including brightness, contrast, edge density, and a damage proxy  
- Applies clustering (K-means) to identify visual patterns  

**Output:**
- Image dataset (stored locally)  
- `image_features.csv`  

**Purpose:**
To translate visual representations of earthquake damage into measurable parameters for spatial use.

---

### 2. earthquake news scraping.ipynb

This notebook collects and processes earthquake-related textual data.

**Function:**
- Scrapes news headlines and descriptions  
- Performs keyword frequency analysis  
- Applies sentiment analysis  
- Uses clustering to group semantic patterns  

**Output:**
- Processed text dataset  
- `blender_input.csv`  

**Purpose:**
To convert narrative and emotional information into structured variables that can influence spatial behaviour.

---

### 3. earthquake_disaster_fusion_workflow.ipynb

This notebook integrates multiple datasets into a unified structure.

**Input:**
- Image features (from photo analysis)  
- Textual data (from news analysis)  
- Geophysical earthquake dataset  

**Function:**
- Normalises and aligns datasets  
- Computes combined indicators such as destruction index, fragmentation, and density signals  
- Prepares data for spatial mapping and downstream use  

**Output:**
- `final_fusion_data.csv`  

**Purpose:**
To construct a multi-modal dataset that directly drives spatial generation in later stages.

---

## Data Sources and Ownership

### External Dataset (Geophysical Data Only)

The geophysical earthquake dataset is the **only dataset sourced from an external platform**:

https://www.kaggle.com/datasets/usgs/earthquake-database

This dataset is provided by the United States Geological Survey (USGS) and contains records of earthquakes with magnitude 5.5 and above, including:

- Date and time  
- Latitude and longitude  
- Depth  
- Magnitude  

This dataset serves as the physical foundation of the project.

---

### Project-Generated Data

All other datasets in this repository are **self-generated through the project's workflow**, including:

- Scraped earthquake image dataset  
- Image feature extraction (`image_features.csv`)  
- Processed news data (`blender_input.csv`)  
- Final fused dataset (`final_fusion_data.csv`)  

These datasets are produced through custom scripts and analysis pipelines developed as part of this project.

---

## Included Files

The repository includes both raw and processed data to ensure reproducibility:

- `database.csv` — original geophysical earthquake dataset (external source)  
- `image_features.csv` — extracted visual features (generated)  
- `blender_input.csv` — processed textual data (generated)  
- `final_fusion_data.csv` — fused multi-modal dataset (generated)  
- Scraped image dataset (generated)  

---

## Project Objective

The project shifts from conventional data representation towards a generative system in which data actively drives spatial and behavioural outcomes.

By integrating multiple data domains, the workflow demonstrates how:

- Geophysical data informs spatial structure  
- Image data influences form and surface complexity  
- Text data introduces semantic and affective variation  

---

## Summary

The workflow can be understood as:

data → analysis → fusion → spatial generation → interaction

Rather than producing static representations, the project constructs a system in which spatial form and behaviour emerge from relationships within the data.
