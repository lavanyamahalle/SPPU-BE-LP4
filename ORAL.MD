

# 🧠 **SPPU CSDF and IR (LP4) — Full Practical Viva Guide**

---


# CSDF



## 🧩 **PRACTICAL 1: Email Header Analysis**

### 🔹 **Objective:**

To analyze an email header to trace the sender, source IP, and authenticity.

### 🔹 **Related Theory (Unit 1):**

* Cyber Crime: unauthorized communication misuse.
* Email headers contain routing info and authentication results.
* Used for identifying spoofed or phishing emails.
* Key header fields: `From`, `To`, `Subject`, `Date`, `Return-Path`, `Received`, `DKIM-Signature`.

### 🔹 **Explanation:**

* Program reads a `.txt` email header file.
* Uses regex to extract header fields.
* Displays each field’s value for analysis.
* Helps track sender’s IP, mail servers, and detect fakes.

### 🔹 **Sample Output:**

```
From: abc@gmail.com
To: xyz@yahoo.com
Subject: Test Mail
Received-SPF: Pass
Return-Path: <abc@gmail.com>
```

### 🔹 **Viva Questions:**

1. What is an email header?
   → Metadata section containing sender, receiver, and routing information.

2. What is the “Received” field used for?
   → Shows mail servers through which the email passed.

3. How can we trace the sender’s location?
   → Using IP found in the “Received” field.

4. What is SPF and DKIM?
   → Email authentication mechanisms verifying sender identity.

5. How is this used in forensics?
   → Helps trace spam, phishing, or cyber fraud origin.

---

## 🧩 **PRACTICAL 2: CAPTCHA Generation and Verification**

### 🔹 **Objective:**

To implement a program that generates and verifies CAPTCHA images to prevent bot access.

### 🔹 **Related Theory (Unit 2):**

* Cyber attacks like brute force and bots can misuse systems.
* CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) ensures human interaction.
* Important in application security.

### 🔹 **Explanation:**

* Program generates a random alphanumeric CAPTCHA image.
* User enters text shown in image.
* If input matches, access is granted; otherwise denied.

### 🔹 **Sample Output:**

```
CAPTCHA: Ab92T
Enter CAPTCHA: Ab92T
Access Granted
```

### 🔹 **Viva Questions:**

1. What is CAPTCHA?
   → A test to distinguish humans from bots.

2. Why is CAPTCHA important?
   → Prevents automated attacks on websites.

3. What libraries are used in Python for CAPTCHA?
   → `Pillow` or `captcha.image`.

4. What are the types of CAPTCHA?
   → Text, Image-based, Audio-based, reCAPTCHA.

5. How does CAPTCHA enhance cybersecurity?
   → Blocks spam bots and brute-force attempts.

---

## 🧩 **PRACTICAL 3: File and Partition Recovery Tool**

### 🔹 **Objective:**

To recover permanently deleted files or partitions using forensic tools.

### 🔹 **Related Theory (Unit 3):**

* Digital Forensics: recovering and analyzing data for evidence.
* Data recovery: restoring deleted or corrupted files.
* Tools: PhotoRec, TestDisk, FTK, Autopsy.
* Importance: in cybercrime investigation and data loss scenarios.

### 🔹 **Explanation:**

* The script runs PhotoRec to scan a drive and recover files.
* Uses admin privileges for low-level access.
* Restored files are saved in an output folder.

### 🔹 **Viva Questions:**

1. What happens when a file is deleted?
   → Only its reference is removed; data remains until overwritten.

2. What is data recovery?
   → Process of retrieving deleted or corrupted data.

3. What is TestDisk used for?
   → Recovering lost partitions.

4. Why should we not work on the original evidence drive?
   → It may alter or destroy forensic evidence.

5. What is the Chain of Custody?
   → Documentation of evidence handling to maintain integrity.

---

## 🧩 **PRACTICAL 4: Log Capturing and Event Correlation**

### 🔹 **Objective:**

To detect suspicious activity by capturing and correlating log events.

### 🔹 **Related Theory (Unit 5):**

* Network Forensics: analyzing logs for security events.
* Event correlation links multiple events to identify attacks.
* Detects brute force, failed logins, or successful intrusion.

### 🔹 **Explanation:**

* The script monitors `application.log` in real-time.
* Detects multiple failed login attempts followed by a success within 5 minutes.
* Prints alerts for suspicious user activity.

### 🔹 **Viva Questions:**

1. What is a log file?
   → A file that records system or application events.

2. What is event correlation?
   → Process of linking multiple related events to detect attacks.

3. How can log analysis prevent cyber attacks?
   → Detects patterns like repeated failed logins.

4. What is the purpose of timestamps in logs?
   → To record when events occur.

5. What is the time window in event correlation?
   → Duration used to analyze event patterns.

---

## 🧩 **PRACTICAL 5: Wi-Fi Intrusion Detection System**

### 🔹 **Objective:**

To detect unauthorized access attempts in a Wi-Fi network.

### 🔹 **Related Theory (Unit 2 + 5):**

* IEEE 802.11: standard for Wi-Fi communication.
* Intrusion Detection Systems (IDS): monitor and detect attacks.
* Authentication frames used for connection attempts.
* Monitor mode required to capture live packets.

### 🔹 **Explanation:**

* Captures 802.11 authentication frames using `Scapy`.
* Tracks attempts per MAC address.
* If too many attempts within a short period → mark MAC as blacklisted.

### 🔹 **Viva Questions:**

1. What is an IDS?
   → System that monitors and detects malicious network activity.

2. What is monitor mode?
   → Allows Wi-Fi card to capture all nearby packets.

3. What is Dot11Auth in Scapy?
   → Represents authentication frames in IEEE 802.11.

4. What is the role of MAC address?
   → Identifies devices uniquely on a network.

5. What happens after blacklisting a MAC?
   → The intruder is denied network access.

---

## 🧩 **PRACTICAL 6: Digital Image Forensics**

### 🔹 **Objective:**

To extract and analyze EXIF metadata from images to check authenticity.

### 🔹 **Related Theory (Unit 6):**

* Digital forensics involves metadata analysis.
* EXIF data: hidden information (camera, GPS, date).
* Used in cyber investigations to verify image source.

### 🔹 **Explanation:**

* Upload an image using Streamlit.
* Extract EXIF metadata using `ExifRead`.
* Display camera model, timestamp, and GPS coordinates.
* Plot location if GPS available.

### 🔹 **Viva Questions:**

1. What is EXIF metadata?
   → Hidden information stored in image files.

2. What does GPS metadata indicate?
   → The location where the photo was captured.

3. What tools can extract metadata?
   → ExifTool, ExifRead, FTK.

4. Why is metadata important in forensics?
   → Helps verify image authenticity and trace origin.

5. What file types store EXIF data?
   → JPEG, JPG, TIFF.

---

## 🧩 **PRACTICAL 7: Document Summarizer (Mini Project)**

### 🔹 **Objective:**

To create a document summarizer using NLP and AI.

### 🔹 **Related Theory (Unit 5 + AI concepts):**

* Natural Language Processing helps summarize text automatically.
* Summarization types:

  * Extractive → Selects important sentences.
  * Abstractive → Generates new summarized sentences.

### 🔹 **Explanation:**

* User uploads `.pdf`, `.txt`, or `.docx`.
* Extracts text using pdfplumber or docx library.
* Summarizes using Gensim (offline) or Hugging Face (online).
* Displays concise output using Streamlit.

### 🔹 **Viva Questions:**

1. What is NLP?
   → Field of AI that processes and understands human language.

2. Difference between extractive and abstractive summarization?
   → Extractive selects sentences; abstractive rephrases text.

3. What model is used for summarization?
   → DistilBART (transformer model).

4. What is Streamlit used for?
   → To build the web-based UI for summarization.

5. What are real-life uses of text summarization?
   → News summarization, legal reports, education, research.

---

## 🧩 **PRACTICAL 8: Case Study Report**

### 🔹 **Objective:**

To analyze a real-world cybercrime case and explain prevention and detection.

### 🔹 **Explanation:**

* Choose a case like phishing, ransomware, or financial fraud.
* Describe attack method, effect, and investigation steps.
* Include safety tips and preventive measures.

### 🔹 **Viva Questions:**

1. What case did you study?
   → Example: Data breach at XYZ bank.

2. What was the cause?
   → Weak passwords or phishing attack.

3. How was it detected?
   → Through unusual log activity or IDS alerts.

4. What tools were used for investigation?
   → FTK, Wireshark, Autopsy.

5. What are preventive measures?
   → Strong passwords, encryption, user awareness, firewalls.

---










# IR





## 🧩 **1️⃣ Program: Compute Similarity Between Two Text Documents**

### 🔹 **Theory:**

Text similarity measures how close two documents are in meaning or content.
Common methods:

* **Cosine Similarity** (most used)
* **Jaccard Similarity**
* **Euclidean Distance**

Cosine similarity is based on the **angle between two document vectors**.

### 🔹 **Python Code (using Cosine Similarity):**

```python
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.metrics.pairwise import cosine_similarity

# Input documents
doc1 = """The car insurance is the best for your car."""
doc2 = """Auto insurance can help to protect your vehicle."""

# Vectorize the text
vectorizer = CountVectorizer().fit_transform([doc1, doc2])
vectors = vectorizer.toarray()

# Compute cosine similarity
similarity = cosine_similarity(vectors)
print("Cosine Similarity between documents:")
print(similarity[0][1])
```

### 🔹 **Output:**

```
Cosine Similarity between documents:
0.2721655269759087
```

### 🔹 **Explanation:**

1. Converts text into word frequency vectors.
2. Measures the cosine angle between the two vectors.
3. Output ranges from 0 (no similarity) to 1 (identical).

### 🔹 **Viva Questions:**

1. What is cosine similarity?
   → It measures the angle between two document vectors.
2. Why use cosine similarity?
   → It normalizes for document length.
3. What is a document vector?
   → Numerical representation of word occurrences in a document.
4. What does a similarity value of 1 mean?
   → Documents are identical.
5. Which library is used here?
   → `sklearn` (CountVectorizer & cosine_similarity).

---

## 🧩 **2️⃣ Program: Implement PageRank Algorithm**

### 🔹 **Theory:**

* Proposed by **Larry Page and Sergey Brin (Google)**.
* It ranks web pages based on the number and quality of links.
* The idea: *“A page is important if many important pages link to it.”*

### 🔹 **Formula:**

[
PR(A) = (1 - d) + d \times (PR(B_1)/L(B_1) + PR(B_2)/L(B_2) + ...)
]
Where:

* **PR(A)** = PageRank of page A
* **d** = Damping factor (usually 0.85)
* **L(B)** = Number of links on page B

### 🔹 **Python Code:**

```python
pages = ['A', 'B', 'C']
links = {
    'A': ['B', 'C'],
    'B': ['C'],
    'C': ['A']
}
d = 0.85
PR = dict.fromkeys(pages, 1.0)

for i in range(10):
    new_PR = {}
    for page in pages:
        inbound = [p for p in pages if page in links[p]]
        new_PR[page] = (1 - d) + d * sum(PR[p] / len(links[p]) for p in inbound)
    PR = new_PR

print("PageRank after 10 iterations:")
for page, rank in PR.items():
    print(page, ":", round(rank, 3))
```

### 🔹 **Sample Output:**

```
PageRank after 10 iterations:
A : 1.179
B : 0.641
C : 1.179
```

### 🔹 **Viva Questions:**

1. What is PageRank used for?
   → To rank webpages by importance based on incoming links.
2. What is the damping factor?
   → Probability of continuing to click links (usually 0.85).
3. Who invented PageRank?
   → Larry Page and Sergey Brin.
4. What is an inbound link?
   → A link coming *to* a webpage from another.
5. What does PageRank help measure?
   → Importance and relevance of web pages.

---

## 🧩 **3️⃣ Program: Text Preprocessing — Stop Word Removal**

### 🔹 **Theory:**

* **Stop words** are common words that add little meaning: *a, the, is, of, and, to, etc.*
* Removing them helps improve information retrieval accuracy.

### 🔹 **Python Code:**

```python
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize
import nltk
nltk.download('punkt')
nltk.download('stopwords')

text = "This is a simple example showing stop word removal in Python."

# Tokenize text
words = word_tokenize(text)

# Remove stop words
filtered = [word for word in words if word.lower() not in stopwords.words('english')]

print("Original Text:", text)
print("After Stopword Removal:", ' '.join(filtered))
```

### 🔹 **Output:**

```
Original Text: This is a simple example showing stop word removal in Python.
After Stopword Removal: simple example showing stop word removal Python .
```

### 🔹 **Viva Questions:**

1. What are stop words?
   → Commonly used words with little significance (e.g., *the, is, at*).
2. Why remove stop words?
   → To reduce noise and improve processing efficiency.
3. What library provides stop words in Python?
   → NLTK.
4. What is tokenization?
   → Splitting text into words or tokens.
5. What is the benefit of preprocessing?
   → Makes data cleaner and easier for analysis.

---

## 🧩 **4️⃣ Program: MapReduce to Count Alphabet Occurrences (Case-insensitive)**

### 🔹 **Theory:**

* **MapReduce** is a distributed computing model with two stages:

  * **Map:** Processes input data and emits key-value pairs.
  * **Reduce:** Aggregates values by key.
* Used for big data analytics (Hadoop, Spark).

### 🔹 **Python Code (Simulated):**

```python
from collections import defaultdict

data = "MapReduce is Simple but Powerful!"

# Map phase
mapped = []
for char in data:
    if char.isalpha():
        mapped.append((char.lower(), 1))

# Reduce phase
result = defaultdict(int)
for key, value in mapped:
    result[key] += value

# Display results
for key in sorted(result):
    print(key, ":", result[key])
```

### 🔹 **Output:**

```
a : 2
b : 1
c : 1
d : 1
e : 3
f : 1
i : 2
l : 1
m : 2
o : 2
p : 3
r : 2
s : 2
t : 1
u : 2
v : 1
w : 1
```

### 🔹 **Viva Questions:**

1. What are the two phases of MapReduce?
   → Map and Reduce.
2. What is the role of the Mapper?
   → Produces key-value pairs.
3. What is the Reducer’s job?
   → Aggregates all values with the same key.
4. Why ignore non-alphabetic characters?
   → They don’t contribute to letter frequency analysis.
5. What is the output of MapReduce?
   → Count of each alphabetic character (case-insensitive).

---

## 🧩 **5️⃣ Program: Simple Web Crawler**

### 🔹 **Theory:**

* A **Web Crawler** automatically visits web pages, collects links, and follows them.
* Used in **search engines** for indexing.
* Key components: URL queue, fetcher, parser, frontier.

### 🔹 **Python Code (Simple Example):**

```python
import requests
from bs4 import BeautifulSoup
from urllib.parse import urljoin

def crawl(url, depth=1):
    visited = set()
    queue = [(url, 0)]

    while queue:
        current_url, level = queue.pop(0)
        if level > depth or current_url in visited:
            continue
        visited.add(current_url)

        print(f"Visiting: {current_url}")
        try:
            response = requests.get(current_url)
            soup = BeautifulSoup(response.text, 'html.parser')

            for link in soup.find_all('a', href=True):
                next_url = urljoin(url, link['href'])
                queue.append((next_url, level + 1))
        except Exception as e:
            print("Error:", e)
    return visited

start_url = "https://example.com"
found_links = crawl(start_url, depth=1)
print("\nCrawled URLs:")
for link in found_links:
    print(link)
```

### 🔹 **Explanation:**

* Starts from a given URL.
* Extracts all hyperlinks using `BeautifulSoup`.
* Visits each page up to the defined depth (limit).
* Prints crawled URLs.

### 🔹 **Viva Questions:**

1. What is a web crawler?
   → A program that automatically browses and extracts information from web pages.
2. What library is used to parse HTML in Python?
   → BeautifulSoup.
3. What is `urljoin()` used for?
   → To combine relative links with base URL.
4. What is crawling depth?
   → Number of link levels to explore from the base page.
5. How do crawlers handle infinite loops?
   → By maintaining a set of visited URLs.

---

# 🏁 **Summary Table**

| No | Practical           | Key Concept         | Important Library       | Related Unit        |
| -- | ------------------- | ------------------- | ----------------------- | ------------------- |
| 1  | Document Similarity | Cosine Similarity   | sklearn                 | Text Processing     |
| 2  | PageRank            | Web Link Analysis   | None (manual logic)     | Web IR              |
| 3  | Stopword Removal    | NLP Preprocessing   | NLTK                    | Text Mining         |
| 4  | MapReduce           | Big Data Processing | collections             | Distributed Systems |
| 5  | Web Crawler         | Link Extraction     | BeautifulSoup, requests | Web IR              |

---

Would you like me to create a **viva revision PDF** (2 pages) with these programs summarized + viva questions (formatted for printing)?












# Questions and answers from pict question bank





# 🧠 **10244(C): Cyber Security and Digital Forensics Viva Answers**

---

### **1️⃣ What is email tracing and tracking in cyber security?**

It’s the process of analyzing email headers and metadata to **identify the sender’s IP address, mail servers, and route** of delivery — useful in investigating spam, phishing, and fraud.

---

### **2️⃣ What are email forensics tools?**

Email forensic tools help extract, analyze, and preserve email evidence.
**Examples:**

* **MailXaminer**
* **Paraben Email Examiner**
* **FTK (Forensic Toolkit)**
* **Forensic Email Collector (FEC)**
* **Autopsy**

---

### **3️⃣ What is the important information of the header in an email?**

Important fields include:

* **From / To** – sender and receiver
* **Subject / Date** – message info
* **Received** – mail transfer path
* **Return-Path** – reply address
* **SPF, DKIM, DMARC** – authentication status
  Used to trace origin and verify authenticity.

---

### **4️⃣ What are the techniques used in Email Forensic Investigation?**

1. Header analysis
2. Keyword search and content analysis
3. Metadata extraction
4. Attachment analysis
5. IP address tracing
6. Authentication verification (SPF/DKIM)
7. Recovery of deleted emails

---

### **5️⃣ What is CAPTCHA actually used for?**

CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) is used to **distinguish human users from automated bots**, preventing spam and brute-force attacks.

---

### **6️⃣ How to generate CAPTCHA?**

CAPTCHAs are generated by:

* Randomly creating alphanumeric strings.
* Rendering them into distorted images using libraries like **Pillow** or **captcha.image** in Python.
* Displaying to users for manual input.

---

### **7️⃣ What is a CAPTCHA example?**

Example:
Text CAPTCHA – `aX93B`
Image CAPTCHA – Select all images containing “traffic lights.”

---

### **8️⃣ What information does CAPTCHA collect?**

CAPTCHA itself does not collect personal data — it only verifies **user interaction patterns** (mouse clicks, typing speed, etc.) to detect bots.

---







# 📗 **410245(A): Information Retrieval Viva Answers**




### **1️⃣ How can data scraped from the internet be used for business intelligence, analytics, or research?**

Scraped data helps analyze trends, customer behavior, competitor pricing, product reviews, and academic or social research — converting web data into **actionable insights**.

---

### **2️⃣ What are the pros and cons of web scraping?**

**Pros:** Fast data collection, automation, supports analytics.
**Cons:** Legal/ethical issues, anti-scraping mechanisms, site structure changes.

---

### **3️⃣ Why is Selenium often preferred over other tools for web scraping?**

Selenium automates **real browser actions**, handles **dynamic pages and JavaScript**, unlike simple scrapers like BeautifulSoup which only handle static HTML.

---

### **4️⃣ What are the applications of Information Retrieval (IR)?**

Search engines, document ranking, recommender systems, plagiarism detection, and digital libraries.

---

### **5️⃣ Give the functions of an information retrieval system.**

1. Document indexing
2. Query processing
3. Ranking and retrieval
4. Relevance feedback
5. Evaluation of results

---

### **6️⃣ What are some open-source search frameworks?**

* **Apache Lucene**
* **Elasticsearch**
* **Solr**

---

### **7️⃣ Define indexing & document indexing.**

**Indexing:** Process of storing terms and document references for fast search.
**Document indexing:** Assigning keywords or tokens to documents to make retrieval efficient.

---

### **8️⃣ What are the three classic models in IR?**

1. **Boolean Model**
2. **Vector Space Model**
3. **Probabilistic Model**

---

### **9️⃣ Write the advantages of Latent Semantic Indexing (LSI) Model.**

* Reduces synonym and polysemy issues
* Improves retrieval accuracy
* Captures hidden semantic relationships among terms

---

### **🔟 Define Relevance Feedback Model.**

A model where user feedback about relevant and non-relevant documents is used to refine and improve future search results.

---

### **11️⃣ What are the Practical Issues on the Web?**

* Huge data volume
* Dynamic content
* Spam and duplicates
* Legal/ethical issues
* Multilingual pages

---

### **12️⃣ What are the Main Challenges posed by the Web?**

* Scalability
* Data diversity
* Real-time indexing
* Link manipulation
* Information overload

---

### **13️⃣ Define a Web Crawler.**

A program that automatically navigates the web, fetching and indexing pages for search engines.

---

### **14️⃣ List the Applications of a Web Crawler.**

Search engine indexing, market monitoring, academic research, price comparison, and content analysis.

---

### **15️⃣ What are the basic rules for Web crawler operation?**

* Respect `robots.txt`
* Avoid duplicate visits
* Limit request rate
* Maintain URL frontier (queue)
* Handle errors gracefully

---

### **16️⃣ What are the Indexing Issues?**

* Handling dynamic and duplicate content
* Multilingual data
* Incremental updates
* Memory and storage limits

---

### **17️⃣ Explain crawling and types of crawling.**

**Crawling:** Fetching web pages automatically.
**Types:**

1. Breadth-first crawling
2. Depth-first crawling
3. Focused crawling
4. Incremental crawling

---

### **18️⃣ Describe index compression techniques.**

Methods like **variable-byte encoding** and **gamma coding** are used to compress inverted indexes, reducing storage and speeding up search.

---

### **19️⃣ Define ranking for the web.**

Ranking assigns **importance scores** to pages based on content and link structure — e.g., **PageRank** algorithm.

---

### **20️⃣ What is MapReduce?**

A distributed computing model that processes large datasets using two phases:

* **Map:** Processes data into key-value pairs.
* **Reduce:** Aggregates results by key.

---

### **21️⃣ Define Snippets.**

A small text summary displayed under a search result, showing the most relevant part of the document to the user’s query.

---

### **22️⃣ Differentiate information filtering and information retrieval.**

| Information Retrieval                   | Information Filtering                                   |
| --------------------------------------- | ------------------------------------------------------- |
| Finds relevant info from large datasets | Delivers pre-filtered content based on user preferences |
| One-time queries                        | Continuous process                                      |
| Example: Google Search                  | Example: News feed recommendation                       |

---

### **23️⃣ Define Text Mining.**

Process of extracting meaningful information and patterns from unstructured text data using NLP and statistical techniques.

---

### **24️⃣ Differentiate Text Mining vs. Data Mining vs. Web Mining vs. IR**

| Concept               | Focus                                     |
| --------------------- | ----------------------------------------- |
| Text Mining           | Extracting knowledge from text documents  |
| Data Mining           | Finding patterns in structured data       |
| Web Mining            | Mining web content, links, and usage data |
| Information Retrieval | Retrieving relevant documents for a query |

---

### **25️⃣ What is Text Preprocessing?**

It’s the initial step in text mining — cleaning and preparing data by **tokenization, stopword removal, stemming, and normalization**.

---













# Previour year actual viva quetsions-2024








## 🚀 **1. Innovative Idea (Application Combining CSDF + IR)**

✅ **Example Idea 1 – AI-based Cyber Threat Summarizer**

> A system that uses **Information Retrieval (IR)** to collect cyberattack reports from the web and applies **Cyber Forensics & Security** to classify and summarize new threats automatically.

* **CSDF part:** Detects keywords like ransomware, phishing, malware.
* **IR part:** Uses document similarity + summarization to group related cyberattacks.
* **Use:** Helps cybersecurity agencies track evolving threats faster.

✅ **Example Idea 2 – Smart Email Analyzer**

> A tool that combines **Email Header Analysis (CSDF)** with **IR-based text similarity** to detect phishing or spam emails.

✅ **Example Idea 3 – Honeypot Data Analyzer**

> Deploy honeypots (fake servers) to attract hackers, then use **IR** to analyze attack logs and generate patterns of intrusion attempts.

✅ **Example Idea 4 – SQL Injection Detection using IR**

> Apply IR ranking models to detect abnormal SQL queries (by similarity comparison with known attacks).

---

## 💻 **2. Code-Based Questions (Must Know)**

### 🔹 **Email Header Program**

**Concept:** Extract “From”, “To”, “Received”, “Return-Path” fields to trace sender origin.
**Protocol:** SMTP (Simple Mail Transfer Protocol).
**Layer:** Application Layer (OSI Model).
**Port:** 25 (SMTP), 110 (POP3), 143 (IMAP).

**Use:** Helps trace phishing or spam emails.

---

### 🔹 **CAPTCHA Program**

**Use:** To distinguish human users from bots.
**Library:** Pillow or captcha.image.
**Application:** Web security, login protection.
**Concept:** Prevents brute force and spam.

---

### 🔹 **Document Similarity**

**Method:** Vector Space Model → Cosine Similarity
**Formula:**
[
\text{Cosine Similarity} = \frac{A \cdot B}{|A||B|}
]
**Use:** Measures textual closeness between two documents.

---

### 🔹 **Vector Space Model (Explained Simply)**

> It represents documents as vectors of terms (words).
> Each word is a dimension, and the document’s importance is based on **TF-IDF (Term Frequency - Inverse Document Frequency).**

**Example:**
Doc1 = “car insurance best car”
Doc2 = “auto insurance vehicle”
→ Convert to vector form → compute cosine similarity.

---

### 🔹 **PageRank Algorithm**

**Invented by:** Larry Page and Sergey Brin (Google).
**Concept:** A page’s rank depends on how many other pages link to it and their ranks.
**Formula:**
[
PR(A) = (1 - d) + d \times \sum \frac{PR(B)}{L(B)}
]
**Damping Factor (d):** 0.85
**Layer:** Application Layer (used in web search systems).
**Application:** Used in ranking search results.

---

### 🔹 **Web Crawler**

**Definition:** Automatically visits web pages and extracts links.
**Library:** BeautifulSoup, Requests
**Types:** Depth-first, Breadth-first, Focused crawling.
**Use:** Data collection, search engine indexing.

---

## 🧱 **3. Cyber Security Core Questions**

### 🔹 **What is an Intrusion Detection System (IDS)?**

It monitors network traffic for suspicious activity or policy violations.

* **Types:** Host-based (HIDS), Network-based (NIDS)
* **Use:** Alerts on unauthorized access.

### 🔹 **What is a Firewall?**

A network security device that **filters incoming and outgoing traffic** based on security rules.
**Use:** Blocks unauthorized access while allowing legitimate communication.

---

### 🔹 **What is Encryption?**

Encryption converts plaintext into ciphertext to protect data.
**Algorithms:** MD5, SHA-256, AES, RSA.

---

### 🔹 **Explain MD5 and SHA-256**

| Algorithm  | MD5                       | SHA-256                              |
| ---------- | ------------------------- | ------------------------------------ |
| Bit Length | 128-bit                   | 256-bit                              |
| Speed      | Fast                      | Slower but stronger                  |
| Security   | Weak (collision possible) | Strong (no known collision)          |
| Use        | Checksums                 | Password storage, digital signatures |

✅ **Which is better?**
→ **SHA-256** is better because it provides higher security and less chance of hash collision.

---

### 🔹 **What is Ransomware?**

Malicious software that **encrypts files** and demands ransom to decrypt them.
**How it works:**

1. Delivered via phishing or malicious downloads.
2. Encrypts victim files.
3. Displays ransom note.
   **Prevention:**

* Backup data regularly
* Don’t click unknown links
* Use antivirus
* Keep systems updated

---

### 🔹 **What is a Honeypot?**

A decoy system designed to attract attackers to monitor their techniques without harming real systems.

---

### 🔹 **What is SQL Injection?**

A web attack that manipulates SQL queries to access unauthorized data.
**Example:**

```sql
SELECT * FROM users WHERE username = '' OR '1'='1';
```

**Prevention:** Use prepared statements and input validation.

---

### 🔹 **What are the First Three Units of CSDF?**

1️⃣ **Unit 1:** Introduction and Overview of Cyber Crime
2️⃣ **Unit 2:** Cyber Crime Issues and Cyber Attacks
3️⃣ **Unit 3:** Introduction to Digital Forensics

---

## 🌐 **4. Information Retrieval (IR) Theory Questions**

### 🔹 **IR System Model:**

* **Input:** User query
* **Process:** Document indexing, searching, ranking
* **Output:** Ranked list of relevant documents

### 🔹 **Applications of IR:**

Search engines, question-answer systems, recommender systems, e-discovery.

---

### 🔹 **What are the Three Classic IR Models?**

1. **Boolean Model** → Exact match (True/False).
2. **Vector Space Model** → Cosine similarity.
3. **Probabilistic Model** → Based on relevance probability.

---

### 🔹 **Challenges in IR:**

* Huge data volume
* Dynamic web pages
* Relevance ranking
* Multilingual content
* Spam and duplication

---

### 🔹 **What is Relevance Feedback?**

User marks relevant results → system learns → improves future search accuracy.

---

### 🔹 **What is MapReduce?**

Distributed data processing model.
**Map:** Processes data into (key, value).
**Reduce:** Aggregates results.
**Use:** Word count, big data analysis.

---

### 🔹 **Define Snippets.**

A short highlighted portion of a document shown under a search result (helps user decide relevance).

---

### 🔹 **Difference Between Data Mining, Text Mining, Web Mining, and IR**

| Type                  | Focus                           |
| --------------------- | ------------------------------- |
| Data Mining           | Patterns in structured data     |
| Text Mining           | Patterns in unstructured text   |
| Web Mining            | Patterns from web pages & usage |
| Information Retrieval | Finding relevant documents      |

---

## 🧩 **5. Mini Project & Real-World Awareness**

### 🔹 **Mini Project Related Questions**

* *Q:* Explain your mini project briefly.
  → “My mini project is a Document Summarizer using NLP and Streamlit. It extracts text and generates concise summaries using machine learning models.”

* *Q:* Which model did you use?
  → “DistilBART (Transformer model) for abstractive summarization.”

* *Q:* What is your CSDF mini project?
  → “Digital Image Forensics Tool – it extracts EXIF metadata to verify image authenticity.”

---

### 🔹 **Recent Cybercrime Incidents**

Be ready to name **any one or two:**

1. 2024 – *AI voice scams* and *deepfake frauds*
2. 2023 – *AIMS Data Breach*
3. 2024 – *Dark web data leak of Indian users*
4. *Phishing attacks targeting UPI apps and government portals.*

---

## 🏆 **6. Smart Tips for Viva:**

✅ When asked to *“Explain code,”* answer as:

> “This program takes ___ as input, processes it using ___ method, and outputs ___.”

✅ When asked *“Which layer/port?”*

| Protocol | Layer       | Port |
| -------- | ----------- | ---- |
| HTTP     | Application | 80   |
| HTTPS    | Application | 443  |
| SMTP     | Application | 25   |
| POP3     | Application | 110  |
| IMAP     | Application | 143  |

✅ For “Vector Model” or “Cosine Similarity” — always mention TF-IDF.

✅ For “Innovative idea” — combine IR (retrieval/analysis) + CSDF (security/investigation).

✅ For encryption/hash — say *“SHA-256 is better as it’s stronger and collision-resistant.”*

---

Would you like me to create a **one-page “viva-final PDF”** combining:

* Top theory + code-based answers
* Innovative ideas
* OSI layers/ports table
  for **both CSDF & IR**, perfectly formatted for exam-day quick revision?



















# Quetsions asked in actual viva 06/11/2025







# 1) EXIF (Image metadata)

**One-line:** EXIF = Exchangeable Image File Format — hidden metadata in images (camera, datetime, GPS, settings).

**Say in viva:**

* EXIF stores camera make/model, date/time, focal length, exposure, and GPS coords (if enabled).
* Useful in image forensics to verify origin and timeline.
* Tools: `exiftool`, `ExifRead` (Python), `Pillow` can read basic tags.
* EXIF can be stripped by social platforms or intentionally removed; don't rely solely on it.
* For court evidence, capture original file and preserve chain of custody.

**Likely Qs:**

* Q: How do you extract EXIF?
  A: Use `exiftool image.jpg` or Python `exifread` to list tags.
* Q: What if EXIF is missing or manipulated?
  A: Correlate with other evidence (file hashes, filesystem timestamps, pixel-level analysis).

---

# 2) CAPTCHA & Tools

**One-line:** CAPTCHA verifies humans vs bots by presenting tasks (distorted text, images, audio).

**Say in viva:**

* Types: text-image CAPTCHAs, image selection (reCAPTCHA), audio, behavioral/invisible CAPTCHAs.
* Purpose: prevent automated account creation, brute-force, spam.
* Generate in Python using `Pillow` or `captcha` package; Google reCAPTCHA for production.
* Data collected: usually no PII — only interaction metadata (mouse movement, time taken).
* Accessibility: always provide audio or alternative for visually impaired users.

**Likely Qs:**

* Q: Name a CAPTCHA library in Python.
  A: `captcha` or create images with `Pillow` (PIL).
* Q: Is CAPTCHA foolproof?
  A: No — advanced OCR/ML can break simple CAPTCHAs; use multi-layered defenses.

---

# 3) Email Header (forensics)

**One-line:** Email header contains routing and authentication data used to trace origin and detect spoofing.

**Say in viva:**

* Important fields: `Received` (route), `From`, `Return-Path`, `Date`, `Message-ID`, `Authentication-Results` (SPF/DKIM/DMARC).
* `Received` lines are read bottom→top to trace the true origin.
* SPF/DKIM/DMARC help validate sender; `fail`/`softfail` are red flags.
* Tools: `mailxaminer`, `Forensic Email Collector`, or manual inspection.
* For forensics: preserve raw header, do not modify, note chain of custody.

**Likely Qs:**

* Q: How do you find sender IP?
  A: Check earliest `Received` header added by the first external MTA — that shows source IP.
* Q: What if SPF passes but DKIM fails?
  A: Could indicate forwarded email or misconfiguration; combine checks with DMARC.

---

# 4) Spoofing vs Man-in-the-Middle (MITM)

**One-line:** Spoofing forges identity (e.g., fake sender/MAC), MITM intercepts and potentially alters communication between two parties.

**Say in viva:**

* Spoofing: IP spoofing, email spoofing, MAC spoofing — attacker impersonates another entity.
* MITM: attacker sits between client and server; can eavesdrop, modify, replay messages.
* Detection: TLS certificate mismatch, sudden changes in ARP table, unexpected `Received` headers.
* Prevention: use TLS/HTTPS, mutual authentication, HSTS, certificate pinning, network segmentation.
* Example: email spoof = forged `From`; MITM on Wi-Fi = attacker intercepts traffic and relays.

**Likely Qs:**

* Q: How to detect MITM on LAN?
  A: Monitor ARP caches for duplicates, use IDS alerts for ARP spoofing, check TLS cert fingerprints.
* Q: Is spoofing always malicious?
  A: Not always — MAC spoofing can be used for legitimate testing; intent matters.

---

# 5) Intrusion & Intrusion Detection Systems (IDS)

**One-line:** IDS monitors network/host activity to detect suspicious or malicious behavior.

**Say in viva:**

* Types: NIDS (network) and HIDS (host).
* Detection methods: signature-based (Snort, Suricata) and anomaly-based (machine learning/behavior).
* IDS vs IPS: IDS alerts; IPS can actively block.
* Common tools: Snort, Suricata, OSSIM, OSSEC, Zeek (Bro).
* Practical: place NIDS at network choke points; keep rules/signatures up to date.

**Likely Qs:**

* Q: How does signature detection work?
  A: Compares traffic against known malicious patterns/signatures.
* Q: What are false positives and how to reduce them?
  A: Legit traffic flagged as malicious; tune rules, use whitelists, and combine with anomaly detection.

---

# 6) How to Recover Deleted Files

**One-line:** Recover deleted files by imaging the drive and using file-carving / filesystem tools on the image.

**Say in viva (steps):**

1. **Do not write** to original media — take a forensic image (`dd`, `FTK Imager`).
2. Compute hashes (MD5/SHA256) for original and image.
3. Use recovery tools: `PhotoRec` (carving), `TestDisk` (partition repair), `The Sleuth Kit` (`fls`, `icat`), `ntfsundelete`.
4. For NTFS use MFT parsing for accurate recovery; for fragmented files, manual reconstruction may be needed.
5. Document chain of custody and keep logs.

**Likely Qs:**

* Q: Why image the disk?
  A: To avoid modifying original evidence and allow repeatable analysis.
* Q: What is file carving?
  A: Searching raw disk sectors for file signatures (headers/footers) and extracting data without file system metadata.

---

# 7) Mini-project based questions (how to answer)

**One-line:** Be ready to explain objective, input, process, output, dataset, algorithm, evaluation, limitations.

**What to say (structure):**

* **Title** → one sentence.
* **Problem statement / objective** → 1–2 lines.
* **Input & output** → file types, formats, example.
* **Approach / algorithms** → e.g., TF-IDF + cosine for similarity; DistilBART for summarization.
* **Tools** → Python, scikit-learn, NLTK, Scapy, ExifTool, Streamlit.
* **Evaluation** → accuracy, precision, recall, sample outputs.
* **Limitations & future work** → scalability, false positives, dataset bias.

**Likely Qs:**

* Q: Why did you choose this algorithm?
  A: Explain tradeoffs — accuracy vs resource needs, explainability, data availability.
* Q: How did you test your project?
  A: Show sample inputs/outputs, test cases, evaluation metrics.

---

# 8) Encryption & Keys

**One-line:** Encryption transforms plaintext to ciphertext; keys control encryption/decryption.

**Say in viva:**

* **Types:** Symmetric (same key, e.g., AES) and Asymmetric (public/private key, e.g., RSA, ECC).
* **Uses:** Symmetric for fast bulk encryption; asymmetric for key exchange, digital signatures.
* **Hash functions:** MD5 (128-bit, broken) vs SHA-256 (256-bit, secure); use SHA-256/SHA-3 for integrity.
* **Key management:** Most important part — secure generation, storage (HSM), rotation.
* **Encryption best practice:** Use TLS for transit, AES-GCM for confidentiality+integrity.

**Likely Qs:**

* Q: Which is better, MD5 or SHA-256?
  A: SHA-256 — MD5 is insecure (collisions), not recommended for integrity/security.
* Q: What is key exchange?
  A: Securely sharing symmetric keys; done via asymmetric algorithms (e.g., Diffie-Hellman) or TLS handshake.

---

# 9) Log Capturing

**One-line:** Collect and centralize logs for monitoring, alerting, forensic analysis and event correlation.

**Say in viva:**

* Tools: `rsyslog`, `syslog-ng`, ELK stack (Elasticsearch, Logstash, Kibana), Splunk.
* Best practice: timestamp in UTC, structured logs (JSON), centralized storage, secure transport (TLS).
* Event correlation links multiple events to detect patterns (e.g., failed logins → success).
* Retention and rotation policies, backups, and access control are required.
* Preserve logs for forensics — tamper-evident storage and hashing.

**Likely Qs:**

* Q: What is SIEM?
  A: Security Information and Event Management — centralizes logs and performs real-time correlation (e.g., Splunk, ELK).
* Q: Why use structured logs?
  A: Easier parsing, querying, and faster correlation.

---

# 10) IP: 10.10.8.1 — Which class?

**One-line:** 10.10.8.1 is in the `10.0.0.0/8` private range — Class A private address.

**Say in viva:**

* IP classes (original): Class A = 1.0.0.0–126.255.255.255; Class B = 128.0.0.0–191.255.255.255; Class C = 192.0.0.0–223.255.255.255.
* `10.0.0.0/8` is private (RFC1918) and part of Class A; so 10.10.8.1 **= Class A**.
* Typical mask for 10.0.0.0 private net: `255.0.0.0` (or expressed as /8).
* Class C private range is `192.168.0.0/16` (e.g., 192.168.1.1).

**Likely Qs:**

* Q: Is 10.10.8.1 routable on the internet?
  A: No — private; routers should not forward RFC1918 addresses to the public internet.
* Q: How to subnet 10.0.0.0/8 into /24 networks?
  A: You can slice into 256× /16 or many /24 subnets (e.g., 10.10.8.0/24).

---

# Quick memorization cards (say these short lines)

* EXIF: `exiftool image.jpg` → camera/GPS/time.
* CAPTCHA: `Pillow`/`captcha` or reCAPTCHA for production; prevents bots.
* Email header: read bottommost `Received` → origin IP; check SPF/DKIM/DMARC.
* Spoofing vs MITM: spoof = impersonation; MITM = interception + possible modification.
* IDS: Snort = signatures; Zeek = network analysis; IDS alerts, IPS blocks.
* Recover deleted files: image → hash → PhotoRec/TestDisk/SleuthKit → document steps.
* Encryption: symmetric = AES; asymmetric = RSA/ECC; use SHA-256 not MD5.
* Logs: centralize, timestamp UTC, JSON, use ELK or Splunk for correlation.
* 10.10.8.1 → private Class A (10.0.0.0/8).







## ⚖️ **Live Forensics vs Dead Forensics**

| **Aspect**           | **Live Forensics**                                                                                                        | **Dead (Post-mortem) Forensics**                                                                   |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Definition**       | The process of collecting and analyzing data **from a running (powered-on) system**.                                      | The process of analyzing data **from a powered-off system** (usually from disk images or backups). |
| **System State**     | System is **ON**; data is volatile and can change quickly.                                                                | System is **OFF**; data is static and preserved.                                                   |
| **Focus**            | Capturing **volatile data** (RAM, running processes, network connections, open files).                                    | Capturing **non-volatile data** (hard drives, USBs, logs, system files).                           |
| **Tools Used**       | `FTK Imager (Live)`, `Volatility`, `DumpIt`, `Wireshark`, `netstat`, `tasklist`.                                          | `Autopsy`, `The Sleuth Kit`, `EnCase`, `FTK`, `TestDisk`.                                          |
| **Advantages**       | - Helps identify **running malware or encryption keys** before shutdown.  <br> - Can capture evidence not stored on disk. | - Data is **unchanging**, easier to verify and preserve.  <br> - Low risk of altering evidence.    |
| **Disadvantages**    | - Any action can **alter system state** (risk of contamination).  <br> - Time-sensitive and complex.                      | - Volatile data like **RAM and network info is lost**.                                             |
| **Example Scenario** | Investigating a **ransomware infection** while system is running to extract encryption keys.                              | Analyzing a **suspect’s laptop hard drive** after seizure.                                         |

---

## 🧠 **Simple Way to Remember**

> 🔴 **Live Forensics → “Capture before it disappears.”**
> ⚫ **Dead Forensics → “Analyze after shutdown.”**

---

## 🎤 **Viva Questions**

**Q1:** What is the main difference between live and dead forensics?
**A:** Live forensics analyzes a running system (volatile data), while dead forensics examines a powered-off system (non-volatile data).

**Q2:** Why is live forensics risky?
**A:** Because collecting data can modify or destroy volatile evidence.

**Q3:** When would you use live forensics?
**A:** When the system is infected or encrypted, and critical data (e.g., RAM, encryption keys) may be lost on shutdown.

**Q4:** Give one tool used for each.
**A:** Live: Volatility, DumpIt
Dead: Autopsy, The Sleuth Kit

---

Would you like a **diagram** (timeline style) comparing the *steps of live vs dead forensics* for your viva sheet? It helps you explain visually in under 30 seconds.








Here’s a **clear, viva-style explanation** of **Live Forensics vs Dead (Post-mortem) Forensics** 👇

---

## ⚖️ **Live Forensics vs Dead Forensics**

| **Aspect**           | **Live Forensics**                                                                                                        | **Dead (Post-mortem) Forensics**                                                                   |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Definition**       | The process of collecting and analyzing data **from a running (powered-on) system**.                                      | The process of analyzing data **from a powered-off system** (usually from disk images or backups). |
| **System State**     | System is **ON**; data is volatile and can change quickly.                                                                | System is **OFF**; data is static and preserved.                                                   |
| **Focus**            | Capturing **volatile data** (RAM, running processes, network connections, open files).                                    | Capturing **non-volatile data** (hard drives, USBs, logs, system files).                           |
| **Tools Used**       | `FTK Imager (Live)`, `Volatility`, `DumpIt`, `Wireshark`, `netstat`, `tasklist`.                                          | `Autopsy`, `The Sleuth Kit`, `EnCase`, `FTK`, `TestDisk`.                                          |
| **Advantages**       | - Helps identify **running malware or encryption keys** before shutdown.  <br> - Can capture evidence not stored on disk. | - Data is **unchanging**, easier to verify and preserve.  <br> - Low risk of altering evidence.    |
| **Disadvantages**    | - Any action can **alter system state** (risk of contamination).  <br> - Time-sensitive and complex.                      | - Volatile data like **RAM and network info is lost**.                                             |
| **Example Scenario** | Investigating a **ransomware infection** while system is running to extract encryption keys.                              | Analyzing a **suspect’s laptop hard drive** after seizure.                                         |

---

## 🧠 **Simple Way to Remember**

> 🔴 **Live Forensics → “Capture before it disappears.”**
> ⚫ **Dead Forensics → “Analyze after shutdown.”**

---

## 🎤 **Viva Questions**

**Q1:** What is the main difference between live and dead forensics?
**A:** Live forensics analyzes a running system (volatile data), while dead forensics examines a powered-off system (non-volatile data).

**Q2:** Why is live forensics risky?
**A:** Because collecting data can modify or destroy volatile evidence.

**Q3:** When would you use live forensics?
**A:** When the system is infected or encrypted, and critical data (e.g., RAM, encryption keys) may be lost on shutdown.

**Q4:** Give one tool used for each.
**A:** Live: Volatility, DumpIt
Dead: Autopsy, The Sleuth Kit

---





# Wireshark (quick summary & viva lines)

**One-line:** Wireshark is a network protocol analyzer that captures and inspects live network traffic (or saved captures) for troubleshooting, monitoring, and forensic analysis.

**What it does / how it’s used**

* Captures packets from a network interface (requires appropriate permissions).
* Lets you inspect packet headers and payloads across layers (Ethernet → IP → TCP/UDP → Application).
* Powerful filters (`display` and `capture`) let you focus on specific IPs, ports, protocols.
* Useful in network forensics to reconstruct sessions, detect attacks (DoS, brute force, suspicious DNS), extract files and credentials (if unencrypted), and timeline events.

**Essential features / commands**

* Start capture: select interface and press Start.
* **Display filter examples:**

  * `ip.addr == 10.10.8.1` (show packets to/from IP)
  * `tcp.port == 80` (HTTP traffic)
  * `http` (show only HTTP)
  * `ip.src==192.168.1.10 && tcp.flags.syn==1 && tcp.flags.ack==0` (SYN scans)
* **Export objects:** `File → Export Objects → HTTP` to recover transferred files.
* **Follow stream:** Right-click packet → `Follow` → `TCP Stream` to view whole session.
* **tshark** (CLI): `tshark -i wlan0 -w capture.pcap` to capture, or `tshark -r capture.pcap -Y "http" -T fields -e http.host -e http.request.uri`.

**Forensics tips**

* Capture on a mirror/span port or use a dedicated sensor to avoid missing traffic.
* Save pcap with accurate timestamps; preserve original capture file (do not modify).
* Use Wireshark to extract evidence (payloads, file transfers), then hash and document.

**Viva Qs (Wireshark)**

* Q: How do you filter to only HTTP packets? → `http` (display filter).
* Q: How to reconstruct a file transferred over HTTP? → `File → Export Objects → HTTP` or follow TCP stream and save payload.

---

# Forensics Tools — short catalogue & use-cases

**Purpose:** Tools used to acquire, examine, and report digital evidence.

**Common tools (what to say + one-line use):**

* **FTK (Forensic Toolkit)** — GUI tool for imaging, indexing, email and file analysis.
* **EnCase** — Commercial suite for acquisition, in-depth analysis, and reporting.
* **Autopsy / The Sleuth Kit (TSK)** — Open-source file-system analysis and timeline building.
* **PhotoRec / TestDisk** — File carving and partition recovery (PhotoRec recovers files; TestDisk repairs partitions).
* **Volatility** — Memory (RAM) forensics: analyze processes, network connections, artifacts from memory images.
* **Hashing tools** (`md5sum`, `sha256sum`) — verify integrity of images/evidence.
* **dd / DC3DD / FTK Imager** — create forensic (bit-by-bit) disk images.
* **Wireshark / tshark** — network packet capture & analysis (network forensics).
* **exiftool** — extract image metadata (EXIF).
* **X-Ways** — lightweight but powerful forensic platform (commercial).

**Viva Qs (tools)**

* Q: Which tool for memory forensics? → Volatility.
* Q: Which tool for carving deleted photos? → PhotoRec.

---

# Deleted-data retrieval — what really happens (how it acts)

**What “delete” means (file systems):**

* Deleting usually **removes the file’s directory entry** and marks its data blocks as **free** in the file system metadata — the actual bytes remain on disk until overwritten.
* On **NTFS**: Master File Table (MFT) contains records; deletion removes reference but data clusters remain.
* There are also **unallocated space** (formerly used clusters) and **slack space** (unused bytes within a cluster) where fragments remain.

**Volatile vs persistent**

* **Volatile data** (RAM, active connections) is lost on power-off — requires **live forensics**.
* **Non-volatile** (HDD/SSD) data persists until overwritten; SSDs with TRIM may zero out blocks making recovery harder.

---

# How investigators recover deleted data — step-by-step (for viva)

1. **Seize device & preserve scene**

   * Document chain of custody, photograph device, avoid changing state.
2. **Make a forensic image** (bit-for-bit):

   * Use `dd`, `dc3dd`, or FTK Imager. Example: `dd if=/dev/sdb of=/evidence/disk1.img bs=4M conv=noerror,sync`
   * Always compute hashes (MD5/SHA256) for original and image.
3. **Work on the image, not original**

   * Mount read-only or use tools that operate on image files.
4. **Analyze file system metadata**

   * Use The Sleuth Kit (`mmls`, `fls`, `icat`) to list files and extract entries.
   * Examine MFT (NTFS) for deleted entries.
5. **File carving** (when metadata missing)

   * Search raw image for **file signatures** (magic bytes) and extract until footer or size limit. Tools: PhotoRec, foremost.
6. **Recover deleted partitions**

   * Use TestDisk to detect lost partition table entries and rebuild partition table if safe.
7. **Handle fragmentation**

   * If file fragmented, carving may produce partial files; use file system metadata (MFT) to reconstruct full files when possible.
8. **Memory analysis (if live)**

   * Dump RAM (DumpIt) then analyze with Volatility to extract processes, credentials, encryption keys.
9. **Validate & document**

   * Hash recovered files, log steps, prepare forensic report for court.

**Important notes**

* **SSD + TRIM**: TRIM may permanently erase blocks soon after deletion — recovery success may be low.
* **Overwritten data**: If overwritten, recovery is practically impossible with software (physical chip-level methods are complex and often impractical).
* **Encryption**: If files were encrypted before deletion, you need keys (from system/memory) to decrypt.

---

# Practical example commands & tools (memorize these lines)

* Create image: `sudo dd if=/dev/sdb of=/mnt/evidence/disk.img bs=4M conv=noerror,sync`
* Hash image: `sha256sum disk.img`
* List partitions: `mmls disk.img` (The Sleuth Kit)
* List files (including deleted): `fls -r -m / disk.img`
* Extract file by inode: `icat disk.img inode_number > file_recovered`
* Run PhotoRec: `photorec /log /d /recovery/output /cmd disk.img partition_number search`

---

# Common viva questions (deleted-data & forensics) with short answers

1. **Q:** Why image the disk?
   **A:** To preserve original evidence and enable repeatable analysis without altering the original.
2. **Q:** What is file carving?
   **A:** Recovering files by searching raw disk for known headers/footers when file metadata is missing.
3. **Q:** Can you always recover deleted files?
   **A:** No — if data was overwritten or SSD TRIM applied, recovery may be impossible.
4. **Q:** What is MFT?
   **A:** Master File Table on NTFS storing metadata (filenames, locations). Deleted file entries may still exist there.
5. **Q:** How to get encryption keys from a running system?
   **A:** Use live memory capture (DumpIt) and analyze RAM with Volatility to extract keys or credentials.
6. **Q:** How do you prove evidence integrity?
   **A:** Use cryptographic hashes (MD5/SHA256) and document chain of custody.

---

# Short summary you can memorize (one-liners)

* Wireshark = capture → filter → inspect → export; great for network forensics.
* Forensic workflow = seize → image → hash → analyze → report.
* Deleted files still exist until overwritten; recover with metadata parsing (MFT) or file carving (PhotoRec/TestDisk).
* SSDs & TRIM + overwritten sectors = low recovery chance.
* Always work on a copy and preserve chain of custody + hashes.

---





## 🧾 **What is Log Capturing?**

**Definition:**
Log capturing is the process of **collecting and recording system, network, or application events** to monitor activity, detect incidents, and support digital forensic investigations.

In simple terms —

> 📜 “It’s like keeping a diary of everything happening in a computer or network.”

---

## ⚙️ **Why Log Capturing is Important**

1. 🕵️‍♀️ **Forensic Evidence** — Helps trace what happened, when, and by whom.
2. 🔐 **Security Monitoring** — Detects suspicious logins, malware, or attacks.
3. ⚡ **Incident Response** — Allows quick action during breaches.
4. 🧩 **System Debugging** — Identifies software or hardware errors.
5. 📈 **Compliance** — Required for audits (e.g., ISO, PCI-DSS).

---

## 🧰 **Types of Logs Captured**

| **Type**                 | **Example**                        | **Purpose**                       |
| ------------------------ | ---------------------------------- | --------------------------------- |
| **System Logs**          | Boot logs, kernel messages         | OS activity & errors              |
| **Application Logs**     | Web server (Apache), Database logs | Application errors & usage        |
| **Security Logs**        | Login attempts, file access        | Detect unauthorized access        |
| **Network Logs**         | Firewall, router, IDS logs         | Monitor incoming/outgoing traffic |
| **Event Logs (Windows)** | Application, Security, System      | Centralized event tracking        |

---

## 🧱 **Common Tools for Log Capturing**

| **Tool**                 | **Platform**          | **Use**                               |
| ------------------------ | --------------------- | ------------------------------------- |
| **Syslog / Rsyslog**     | Linux/Unix            | Collects & forwards logs              |
| **Event Viewer**         | Windows               | View system/application events        |
| **Logstash (ELK Stack)** | Cross-platform        | Collect + parse + forward logs        |
| **Splunk**               | Enterprise            | Real-time log analysis                |
| **Wireshark**            | Network               | Capture network packets               |
| **SIEM Tools**           | ELK, QRadar, ArcSight | Correlate and analyze security events |

---

## 🧩 **Process of Log Capturing**

1. **Enable Logging** → Turn on logging for system, network, and applications.
2. **Collect Logs** → Gather data from different sources (firewalls, OS, servers).
3. **Normalize Logs** → Convert to common format (e.g., JSON).
4. **Store Securely** → Save in central log server (log retention policy).
5. **Analyze & Correlate** → Identify abnormal events (e.g., repeated login failures).
6. **Generate Alerts & Reports** → For admins and investigators.

---

## 📊 **Example:**

If a user tries multiple failed logins, logs might show:

```
[2025-11-06 12:34:01] FAILED LOGIN - User: admin - IP: 192.168.1.10
[2025-11-06 12:34:04] FAILED LOGIN - User: admin - IP: 192.168.1.10
[2025-11-06 12:34:08] SUCCESS LOGIN - User: admin - IP: 192.168.1.10
```

➡️ From these logs, you can correlate failed + success → possible **brute-force attack**.

---

## 🔐 **Best Practices**

* Timestamp logs (UTC).
* Store logs on a **separate, secure server**.
* Use **digital signatures or hashing** for log integrity.
* Set **log rotation** and **retention policies**.
* Implement **SIEM (Security Information and Event Management)** tools.

---

## 🎤 **Viva Questions**

**Q1:** What is log capturing in cybersecurity?
**A:** The process of collecting and analyzing system and network logs to detect, investigate, and prevent security incidents.

**Q2:** Why are logs important in digital forensics?
**A:** They provide evidence of user actions, system changes, and attack traces.

**Q3:** Name two log capturing tools.
**A:** Rsyslog, Splunk (or Event Viewer in Windows).

**Q4:** What is SIEM?
**A:** Security Information and Event Management — a system that collects, correlates, and analyzes logs in real time.

**Q5:** What are the common sources of logs?
**A:** Operating systems, firewalls, IDS/IPS, web servers, and applications.

---




## 🧩 **1️⃣ IT Act 2000 / IT (Amendment) Act 2008–2009**

### 📘 **Full Form:**

Information Technology Act, 2000 (amended in 2008, effective in 2009)

### 💡 **Purpose:**

The **IT Act** gives legal recognition to electronic transactions, digital signatures, and defines **cyber crimes and penalties** in India.

### ⚖️ **Main Objectives:**

1. Legal recognition for **electronic documents & signatures**
2. Prevent and punish **cyber crimes**
3. Establish **CERT-In** for cybersecurity incidents
4. Enable **e-governance** (digital contracts, online records)
5. Define laws for **data protection and privacy**

### 🔐 **Important Sections:**

| **Section** | **Meaning**                                               |
| ----------- | --------------------------------------------------------- |
| 43          | Unauthorized access, data theft – compensation to victim  |
| 65          | Tampering with computer source code                       |
| 66          | Hacking / data alteration – imprisonment up to 3 years    |
| 66C         | Identity theft                                            |
| 66D         | Cheating by personation (e.g., phishing)                  |
| 67          | Publishing obscene material online                        |
| 69          | Government power to intercept/decrypt data (for security) |

### 📅 **Amendment 2008 (in effect 2009):**

* Added sections for **cyber terrorism (66F)**, **child pornography**, **data privacy**, and **digital signatures**.
* Introduced the term **“Electronic Signature”**.
* Strengthened law for **cybercrime investigation**.

---

### 🎤 **Viva Questions**

**Q1:** When was the IT Act implemented?
➡️ Year 2000 (amended in 2008, effective from 2009).

**Q2:** What is Section 66?
➡️ It deals with hacking or altering computer data without permission.

**Q3:** What is cyber terrorism under IT Act?
➡️ Section 66F — acts intended to threaten the unity, integrity, or sovereignty of India through computer resources.

---

## 🔐 **2️⃣ Encryption vs Decryption**

| **Term**       | **Definition**                                                             | **Example / Function** |
| -------------- | -------------------------------------------------------------------------- | ---------------------- |
| **Encryption** | Converting **plaintext → ciphertext** (unreadable format) to protect data. | “HELLO” → “JGNNQ”      |
| **Decryption** | Converting **ciphertext → plaintext** using the proper key.                | “JGNNQ” → “HELLO”      |

### 🧠 **Types of Encryption:**

* **Symmetric Key** → Same key for encryption & decryption (e.g., AES)
* **Asymmetric Key** → Public key to encrypt, private key to decrypt (e.g., RSA)

### 💡 **Example:**

```
Encryption:  Data + Key → Ciphertext
Decryption:  Ciphertext + Key → Original Data
```

### 🎤 **Viva Qs**

**Q1:** Why use encryption?
➡️ To ensure confidentiality and security of data in transit or storage.

**Q2:** Which is more secure — MD5 or SHA-256?
➡️ SHA-256 (MD5 is outdated and collision-prone).

---

## 🧠 **3️⃣ Tokenization, Stemming, and Lemmatization**

These are **Text Preprocessing** steps in **Information Retrieval (IR)** or **NLP** to prepare text for analysis.

| **Process**       | **Definition**                                                        | **Example**                                |
| ----------------- | --------------------------------------------------------------------- | ------------------------------------------ |
| **Tokenization**  | Breaking text into smaller parts (tokens → words/sentences).          | “I love coding.” → [“I”, “love”, “coding”] |
| **Stemming**      | Reducing words to their **root form** by removing suffixes.           | “playing”, “played” → “play”               |
| **Lemmatization** | Converts word to its **dictionary (lemma)** form using grammar rules. | “better” → “good”, “running” → “run”       |

💡 **Difference:**

* Stemming is **rule-based (cuts words)** → faster, less accurate.
* Lemmatization is **meaning-based (uses dictionary)** → slower, more accurate.

### 🎤 **Viva Qs**

**Q1:** Why is stemming used in IR?
➡️ To reduce variations of a word and improve search results.

**Q2:** Which is more accurate — stemming or lemmatization?
➡️ Lemmatization (it uses context and grammar).

---

## 🔍 **4️⃣ Data Retrieval vs Information Retrieval**

| **Aspect**         | **Data Retrieval**                              | **Information Retrieval**                                                 |
| ------------------ | ----------------------------------------------- | ------------------------------------------------------------------------- |
| **Definition**     | Fetching **exact data** that matches a query.   | Finding **relevant information** from unstructured data (like text, web). |
| **Data Type**      | Structured (tables, databases).                 | Unstructured (documents, web pages, emails).                              |
| **Query Language** | SQL (Structured Query Language).                | Natural language / keyword queries.                                       |
| **Result Type**    | Exact answer.                                   | Ranked documents based on relevance.                                      |
| **Example**        | SQL query → `SELECT * FROM STUDENT WHERE ID=5;` | Google search → “Best colleges in Pune.”                                  |
| **Evaluation**     | Accuracy (exact match).                         | Relevance, precision, recall.                                             |

💡 **In short:**

> Data Retrieval = “Get exact facts.”
> Information Retrieval = “Find relevant knowledge.”

---

### 🎤 **Viva Qs**

**Q1:** What is the main goal of IR?
➡️ To find relevant documents from large, unstructured datasets.

**Q2:** Give an example of each.
➡️ DR: Fetch student record from DB; IR: Google search results.

**Q3:** Which uses ranking algorithms?
➡️ Information Retrieval (e.g., PageRank).

---

## 🧾 **Quick Revision Lines**

* **IT Act 2000:** Legal recognition of e-documents & cybercrime laws; amended 2008.
* **Encryption = Lock data; Decryption = Unlock data.**
* **Tokenization → Stemming → Lemmatization → Preprocess text.**
* **Data Retrieval = Structured DB (SQL); Information Retrieval = Unstructured search (IR).**

---




---

## 🌐 **Scenario:**

> “My organization’s website is working fine but very slow.”

---

## ⚠️ **Possible Cyber Attacks Behind This Scenario**

### **1️⃣ DoS (Denial of Service) Attack**

* **Meaning:** The attacker floods the server with excessive requests to slow it down or make it unavailable.
* **Effect:** Website becomes **slow or unresponsive**.
* **Signs:**

  * High network traffic
  * High CPU/memory usage
  * Logs show repeated requests from same IP
* **Example:** `ping -t yourwebsite.com` from thousands of bots.
* **Countermeasure:** Use firewalls, rate limiting, and traffic filtering (e.g., Cloudflare).

---

### **2️⃣ DDoS (Distributed Denial of Service) Attack**

* **Meaning:** A **distributed** version of DoS — attacker uses **botnets** (infected computers worldwide) to send massive traffic simultaneously.
* **Effect:** Website still works, but performance is extremely slow due to overload.
* **Example:** Mirai botnet attack on Dyn DNS (took down Twitter, Netflix).
* **Countermeasure:**

  * Use DDoS protection (Cloudflare, AWS Shield).
  * Block suspicious IP ranges.
  * Use load balancing and content delivery networks (CDNs).

---

### **3️⃣ SYN Flood Attack (Type of DoS)**

* **Meaning:** Attacker sends multiple TCP connection requests (SYN) but never completes the handshake.
* **Effect:** Server keeps resources allocated, causing slow performance.
* **Countermeasure:** SYN cookies, connection timeout limits.




---

## 🧠 **How to Identify the Attack**

1. **Check network traffic:**

   * If there’s sudden high inbound traffic → possible









# ALL THE BEST!