# **DocXtractAI**  
**DocXtractAI** is an AI-powered tool that extracts structured data from **purchase order PDFs**, converting text and tables into a well-organized **JSON format**. It leverages **Ollama** for intelligent data structuring and uses **PyMuPDF (fitz) and pdfplumber** for PDF text and table extraction.  

---

## NOTE:
Currently, this project uses **Mistral (Ollama's model)** for local implementation, as it is lightweight and free to use. However, for **even better accuracy in data extraction**, more advanced **LLMs such as GPT-4-turbo, Claude 3, or fine-tuned domain-specific models** could be used.  

Since many of these high-performance models require **paid API access**, I have designed this implementation to run **entirely locally**, making it accessible without additional costs. 

---

All Jupyter Notebook (`.ipynb`) files in this repository contain **the same code**, with only the **document path changed** for extracting different PDFs.  

To ensure **easier access and structured organization**, I have uploaded separate notebooks for each document instead of modifying a single file repeatedly.  

---

## **Accessing Output HTML Files**  
The extracted data is also saved as **HTML files** for easy visualization. These files can be accessed in the `output_html_files` folder:  

- [Task2_KsamaArora_Doc1.html](output_html_files/Task2_KsamaArora_Doc1.html)  
- [Task2_KsamaArora_Doc2.html](output_html_files/Task2_KsamaArora_Doc2.html)  

---

## **Installation & Setup**  

### **1. Clone the Repository**  
```bash
git clone https://github.com/ksamaarora/DocXtractAI.git
cd DocXtractAI
```

---

### **2. Set Up a Virtual Environment**  
It is recommended to use a separate **Conda environment** for this project.  

#### **Create a new environment:**  
```bash
conda create --name doc_env python=3.8
```

#### **Activate the environment:**  
```bash
conda activate doc_env
```

#### **To deactivate the environment when finished:**  
```bash
conda deactivate
```

---

### **3. Install Dependencies**  
Ensure that Python 3.8+ is installed. The required dependencies can be installed using:  
```bash
pip install -r requirements.txt
```

---

### **4. Set Up Ollama**  
Ollama must be installed and running to execute the model. It can be downloaded from **[Ollama's official website](https://ollama.com/)**.  

Once installed, retrieve the **Mistral** model by executing:  
```bash
ollama pull mistral
```

---

### **5. Run the Application**  
To run the application locally, open **two separate terminals**:  

#### **In the first terminal, start the Ollama server:**  
```bash
ollama serve
```

#### **In the second terminal, start Jupyter Notebook:**  
```bash
jupyter notebook
```

Open the notebook file (`.ipynb`) and run the necessary cells.

---

## **Dependencies**  
Ensure the following libraries are installed:  

- `ollama`  
- `PyMuPDF (fitz)`  
- `pdfplumber`  
- `pillow`  
- `json`  
- `ipython`  
- `jupyter`  

These are included in the `requirements.txt` file.
