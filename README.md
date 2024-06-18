# ESG_ranking_system

Classifier for ESG on news.


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

---

### Title: ESGer — Top Advisor for Corporate Sustainable Development

### Introduction 背景

**ESG 分別是環境保護（E，Environmental）、社會責任（S，Social）以及公司治理（G，governance）的縮寫，是一種新型態評估企業的數據與指標，ESG 代表的是企業社會責任，許多企業或投資人會將 ESG 評分，視為評估一間企業是否永續經營重要的指標及投資決策。**

ESG 可如同一間公司的健檢報告，針對公司內外做評鑑，評估一間公司的整體表現，不僅要財務表現亮眼、照顧好員工與股東，更需要承擔更多社會責任，企業規模不僅需要做大，更要長久達到永續經營。

我們的專題是想要分析新聞文章段落對於特定公司在 ESG 三個面向上面的評分，以第三方的角度來分析公司在 ESG 三個面向上面的表現，並作為企業在未來決策時可以納入考量的支持系統。透過文章段落來建立分類模型來分析各個企業的社會責任的表現。

**ESG stands for Environmental, Social, and Governance, and it is an abbreviation for a new form of assessing companies based on data and indicators. ESG represents a company's social responsibility, and many businesses or investors use ESG ratings as a critical indicator for evaluating a company's sustainability and making investment decisions.**

ESG can be likened to a company's health check report, evaluating both internal and external aspects of a company's overall performance. It requires not only impressive financial performance and taking care of employees and shareholders but also a greater commitment to social responsibility. Companies need to not only grow in size but also strive for long-term sustainability.

Our project aims to analyze specific company's ESG ratings in the three dimensions - Environmental, Social, and Governance - based on news article segments. We approach this analysis from a third-party perspective, assessing a company's performance in these three dimensions and providing a support system for future decision-making in businesses. We will use article segments to build a classification model to analyze the social responsibility performance of various companies.

### Solution 問題與解決方法

探討有關某企業的新聞報導來分類他哪個面向的新聞比較多，並且分析正負面，進而可以建議該企業在缺少的方面進行優化，提供企業決策輔助系統。

To examine news reports about a specific company, classify which aspect of the company is covered more frequently, and analyze the positive and negative aspects. Subsequently, we can recommend areas for optimization where the company may be lacking, thereby providing a decision support system for the company.

### Methodology

### 資料搜集 Data Collection

爬蟲 Web Crawler

標註 Tag

### 模型實驗 Model - 結果先不要

1. 透過分析ＯＯ則新聞，約ＯＯ個段落
2. training set/validation set
3. 模型架構 - Model Structure - Pipeline
    1. R/IR（filter）
    2. teacherforcing E/S/G（classifier）
        1. 刪掉Ｒ中的ＩＲ
        2. 
        3. 不刪
    3. teacherforcing E1/E2/E3（classifier）
    4. teacherforcing 0/1（classifier）
    5. 輔助的 double check

### Results

### 對公司算分方式 Scoring Approach

1. 

### 應用介面呈現 Front-end Presentation

### Future Works

提高模型準確度，更精準地呈現各公司在 ESG 方面的作為，並訓練 NER 命名實體技術模型，精準於文章中提取各產業名稱，應用在系統上。除此之外，還要擴大產業範圍，使平台成為一個整合各產業的全方位系統，可以有更多元的應用。並且定期更新各公司的最新 ESG 相關資訊並更新評分。

To enhance model accuracy and provide a more precise representation of each company's ESG efforts, as well as to train an NER (Named Entity Recognition) model to accurately extract industry names from articles for application within the system. Additionally, we will expand the scope of industries, making the platform a comprehensive system that integrates various sectors for more diverse applications. Furthermore, we will regularly update the latest ESG-related information for each company and update their scores.
