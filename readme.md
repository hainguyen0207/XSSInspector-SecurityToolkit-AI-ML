# XSSInpector Security AI ML 

## Overview

World's first Artificial Intelligence (XSS) Cross Site Scripting powered by Machine Learning with extreme fine-tuning designed to detect Reflected, Stored, DOM, and Blind (XSS) vulnerabilities in servers/apps at RFC design, forms, crawls, and through advanced AI techniques with deep and reinforcement learning, (NLP) and automatic payload generation.

## Creator
Created and designed by Haroon Ahmad Awan.

## Requirements

Save the following content as `requirements.txt` in the root directory of your project:
## Essential Libraries

```bash
numpy
scipy
scikit-learn
pandas
tensorflow
keras
sqlalchemy
flask
beautifulsoup4
requests
lxml
```
## Create a virtual environment:

```bash
python3 -m venv venv
```

## On Windows/Linux/Mac:
```bash
source venv/bin/activate
venv\Scripts\activate
pip install -r requirements.txt
```

## Run your project:
```bash
python xssscanadv.py
```

## Contact 
- haroon@cyberzeus.pk
- https://www.cyberzeus.pk

## Features

# AI-ML Trained Obfuscation Methods

## Known to Unknown
Includes built-in obfuscation methods to automatically check if we successfully bypassed the firewall. Results are then recorded into trained data, enhancing the detection and accuracy of payloads to identify more vulnerabilities.

## HTTP Verbs

### Fuzz
Built-in HTTP verb tampering to check for vulnerabilities, using known and unknown HTTP verbs.

## Machine Learning

### Deep Learning Models
Utilizes neural networks to predict vulnerabilities based on complex features.

### Model Training and Prediction
Trains models on past scan results and uses them to filter and prioritize URLs for scanning.

## Natural Language Processing (NLP)

### Content Analysis
Analyzes web page content to identify forms and input fields that could be susceptible to XSS attacks.

### Form and Input Extraction
Extracts details of forms and input fields to better target XSS injection points.

## Reinforcement Learning

### Adaptive Learning
Learns from each scanning attempt to improve payload selection and application over time.

### History-Based Adjustments
Adjusts future payload selection based on the success of past attempts.

## Automated Payload Generation

### Dynamic Payloads
Generates sophisticated XSS payloads dynamically based on the structure of the web page.

### Server-Specific Payloads
Provides tailored payloads for different server types (e.g., nginx, apache, IIS).

## URL Crawling

### Deep Crawling
Fetches additional URLs using CommonCrawl and Wayback Machine to ensure comprehensive coverage.

### Targeted Crawling
Focuses on URLs likely to be vulnerable based on predictive models.

## Detection of XSS

### Blind XSS
Detects blind XSS vulnerabilities and can use custom endpoints to detect real-time blind XSS, training the software for more accuracy in future scans. Types include:
- Server-Side Blind XSS
- Client-Side Blind XSS
- HTTP verb tampering based Blind XSS
- Server Parameter Tampering for Blind XSS

### Reflected XSS
Identifies reflected XSS vulnerabilities and their subtypes by analyzing the immediate reflection of payloads. Types include:
- GET-Based Reflected XSS
- POST-Based Reflected XSS
- URL-Based Reflected XSS
- HTTP verb tampering based Reflected XSS
- Server Parameter Tampering for Reflected XSS

### Stored XSS
Detects stored XSS vulnerabilities by inspecting whether payloads are saved and executed later within the web application. Types include:
- Database Stored XSS
- File Stored XSS
- HTML Stored XSS
- HTTP verb tampering based Stored XSS
- Server Parameter Tampering for Stored XSS

## Reporting and Logging

### Database Logging
Logs all scan results in a SQLite database for easy access and analysis.

### How to View Logged Database
```bash
Go to https://inloop.github.io/sqlite-viewer/# and import the .db file to see what's going on after you have finished scanning with success and failure ratios(intended for expert users only)
```

### HTML Reports
Generates detailed HTML reports summarizing the scan results and vulnerabilities found.

## Multi-Threading

### Concurrent Scanning
Utilizes multi-threading to scan multiple URLs simultaneously, improving scanning speed and efficiency.

## Usage

## Crawl the target website for URLs
```bash
python xssscanadv.py -d http://testphp.vulnweb.com --crawl
```

##  Target website for URLs with Report
```bash
python xssscanadv.py -d http://testphp.vulnweb.com --crawl --report report.html
```

## Crawling URLs for scanning
```bash
python xssscanadv.py -l crawled_urls.txt -t 100 --duration 3600 -s --mode autounderstand --use-model --report report.html
```

## Quickly extract and clean URLs from the Wayback Machine, Common Crawl
```bash
python xssscanadv.py -d http://testphp.vulnweb.com --extractquick
```

## Use the cleaned URLs for scanning
```bash
python xssscanadv.py -l testphp_vulnweb_com_cleaned_urls.txt -t 100 --duration 3600 -s --mode autounderstand --use-model --report report.html
```

## Use the cleaned URLs with domain for scanning with Aritificial Intelligence and Machine Learning Mode
- This will create testphp.vulnweb.com.pkl trained model
- You model should always be in few kbs and mbs
  
```bash
python xssscanadv.py -d domain testphp.vulnweb.com -l testphp_vulnweb_com_cleaned_urls.txt -t 100 --duration 3600 -s --mode autounderstand --use-model --report report.html
```

## Perform a deep crawl using CommonCrawl and Wayback Machine
```bash
python xssscanadv.py -d http://testphp.vulnweb.com --deepcrawl --report myreport.html
```

## Use the deep crawled URLs for scanning
```bash
python xssscanadv.py -l found_links.txt -t 100 --duration 3600 -s --mode autounderstand --use-model --report report.html
```


## Screenshots
![AI-ML XSS Pic1](https://i.ibb.co/wd5zmmd/ai-ml-xss-pic1.png)
![AI-ML XSS Pic2](https://i.ibb.co/d4jTvD9/ai-ml-xss-pic2.png)

## Training for Machine Learning
- We have initiated Auto Understand Mode for Random Forest Model and Neural Language Processing Capabilities
- This will train the model, train models only have tweaked algorithms like x and y, 0 and 1
- We have raw data with training_data.csv, that imported raw data
- Then we have NLP check to analysis and correct the data
- We have corellated with the Machine Learning Auto Understand Mode for Extreme Fine Tuning
- Once the software stops
- Congratulations! You have trained the model,
- To use model, use --use-model
- Bring down WAF, IDS, IPS and Everything basically
- Enjoy!
![AI-ML XSS Pic3](https://i.ibb.co/YPGsQhG/ai-ml-xss-pic3.png)

## Trained model is ready to use with --mode autounderstand for Artificial Intelligence
![AI-ML XSS Pic4](https://i.ibb.co/zxM9snW/ai-ml-xss-pic4.png)

## High Accuracy and Low Loss Indicating Effective Learning
- High Accuracy: The accuracy remains consistently high, around 98.7% to 99.0%, throughout the training epochs. This indicates that the model is performing well on the training data.
- Low Loss: The loss values are relatively low, starting from 0.1046 and decreasing to around 0.0423 - 0.0509. Lower loss values indicate that the model's predictions are close to the actual values.
- Stability: The accuracy and loss values do not fluctuate wildly between epochs, suggesting that the model is not overfitting and is learning the patterns in the data effectively.


## Trained Model of .pkl file and Pkl File Viewer
- The trained model file is provided as testphp.vulnweb.com.pkl.
- High performance is achieved with the testphp.vulnweb.com.pkl file.
- Use pklfileview.py to view the .pkl file and evaluate the model's performance.
- Use the --domain option to change the .pkl file for more efficient prediction and attack on the target.
- For example, you can use myownname.pkl --domain myownname.com. I hope you understand the rest of the idea.

