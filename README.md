# Web Crawler and Search Engine

A Java-based web crawler and search engine that crawls Wikipedia pages and provides a search interface using TF-IDF and cosine similarity for document ranking.

## Features

- **Web Crawling**: Crawls Wikipedia pages starting from seed URLs
- **Text Processing**: 
  - Stop word removal
  - Word stemming using Porter Stemming Algorithm
  - Text extraction from HTML content
- **Search Engine**:
  - Inverted index implementation
  - TF-IDF vector space model
  - Cosine similarity for document ranking
  - Interactive search interface

## Project Structure

The project is organized into several key components:

- `WebCrawler.java`: Implements the web crawling functionality using Jsoup
- `InvertedIndex.java`: Maintains the inverted index data structure
- `TFIDF_Calculator.java`: Computes TF-IDF vectors for documents
- `QueryProcessor.java`: Processes user queries and computes query vectors
- `SimilarityScorer.java`: Ranks documents using cosine similarity
- `DocumentData.java`: Represents crawled document data
- `Stemmer.java`: Implements the Porter Stemming Algorithm
- `StopWords.java`: Contains common English stop words

## Requirements

- Java 23 or higher
- Maven
- Internet connection (for crawling)

## Dependencies

- Jsoup 1.17.2 (for HTML parsing and web crawling)

## Building the Project

1. Clone the repository
2. Navigate to the project directory
3. Build using Maven:
   ```bash
   mvn clean install
   ```

## Running the Application

1. After building, run the main class:
   ```bash
   java -cp target/Web_Crawler-1.0-SNAPSHOT.jar org.os.Main
   ```

2. The application will:
   - Start crawling from seed Wikipedia URLs
   - Build the inverted index
   - Compute TF-IDF vectors
   - Present an interactive search interface

3. Enter your search queries at the prompt
4. Type 'exit' to quit the application

## Search Features

- The search engine uses TF-IDF weighting and cosine similarity
- Results are ranked by relevance score
- Stop words are automatically removed
- Words are stemmed to their root form
- Results include document titles and URLs

## Implementation Details

### Web Crawling
- Uses breadth-first search (BFS) to crawl pages
- Stays within Wikipedia domain
- Extracts main content from article pages
- Maintains a visited URL set to avoid duplicates

### Text Processing
- Removes HTML tags and extracts clean text
- Filters out stop words
- Stems words to their root form
- Handles basic text normalization

### Search Engine
- Builds an inverted index for efficient retrieval
- Computes TF-IDF weights for terms
- Uses cosine similarity for document ranking
- Supports multi-word queries

## Limitations

- Currently limited to Wikipedia pages
- Maximum of 10 documents crawled
- Basic stemming implementation
- No advanced query features (e.g., phrase search, boolean operators)

## Future Improvements

- Support for more websites
- Advanced query processing
- Improved stemming
- Phrase search capabilities
- Boolean search operators
- Result caching
- Web interface

## License

This project is open source and available under the MIT License.
