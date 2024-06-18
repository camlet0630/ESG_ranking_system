# ESG_ranking_system

Classifier for ESG on news.

ESGer — Top Advisor for Corporate Sustainable Development
### Introduction

ESG, standing for Environmental, Social, and Governance, is a modern approach to assessing companies by scrutinizing relevant data. It serves as a vital metric within corporate and investment spheres, offering insights into a company's dedication to social responsibility and influencing sustainability evaluations and investment choices.

Conceptually, ESG can be likened to a comprehensive health check for a company, extending beyond financial indicators to include internal and external performance aspects. This approach emphasizes not only financial growth but also a steadfast commitment to social responsibility, urging companies to prioritize sustainable practices. Our project is dedicated to a detailed analysis of specific companies' ESG ratings, with a particular focus on the Environmental, Social, and Governance dimensions. Employing news article segments, we adopt a third-party perspective to scrutinize and classify companies based on their social responsibility performance. The ultimate aim is to furnish robust support for informed decision-making in the business domain.

### Solution

To understand a company's performance in terms of ESG criteria, a common approach is to hire professional ESG assessors who analyze data such as corporate financial reports. However, this method incurs high time and financial costs. Therefore, we propose a relatively low-cost corporate ESG scoring system.

We believe that news reports about a company can to some extent reflect its ESG performance. Therefore, we use news related to the company as analytical data, applying deep learning methods to assign labels for each aspect of ESG to the news. Finally, we determine the company's performance in each dimension and provide an overall score based on the frequency of these labels.

### Methodology

We implement the corporate ESG scoring through deep learning, the method can be divided into two main parts: data collection and model training.

**Data Collection**

First, we use web crawlers to gather news related to the company. Subsequently, we segment the obtained news into paragraphs and label them with tags for each aspect of ESG. This labeled data serves as the basis for training the subsequent model.

We collected a total of 2238 news articles, comprising 17426 paragraphs. ESG is classified into several subcategories, each subcategory is further divided into positive or negative evaluations.

**Model Training**

We employ supervised learning, specifically using a neural network, to train a model for classifying news text. Given that the data includes a substantial amount of news unrelated to ESG, we adopt a pipeline approach by splitting the model into two components: a filter and a classifier. The filter  categorizes data into relevant or irrelevant, and the classifier further classifies relevant data into various ESG subcategories.

**Model Architecture**

### System 

### Future Work

Our research has identified the potential of using deep learning models for ESG classification of news texts. Additionally, there are three directions to enhance the model's reliability and the system's scalability:

1. Integrate the pipeline system into an end-to-end system: The current deep learning model is structured as a pipeline. Subsequently, it can be integrated into an end-to-end framework to improve the model's reliability.
2. Data Quality: Utilize kappa to assess the consistency of data labeling, ensuring data quality.
3. Timeline: Differentiate news data over time to observe trends in the scoring variations across various aspects of the company.

*Apprndix*
Training Model Structure
![圖片1](https://github.com/camlet0630/ESG_ranking_system/assets/91883637/f9ae8a77-fe31-4455-9cbe-34b959b64095)

