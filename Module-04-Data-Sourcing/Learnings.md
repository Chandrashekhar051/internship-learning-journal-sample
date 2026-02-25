## Learnings – Data Sourcing

After thoroughly completing the Data Sourcing module, I gained a deeper technical understanding of how data is acquired, extracted, processed, and automated in real-world data science workflows. This module expanded my perspective beyond static datasets and introduced practical strategies for collecting structured, semi-structured, and unstructured data from multiple sources.

### Understanding Data Collection Architectures

I learned that data sourcing strategies depend heavily on the format, accessibility, and structure of the data. Structured data is typically accessible via REST APIs or downloadable files (CSV, JSON), whereas semi-structured and unstructured data require scraping or parsing techniques.

I also understood the importance of identifying:
- The transport mechanism (HTTP/HTTPS requests)
- The response format (JSON, XML, HTML)
- Authentication mechanisms (API keys, tokens)
- Rate limiting and usage policies

Selecting the appropriate extraction approach depends on these technical constraints.

### Spreadsheet-Based Scraping

Through Excel and Google Sheets, I explored how functions such as IMPORTHTML, IMPORTXML, and web queries can retrieve live web data. I understood that spreadsheets can act as lightweight ETL tools, allowing basic extraction and transformation without writing full scripts.

This reinforced the idea that not all data sourcing requires backend programming; simple tools can sometimes solve practical problems efficiently.

### CLI and API Integration

I developed a clearer understanding of using command-line tools (like curl and wget) to make HTTP requests and retrieve raw responses directly from servers. This helped me understand:

- HTTP methods (GET, POST)
- Status codes (200, 404, 500)
- Headers and query parameters
- JSON parsing

Working with APIs such as weather services, Nominatim (geolocation), and Wikipedia APIs strengthened my understanding of RESTful API architecture. I learned how to structure requests, handle JSON responses in Python, and extract nested data fields programmatically.

This improved my knowledge of request-response cycles and data serialization formats.

### Web Crawling and Automation

I learned the difference between static and dynamic websites. Static pages can be scraped using HTML parsers like BeautifulSoup, whereas dynamic pages require browser automation tools such as Playwright.

Using automation frameworks helped me understand:
- Headless browser execution
- DOM rendering after JavaScript execution
- Simulating user interactions (clicks, scrolls, form submissions)
- Waiting for network responses and dynamic elements

This gave me practical exposure to handling modern single-page applications (SPAs).

### JavaScript-Based Scraping and DOM Analysis

While working with JavaScript-based scraping (e.g., IMDb), I understood how to inspect web pages using developer tools, analyze the DOM tree, and target elements using CSS selectors and XPath expressions.

This improved my ability to:
- Identify structured patterns in HTML
- Extract attributes and text content
- Handle pagination and multiple records

### Document Processing and Data Extraction

I learned techniques to extract tabular data from PDFs using tools like Tabula. This demonstrated how structured data can exist within unstructured file formats.

Additionally, converting PDFs and HTML into Markdown showed me how format transformation can simplify downstream processing. I understood that preprocessing is often required before performing analysis.

### AI-Assisted and LLM-Based Scraping

The introduction to AI-assisted scraping highlighted how large language models can interpret semi-structured content and extract meaningful information without strict rule-based selectors.

I learned that LLM-based extraction can:
- Summarize large web pages
- Extract entities from noisy text
- Interpret visual or video content through screen analysis

This represents a shift from deterministic scraping to intelligent extraction systems.

### Advanced Scraping Concepts

I gained awareness of practical challenges such as:
- Rate limiting and throttling
- IP blocking
- Session handling and cookies
- Login-protected content
- Ethical scraping practices and robots.txt compliance

Understanding these constraints helped me appreciate the importance of responsible data collection and adherence to website policies.

### Automation with GitHub Actions

I learned how to automate scraping workflows using GitHub Actions. By defining workflow YAML configurations, I can schedule scripts to run at specific intervals.

This introduced me to:
- CI/CD pipelines for data workflows
- Cron-based scheduling
- Automated dataset updates
- Cloud-based execution environments

Automation ensures data freshness without manual intervention.

### Making Open Data Analysis-Ready

Finally, I understood that raw data is rarely usable in its original form. The process of cleaning, validating, normalizing, and transforming data is essential before analysis.

This includes:
- Removing duplicates
- Handling missing values
- Standardizing formats
- Structuring data into tabular or database-ready schemas

Data sourcing is therefore the first stage of a broader data engineering pipeline.

## Overall Reflection

This module significantly strengthened my technical foundation in data acquisition. I now understand how to choose appropriate sourcing strategies, interact with APIs, scrape both static and dynamic websites, process document-based data, and automate recurring workflows.

More importantly, I gained clarity on the ethical and architectural considerations involved in large-scale data collection. This knowledge prepares me to design efficient, scalable, and responsible data sourcing pipelines in real-world projects.
