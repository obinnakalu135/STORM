## Highlighting Unique Information in Your Research Documents

This program helps analyze a collection of PDF documents and identify those containing the most unique information. It uses a technique called Term Frequency-Inverse Document Frequency (TF-IDF) to achieve this.

**What is TF-IDF?**

Imagine each document as a conversation. TF-IDF considers words like "the" or "and" to be common and not very informative, just like everyday words in a conversation. On the other hand, words specific to your research topic would be like technical terms used in that conversation. 

* **Term Frequency (TF):** TF-IDF considers how often a word appears within a single document. The more a specific word shows up in a particular PDF compared to common words, the higher its TF score. 
* **Inverse Document Frequency (IDF):** IDF focuses on how rare a word is across all the documents in your collection. If a word appears only in a few PDFs, it gets a high IDF score.

By combining these scores (TF x IDF), TF-IDF helps identify documents that use specific vocabulary not found elsewhere in your collection. These documents are likely to contain the most unique and relevant information for your research.

## Using the Code (Mac and Windows)

This project requires Python libraries and some setup steps. Here's a detailed guide for Mac and Windows users.
**Mac and Windows (Using Python)**

1. **Download and Install Python:**

   - Visit the official Python website ([https://www.python.org/downloads/](https://www.python.org/downloads/)) and download the latest version of Python that matches your operating system (Mac or Windows).
   - During installation, make sure to add Python to your system path. This allows you to run Python commands from your terminal/command prompt window.

2. **Install Required Libraries:**

   - Open a terminal window (Mac) or command prompt window (Windows).
   - We'll use the `pip` package manager to install the necessary libraries for this project. Type the following command and press Enter:

     ```bash
     pip install nltk scikit-learn pandas PyPDF2
     ```

     This command downloads and installs the required libraries (`nltk`, `scikit-learn`, `pandas`, and `PyPDF2`) that your project needs to run.

3. **Download NLTK Resources:**

   - Import the `nltk` library in your Python script (or Jupyter notebook) and run the following code to download resources needed for text processing:

     ```python
     import nltk
     nltk.download('stopwords')
     ```

4. **Running the Script:**

   - Save the provided Python code (including the functions) in a file named `your_script_name.py`. 
   - Make sure your PDFs are stored in a folder named "files" within the same directory as your script.

   **Mac:**

     - Open a terminal window and navigate to the directory containing your script and PDFs using the `cd` command. For example, if your files are on your desktop, you might use:

       ```bash
       cd Desktop
       ```

     - Run the script using the following command, replacing `your_script_name.py` with the actual filename:

       ```bash
       python your_script_name.py
       ```

   **Windows:**

     - Open a command prompt window and navigate to the directory containing your script and PDFs using the `cd` command. For example, if your files are on your desktop, you might use:

       ```
       cd \Users\<username>\Desktop
       ```

       (Replace `<username>` with your actual Windows username)

     - Run the script using the following command, replacing `your_script_name.py` with the actual filename:

       ```
       python your_script_name.py
       ```

## Important Notes

* This code might take a while to run depending on the number of PDFs you have. 
* The output will display the top N most unique PDFs (adjust N in the code) based on their TF-IDF scores.
* Include a folder of the pdfs, as downloaded from Zotero. Currently, the file structure is such that there is a main "files" folder, with subfolders which contain PDFs.
