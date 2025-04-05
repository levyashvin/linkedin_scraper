# LinkedIn Post Scraper & Topic Clustering

This tool scrapes public LinkedIn posts from user profiles and clusters them into topics using **TF-IDF** and **Latent Semantic Analysis (LSA)**.

> **Disclaimer**: Scraping LinkedIn may violate their Terms of Service. Use this tool responsibly and only on your own data or with consent.

---

## Features

-  Automated LinkedIn login (via Selenium)
-  Scrapes recent public posts from LinkedIn profiles
-  Clusters posts into topics using NLP
-  Outputs dominant topics for each post

---

##  Requirements

Install the required libraries:

```bash
pip install selenium beautifulsoup4 pandas nltk scikit-learn
```

Make sure you also download [ChromeDriver](https://sites.google.com/chromium.org/driver/) and add it to your system `PATH`.

---

##  Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/yourusername/linkedin-scraper.git
cd linkedin-scraper
```

### 2. Set the ChromeDriver Path

In the script, find this line:

```python
os.environ["PATH"] += r"--"  # Replace this
```

Replace it with your actual path. Example:

```python
os.environ["PATH"] += r"C:\\Users\\YourName\\chromedriver"
```

### 3. Run the Script

Run via Jupyter Notebook or terminal:

```bash
python linkedin_scraper.py
```

You’ll be prompted to enter:

- LinkedIn email and password
- Number of profile links to scrape
- Number of posts per profile

---

## Example

```text
enter linkedin email id: johndoe@email.com
enter linkedin password: ********
enter the number of entries: 2
enter the link: https://www.linkedin.com/in/example1/
enter the link: https://www.linkedin.com/in/example2/
enter number of posts per account: 5
```

Sample Output:

```
Fetching data from account: example1
posts fetched: 5

topic 0: ['ai', 'future', 'tech', 'data', 'ml']
topic 1: ['career', 'growth', 'learning', 'skills', 'job']

post:1
topic 0: ['ai', 'future', 'tech', 'data', 'ml']
```

---

## FAQ

**Q: Can I run this without a GUI browser?**  
A: You can switch to headless mode by editing the Selenium driver setup.

**Q: Is this safe to use on multiple profiles?**  
A: LinkedIn may block repeated automated activity. Always limit usage and use responsibly.

---

## License

MIT License – do whatever you want, just don’t blame me.
