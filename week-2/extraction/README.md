# Data Extraction Strategy

## Objective

The objective of this section is to define suitable methods for
collecting data from publicly available sources for Machine Learning
applications in the Apparel & Textiles industry.

The preferred extraction method depends on the source structure,
availability, reliability, scalability and legal usage conditions.

---

# 1. Official APIs

APIs are the preferred method when a government, organization or
platform provides structured programmatic access.

## Examples

- Government Open Data APIs
- Statistical APIs
- International trade APIs

## Advantages

- Automated data collection
- Structured data
- Reproducible
- Scalable
- Easier to schedule regular updates

## Limitations

- API keys may be required
- Rate limits
- Authentication requirements
- API version changes
- Changes in response structure

## Recommended Practice

Record:

- API endpoint
- Query parameters
- Access date
- Dataset version
- Response format
- Update frequency

---

# 2. CSV and JSON Downloads

CSV and JSON files are useful when an official organization provides
direct downloadable datasets.

## Advantages

- Easy to download
- Easy to process using Python
- Machine-readable
- Easy to archive
- Reproducible

## Limitations

- Dataset may not update automatically
- Manual download may be required
- File structure may change
- Large files may require additional processing

## Recommended Tools

- Python
- pandas
- JSON libraries
- Excel for basic inspection

---

# 3. Web Scraping

Web scraping can be considered when required information is publicly
available on websites but no suitable API or download is provided.

## Possible Applications

- Public product information
- Public fashion trend information
- Public market information
- Public product attributes

## Advantages

- Can collect information not available through an API
- Can automate repetitive collection
- Can capture structured public information

## Limitations

- Website structure can change
- Rate limits
- Robots restrictions
- Terms of service
- Duplicate information
- Anti-bot mechanisms
- Data quality problems

## Recommended Practice

Web scraping should only be performed when it is permitted by the
website's applicable terms and policies.

Use:

- Rate limiting
- Clear user-agent identification where appropriate
- Request logging
- Error handling
- Duplicate detection

---

# 4. PDF and Report Extraction

Government departments and organizations often publish industry
reports in PDF format.

These reports may contain:

- Textile industry statistics
- Export statistics
- Market information
- Production information
- Policy information
- Industry trends

## Advantages

- Contains official information
- Useful for industry research
- Can provide historical information

## Limitations

- Tables may be difficult to extract
- Formatting problems
- OCR errors
- Merged cells
- Different units
- Reporting delays

## Recommended Practice

Extracted values should always be compared with the original PDF.

Important totals should be manually verified.

---

# 5. Survey-Based Data Collection

Surveys can be used to collect targeted information that may not be
available from public datasets.

## Possible Survey Variables

- Customer preferences
- Clothing purchase frequency
- Preferred brands
- Preferred price range
- Size preferences
- Online shopping behavior
- Return behavior
- Fashion preferences

## Advantages

- Targeted information
- Flexible questionnaire
- Can collect domain-specific variables

## Limitations

- Sampling bias
- Response bias
- Small sample size
- Time required
- Participants may provide inaccurate responses

## Recommended Practice

A survey should include:

- Clear objective
- Appropriate sampling strategy
- Consent statement
- Anonymous responses where possible
- Clearly defined questions

---

# 6. Public Trend Data

Trend data can provide additional signals about consumer interest.

## Example

Google Trends can be used to analyze search interest related to:

- Dresses
- Jeans
- T-shirts
- Sneakers
- Sustainable fashion
- Seasonal fashion

## Advantages

- Timely
- Useful for trend analysis
- Geographic information may be available
- Historical search-interest information

## Limitations

Search interest is not the same as actual sales.

Other limitations include:

- Sampling
- Normalization
- Search-intent differences
- Geographic limitations

Therefore, trend data should be treated as a supplementary feature.

---

# 7. Open Machine Learning Datasets

Open datasets can be used for Machine Learning experiments.

## Examples

### Fashion-MNIST

Potential application:

- Image classification
- Computer Vision
- Apparel category recognition

### Fashion Product Datasets

Potential applications:

- Product classification
- Product attribute analysis
- Recommendation research

## Advantages

- Easy to access
- Useful for model experimentation
- Suitable for academic projects

## Limitations

- May be historical
- May not represent current market conditions
- Dataset size may be limited
- Dataset licensing must be checked

---

# 8. Recommended Technology Stack

## Programming

- Python

## Data Collection

- requests
- APIs
- pandas
- JSON
- BeautifulSoup
- Selenium where appropriate

## Data Processing

- pandas
- NumPy

## Database

- PostgreSQL
- MySQL
- SQLite

## Version Control

- Git
- GitHub

## Data Quality

- Pandas validation
- Pandera
- Great Expectations

---

# 9. Extraction Method Selection

The following priority should be used:

```text
Official API
      ↓
CSV / JSON Download
      ↓
Official Structured Dataset
      ↓
PDF Extraction
      ↓
Permitted Web Scraping
      ↓
Survey
