# 📚 Exploring the World of Books  

## 🧠 Abstract  
This project explores the nuanced relationship between an author’s **prolificacy** (number of books written) and the **average ratings** of their works.  

Our findings reveal:  
- A high book count does not guarantee high ratings.  
- Some authors maintain consistent quality across many works.  
- Others show fluctuating ratings regardless of volume.  

The study underscores that **quality, not quantity, shapes literary impact**.  

Through **data analysis, visualizations, and web scraping**, we provide actionable insights for **readers, publishers, and authors** about trends in the literary world.  

---

## 📌 Introduction  
This is a **data-driven exploration** into the book ecosystem, combining structured datasets and scraped reviews to:  
- Analyze trends in book ratings  
- Compare author productivity with perceived quality  
- Visualize publisher dominance and rating distributions  
- Scrape Amazon for live book review data  

---

## 📦 Dataset Overview  
The project uses two primary datasets:  
- **BX-Books.csv** → Book details (title, author, year, publisher)  
- **BX-Book-Ratings.csv** → User ratings  

---

## 🔧 Modules Overview  

| Module | Purpose |
|--------|---------|
| `cleaning/books_cleaning.py` | Preprocessing and merging book & rating data |
| `summary/books_summary.py` | Dataset summary, shape, nulls, and statistics |
| `eda/books_eda.py` | Visualizations: top authors, publishers, rating distributions |
| `inference/books_inference.py` | Correlation analysis between authorship and ratings |
| `scraping/books_scraper.py` | Web scraping Amazon for book review metadata |
| `surprise/book_surprise.py` | Generating recommendation-based insights |

---

## 📊 Features  

- 📈 **Top Publishers/Authors** → Bar plots for most prolific contributors  
- 🧩 **Ratings Distribution** → Histograms of user ratings  
- ☁️ **Word Clouds** → Frequent titles at a glance  
- 🔬 **Author–Rating Correlation** → Quality vs. quantity analysis  
- 🌐 **Amazon Scraper** → Pull book titles, ratings, and review counts live  
- 📈 **Publication Year Analysis** → Study reader preferences over time  

---

## 🔎 Web Scraping Example  

```python
from src.scraping.books_scraper import BooksScraper  

book_list = ["The Big Book of American Trivia", "Hamlet (Wordsworth Classics)"]  
scraper = BooksScraper("https://www.amazon.com")  
book_data = scraper.scrape_books(book_list)  
