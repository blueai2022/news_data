### 📰 The Geolocated German News Dataset

This dataset is described in a Data Descriptor published in *Scientific Data* and aligns closely with your requirement for regionally coded news.

- **Data Source and Volume**: The data is collected from the **CommonCrawl News dataset**, covering a period from August 2016 to December 2023. The final compiled dataset contains about **50 million German news articles**, with approximately **70% (around 35 million) including geographic locations**.
- **Geolocation Method**: The geographic coding is achieved through a **Named-Entity Recognition (NER) model** that identifies location entities within the text and links them to specific geographic coordinates. This allows you to analyze news based on the event location discussed in the articles.
- **Sentiment Analysis Potential**: While the dataset itself provides the raw text and geographic metadata, it does not come with pre-computed sentiment scores. However, the articles are processed into **text embeddings using SBERT** (Sentence-BERT). These vector representations capture the semantic meaning of the text and can be directly used to train custom classifiers, such as a **sentiment analysis model** tailored to your research question.
- **Access Information**: This appears to be a published scientific dataset rather than a GitHub repository. You can likely access it through the **Nature Scientific Data** article, which should provide a link or instructions for downloading the data.

### 💡 How to Leverage This Dataset for Your Thesis

To correlate news sentiment with populist voting, you will need to integrate this news dataset with external data sources. The following table outlines a potential research strategy:

| Step | Task | Description | Data Sources / Methods |
| :--- | :--- | :--- | :--- |
| **1** | **Perform Sentiment Analysis** | Add a sentiment dimension to the news dataset. | Use the SBERT text embeddings to train a custom sentiment classifier, or apply an existing German sentiment tool. |
| **2** | **Aggregate Data by Region** | Prepare both news and election data for correlation. | Aggregate news sentiment by German states (*Bundesländer*) or voting districts. Merge with official election results. |
| **3** | **Acquire Election Data** | Obtain data on populist voting. | Source from state statistical offices, the Federal Returning Officer, or political datasets like "PolData". |
| **4** | **Conduct Statistical Analysis** | Test the correlation between your variables. | Use statistical methods (e.g., regression analysis) to examine the relationship between regional news sentiment and populist vote share. |

### 🔍 Other Relevant Resources

While not a perfect fit, the following GitHub repositories involve German text analysis and could provide useful code or methodological insights for your work. You might adapt their approaches for sentiment analysis or topic modeling.

| Repository Name | Relevance to Your Project | Direct Fit for Your Needs |
| :--- | :--- | :--- |
| **GC News** | A master's thesis analyzing populism in German news media during COVID-19; implements text classification. | **Low-Medium**: Offers methodological inspiration for analyzing populism in news text, but does not provide a ready-to-use regional dataset. |
| **NeMig** | A bilingual (German/English) news collection on migration, annotated with sentiment and political orientation. | **Low-Medium**: Focused on a single topic (migration); useful for methodology but limited in thematic scope for your thesis. |
| **PolData** | A meta-list of political datasets; may help you find election results and data on populist party performance. | **Low**: An index of links, not a direct data source; requires you to search for and vet the specific datasets you need. |

### ✍️ Suggested Next Steps

1.  **Access the Core Dataset**: Obtain the **geolocated German news dataset** by following the instructions in the *Scientific Data* article. This will be the foundation of your analysis.
2.  **Source Election Data**: Use the "PolData" repository or official sources to find data on election results for populist parties (like AfD) at the regional level in Germany.
3.  **Develop Your Sentiment Model**: Decide on your method for sentiment analysis. You can train a model using the provided text embeddings or benchmark existing German sentiment tools for suitability.
4.  **Seek Out Code**: Look for GitHub repositories that provide code for sentiment analysis on German text. You can use the methodologies from "GC News" or "NeMig" as a starting point and adapt them to work with your newly acquired news dataset.
