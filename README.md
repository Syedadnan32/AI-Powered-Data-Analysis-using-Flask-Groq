# AI-Powered Data Analysis using Flask & Groq

**Name:** Syed Adnan              
**Topic:** AI-Powered Data Analysis using Flask & Groq                     
**Company:** Zidio Development                            

**Over View:**

This project demonstrates an AI-driven approach to automate **data preprocessing and analysis**. Instead of manually writing pandas code, users can upload a dataset and query it in plain English. The system instantly generates the corresponding pandas code, executes it, and returns results.

## 📌 Problem Statement

* Traditional workflows require analysts to write pandas code manually for each query.                 
* Repetitive tasks are **time-consuming**.                       
* **Non-technical users** can’t directly analyze data.                       
* High dependency on skilled programmers.                     

## 🎯 Objective

* Build a **Flask web app** where users:

  * Upload CSV/XLSX datasets.              
  * Enter queries in plain English.           
  * Get instant results (tabular preview or numeric summary).                
* Bridge the gap between **data and decision-making**.              

## 🏗️ System Architecture

**Flow of the Application:**                   
Frontend (Flask + HTML Templates) → File Upload & Query Input                 
⬇️                           
**AI Model (Groq LLaMA 3.3-70B)** → Translates query → pandas code                      
⬇️                                                             
**Execution Layer** → Safely executes code and returns results                                       
⬇️                                
**Output** → Cleaned, analyzed data (tables/summaries)                                        
                    
## ⚙️ Data Preprocessing (utils.py & test.py)

* Detects file format (CSV/XLSX).                             
* Cleans dataset (handles missing values, converts datatypes).                           
* Standardizes columns (e.g., dates, numeric conversion).                        
* Saves a temporary cleaned CSV for smooth handling.                              

## 🤖 AI Query Processing

**Example:**
User: *“How many patients have diabetes (Outcome = 1)?”*                                          
AI Prompt: *“Given a pandas DataFrame named df, write Python code to answer this question.”*                                   

Generated Code:

```python                    
result = df[df['Outcome'] == 1].shape[0]                          
```                               

✅ Executed dynamically → Result returned instantly.                             

## 🧪 Testing & Validation

* `test.py` for offline debugging:

  * Runs preprocessing without Flask.                              
  * Validates queries on sample datasets.                             
  * Shows generated pandas code + execution output.                                    
* Ensures **accuracy, reliability, and faster debugging**.                                  

## 🚀 Future Enhancements

* Interactive visualizations (graphs, dashboards).                                  
* Multi-dataset analysis support.                                   
* SQL database integration.                                       
* SaaS deployment for wider adoption.                    
 
## 👥 Contributors

* **Naaz**

  * Designed system architecture                   
  * Implemented Flask integration & AI query processing                 
  * Developed preprocessing modules (`utils.py`, `test.py`)                    

* **Syed Adnan**

  * Performed **testing & validation** of the application                
  * Verified results using **APIs **                     
  * Ensured **accuracy, reliability, and robustness** of outputs                  
  * Reported and documented issues for improvement                         


✨ *Turning data into decisions with the power of AI + Flask.*

✨ *This repository is for educational and portfolio purposes.*
