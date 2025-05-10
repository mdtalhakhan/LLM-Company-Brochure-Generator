# Website Brochure Generator using GPT-4o Mini

Using LLM to automatically generate a neat, presentable brochure for your website using GPT-4o Mini.

## Project Description

This project is designed to **visit any given website**, intelligently **extract relevant content**, and **generate a Markdown brochure** summarizing your business.

- Scrapes your **homepage** and finds **only meaningful internal links** (like "Services", "About Us", "Contact", etc.)
- Ignores irrelevant links such as:
  - Terms of Service
  - Privacy Policy
  - Email links (mailto)
  - External social links (e.g., LinkedIn, Twitter)
- Extracts full text content from these relevant pages.
- Generates a **clean, concise, and readable brochure** in Markdown using a second LLM model.

## Technologies Used

- **Python**
- **BeautifulSoup** – For web scraping
- **OpenAI GPT-4o Mini** – For:
  - Filtering relevant website links
  - Generating the final brochure content in Markdown

---

## 🧱 How It Works

1. **Scrape**: The homepage is scraped using `BeautifulSoup`.
2. **Filter Links**: 
   - GPT-4o Mini filters out only *relevant links* such as:
     - `/services`, `/about`, `/contact`, `/portfolio`, etc.
     - Ignores: `/privacy`, `/terms`, `mailto:`, `#`, external links, etc.
3. **Content Collection**: Scrapes data from all valid internal links.
4. **Brochure Generation**: Another GPT-4o Mini prompt processes all this data into a well-structured **Markdown brochure**.

