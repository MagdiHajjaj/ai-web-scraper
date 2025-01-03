# AI Web Scraper
 
This Python-based web scraper uses **Selenium** and **BeautifulSoup** to scrape data from websites. It supports **BrightData Super Proxy** for accessing sites securely through a proxy network.

---

## Features
- **Automated Browsing**: Uses Selenium WebDriver for browser automation.
- **HTML Parsing**: Extracts web page content using BeautifulSoup.
- **Proxy Support**: Configured to use BrightData for secure and efficient scraping.
- **Screenshot Capture**: Automatically captures screenshots of the visited pages.
- **Interactive DOM Parsing**: Allows users to describe and parse specific DOM content through Streamlit using **Ollama**.

---

## Setup Instructions

### 1. Download or clone the Repository
To clone:
```bash
git clone https://github.com/your-username/ai-web-scraper.git
cd ai-web-scraper
```
### 2. Create and Activate a Virtual Environment
On Windows:
```bash
python -m venv scraper_env
.\scraper_env\Scripts\activate
```
On macOS/Linux:
```bash
python3 -m venv scraper_env
source scraper_env/bin/activate
```
### 3. Install Dependencies
Install the required Python packages:
```bash
pip install -r requirements.txt
```
### 4. Set Up BrightData Authentication
Create a .env file in the root directory of the project with your BrightData credentials:
```bash
BRIGHTDATA_AUTH=your-authentication-token
```
Replace your-authentication-token with your BrightData credentials.
### 5. Install Chrome Driver
#### Ensure you have the correct version of Chrome WebDriver:

1. Download from [https://googlechromelabs.github.io/chrome-for-testing/#stable](https://googlechromelabs.github.io/chrome-for-testing/#stable).
2. Make sure it matches the version of your installed Google Chrome browser.
3. Add the `chromedriver.exe` to your system PATH or place it in the project directory.

## Ollama Setup

**Ollama** is used in this project to parse DOM content based on user descriptions. Here’s how to set it up and use it:

### 1. Download Ollama
First, download **Ollama** from the official website:
- [Ollama Download Link](https://ollama.com/)

### 2. Install a Model from Ollama GitHub
After installing **Ollama**, you can choose which model you want to use by visiting the [Ollama GitHub Model](https://github.com/ollama/ollama). Follow these steps:
1. Scroll to the bottom of the README on the GitHub page.
2. Choose the version of the model you want to use.

### 3. Pull the Model
To pull the model you selected, use the following command:
```bash
ollama pull <model-name>
```
Replace <model-name> with the model version you selected.
### 4. Modify the Code to Use the Correct Model
After you’ve pulled the model, navigate to `parse.py` in the project directory. Locate the line:

```bash
model = OllamaLLM(model="llama3.1")
```
Change "llama3.1" to the model you pulled from Ollama. For example:

```bash
model = OllamaLLM(model="your-chosen-model")
```
### Usage
Run the scraper by executing the script and providing the target website:
```bash
streamlit main.py
```
#### The script will:
1. Navigate to the specified website.
2. Take a screenshot of the page (saved as page.png).

Follow the instruction on the website.
## License

[MIT](https://choosealicense.com/licenses/mit/)

Copyright (c) 2024 Magdi Hajjaj

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
