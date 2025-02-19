# 🏆 RPA Challenge - UiPath Automation

## 📌 Project Overview
This project automates the **RPA Challenge - Input Form** using UiPath **Studio 2023.10** and the **Robotic Enterprise Framework (REFramework)**.  
It follows best practices for modular development, logging, error handling, and structured automation.  

## 🚀 Features
- **Web Automation** → Uses `Use Application/Browser` for efficient browser interaction.  
- **Retry Mechanism** → Implements `Retry Scope` to handle download waiting times.  
- **Excel Processing** → Reads and processes Excel data dynamically.  
- **Transaction-Based Processing** → Uses `Get Transaction Data` to handle structured data.  
- **Final Score Extraction** → Captures and logs the final challenge score.



---

## **📌 How It Works**
### **1️⃣ Initialization (`Init`)**
- **`InitAllSettings.xaml`** → Loads configuration data from `Config.xlsx`.  
- **`InitAllApplications.xaml`** → Opens and prepares the browser for the challenge.
  - Calls `I-1.RPAChallenge_OpenBrowser`.
- **`I-2.RPAChallenge_DownloadExcel`** Download the data.
- **`I-3.RPAChallenge_ExtractExcelData`** Extract all data from excel file.
- **`I-4.RPAChallenge_ClickStart.xaml`** Init the Challenge.

### **2️⃣ Get Transaction Data (`GetTransactionData`)**
- Fetches each row as a transaction for processing.
- **`G-1.RPAChallenge_GetFinalScore.xaml`** when transactions are finished get the final score.  

### **3️⃣ Process Transaction (`Process`)**
- **`P-1.RPAChallenge_InputFormData.xaml`** → Enters transaction data into the web form.  

### **4️⃣ End Process (`End Process`)**
- **`E-1.RPAChallenge_CloseBrowser.xaml`** → Closes the browser session after completion.  

---

## **🛠️ Setup Instructions**
1️⃣ **Clone this repository**  
```bash
git clone https://github.com/Make310/AUX-RPAChallenge_InputForm
