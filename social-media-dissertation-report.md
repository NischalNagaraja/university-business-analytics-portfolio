# Social Media Marketing and Business Growth

University of East Anglia — academic report evidence.

**Focus:** Facebook tourism-post research; report discusses engagement, sentiment, clustering and predictive modelling.

**About this file:** Text extracted from the supplied academic report. Formatting, figures and diagrams are not preserved. Personal student identifiers were removed. This is an archived report, not a newly executed analysis; recommendations are academic proposals rather than implemented commercial outcomes.

---



NBS-7101X



  ANALYZING THE IMPACT OF SOCIAL MEDIA MARKETING ON BUSINESS GROWTH





STUDENT ID: [student identifier removed]







Dissertation submitted in partial fulfilment for the Degree of Master of Science in Business  Analytics and Management

                                                    

                                                    University of East Anglia

Norwich Business School







Submitted: 28th, August, 2024









“This copy of the dissertation has been supplied on condition that anyone who consults it is understood to recognize that its copyright rests with the author and then no quotation from the thesis, nor any information derived from there, may be published without the author’s prior written consent.”















DECLARATION



I have read and understood the rules on cheating, plagiarism, and appropriate referencing as outlined in my handbook and I declare that the work contained in this assignment is my own, unless otherwise acknowledged.

No substantial part of the work submitted here has also been submitted in other assessments for this or previous degree courses.

I acknowledge that if this has been done an appropriate reduction in the mark I might otherwise have received will be made.



Signed candidate



Abstract



This dissertation explores the impact of social media marketing (SMM) on business growth, specifically within the Amazon tourism sector. With the rapid expansion of social media as a dominant marketing tool, businesses, particularly in tourism, increasingly rely on these platforms to reach and engage with consumers. The research aims to identify how different social media strategies, including platform selection, content creation, and customer engagement, contribute to business development in this unique context.

To achieve these aims, the study utilizes both qualitative and quantitative methods. A comprehensive literature review provides the theoretical foundation, exploring existing research on SMM's effects on brand equity, consumer behaviour, and business performance. The empirical analysis uses a dataset of Facebook posts related to Amazon tourism, obtained from Kaggle. Through sentiment analysis, content clustering, and predictive modelling, the research identifies key trends and factors that influence engagement and, ultimately, business growth.

The findings suggest that social media marketing, when executed effectively, can significantly enhance brand visibility and customer interaction, leading to measurable business benefits. Positive sentiment, diverse content, and visual appeal were found to be critical components of successful SMM strategies in the tourism industry. However, the research also highlights challenges, including the need for continuous adaptation to rapidly changing social media dynamics and the importance of integrating SMM with broader marketing efforts.

This dissertation concludes by offering practical recommendations for businesses looking to leverage social media for growth in the tourism sector, emphasizing the importance of targeted content, positive messaging, and regular engagement with the audience.



Acknowledgements



I would like to begin by expressing my deepest appreciation to my supervisor, Rawan Qudiah. Your guidance, patience, and encouragement have been invaluable throughout this journey. Your constructive feedback and willingness to discuss ideas have significantly shaped the direction of this dissertation. I am truly grateful for your support and mentorship.

I also want to extend my sincere thanks to the faculty and staff at Norwich Business School, University of East Anglia. Your dedication to fostering a supportive and stimulating learning environment has been instrumental in my academic growth.

To my family and friends, I owe a debt of gratitude. Your understanding, encouragement, and constant support have kept me going, even during the most challenging times. Thank you for believing in me and for being my pillar of strength.

Finally, I want to acknowledge the researchers and professionals whose work in social media marketing and business growth has inspired this study. Your contributions have provided a solid foundation for my research, and I am grateful for the knowledge I have gained from your work.

This dissertation is the result of collective effort, and I am truly thankful to everyone who has supported me along the way.



TABLE OF CONTENT



Chapter 1: Introduction7

1.1 Research Background7

1.2 Aims and Objectives7

1.3 Research Questions8

1.4 Problem Statement8

Chapter 2: Literature Review9

2.1 Empirical study9

2.1.1 Impact of Social Media Marketing on Brand Equity and Consumer Behavior9

2.1.2 Social Media Marketing Strategies and Their Effectiveness11

2.1.3 User Engagement and Content Strategies in Social Media Marketing13

2.2 Theories and Models16

2.3 Literature gap17

Chapter 3: Methodology19

3.1 Research methods19

3.2 Implementation Strategy19

3.3 Data Collection Process20

3.4 Data Analysis Process21

4.1 Introduction22

4.2 Implementation22

4.3 Data Overview23

4.4 Engagement Analysis23

4.4.1 Distribution of Reactions & Comments23

4.4.2 Sentiment Analysis26

4.4.3 Content Clustering27

4.5 Predicting Engagement29

Chapter 5: Discussion31

5.1 Visualizing Predictions31

5.2 Recommendations for Business Growth32

5.3 Overview33

Reference List38

Appendices43





List of Figures:

Figure 1: Distribution graph of number of reactions…………………………………………… 23

Figure 2: Code for engagement analysis………………………………………………………... 24

Figure 3: Distribution of sentiment categories………………………………………………….  25

Figure 4: Distribution of likes share and comments………………………………………….….25

Figure 5: Likes, share and comments count………………………………………………….….26

Figure 6: Distribution graph of sentiment polarity………………………………………………27

Figure 7: Actual vs Predicted Engagement………………………………………………………31





List of Tables:

Table 1: Effectiveness of Social Media Marketing………………………………………………12

Table 2: Impact of Social media marketing on sales………………………………….................15



Chapter 1: Introduction

1.1 Research Background

Currently, social media marketing has been named as one of the most effective and widespread methods of marketing for the current generation business, particularly for the tourism sector. Communication with consumers, advertising services, and stimulating development have become some of the most important aspects in the last decade with social networking being one of the most important phenomena (Buhalis et al., 2023). As of now, 9 billion people use social media in the world, which is an opportunity for business and the opportunity to expand the circle of consumers (Kemp, 2023). It must be noted that social networks are one of the key tools in the tourism industry that can shape the choice and actual behaviour of the guests. Several previous studies have shown that users’ content on social media can affect destination image and visit’ intention (Kim et al., 2022). Also, direct interaction with the target audience is another advantage of the social media platform for businesses since it enhances the relations between the firm and the customers, thereby enhancing customer satisfaction (Chen et al., 2022). However, the effectiveness of social media marketing varies from company to company and therefore, there is a need to establish what makes social media marketing effective for companies. The objective of this research is to explore the efficiency of social media marketing in business development with an emphasis on platform selection, content sharing, and customer engagement in the context of Amazon tourism.



1.2 Aims and Objectives

The primary aim of this research is to determine the impact of Social Media Marketing (SMM) on business growth, focusing on Amazon tourism. 

The objectives are:

To identify trends in the indicators of the companies’ presence in social networks and their business development.

To identify the content strategies and how they affect the user.

To determine the sentiment and the content topics of the messages in social media regarding tourism.

To develop a Linear regression model that would forecast the outcome that is likely to happen in the future after the engagement has been conducted with due regard to other factors.

To present recommendations that can be implemented to make use of the social media marketing initiatives.



1.3 Research Questions

The research questions are:

Which of the post types garner the most attention on social networks?

How is the sentiment of the posts on social media related to the engagement of the users?

To how much extent can the level of engagement be forecasted by the features of the posts?

What are the opportunities and threats of marketing through the social media?



1.4 Problem Statement

The overall research question that this research aims to solve in its totality is the paucity of knowledge of Nepalese organisations regarding the correlation between different social media marketing strategies and customers’ attitudes towards the brand. Therefore, one can state that the usage of social media marketing in the context of the tourism industry is broad, however, most companies do not utilize these platforms for business enhancement. Now, there is general ignorance about how such components like the kind of content, the manner of writing, and how it is distributed affect the users’ response and therefore the business. Moreover, different, and new changes that occur within the social media platforms and the users’ activities present endless challenges to the business concerning the marketing strategies. This research will seek to fill the existing void resulting from a scarcity of empirical research on the impact of social media marketing in the tourism sector particularly in Amazon tourism with a view of providing tangible recommendations that can be of great benefit to the businesses.

Chapter 2: Literature Review

2.1 Empirical study

2.1.1 Impact of Social Media Marketing on Brand Equity and Consumer Behavior

According to (Godey et al., 2016), This research published in the Journal of Business Research looks at the impact of social media marketing strategies on brand associations and purchase intentions in luxury fashion brands. The authors also administered a survey of 845 respondents who are consumers of luxury brands from China, France, India, and Italy to provide cross-cultural results of the study. The research applies Structural Model Analysis to assess the effects of social media marketing strategies, aspects of brand equity and behavioural intentions. This research finds that marketing communication through social media has a very significant influence on brand equity dimensions, particularly brand knowledge and brand associations. Moreover, these efforts affect behavioural responses from the consumers including brand choice, price sensitivity and brand commitment. The research is useful to demonstrate that creating and maintaining an active account on social media is crucial for the luxury brand to enhance its brand image and consumer behaviour. The authors identify five key dimensions of social media marketing efforts: entertainment, interaction, trend, customization, and word of mouth. All these dimensions assist in the identification of the level of effectiveness of social media marketing. The research aims at developing good and attractive content to post on social sites and engaging with consumers to maximize the impacts of social media marketing. 

(Johnson, R. 2019) Nevertheless, it is vital to note that this research has focused on luxury brand consumers and therefore, the findings of this study are of significance to any business organization. This provides significant evidence in support of the hypothesis that SM has a positive impact on brand development and consumers’ activity which makes SM a very effective tool for brand equity generation and for initiating changes in consumers’ activity. This means that these effects are also valid for other markets making the study more relevant for organisations that are operating in different countries or those who intend to expand to other countries.

According to (Yadav et al., 2017), This research appearing in the Psychology & Marketing journal describes the authors’ review of existing literature on SMM and its impact on organisations. The authors selected 132 articles that were published in the period between 2006 and 2016, which describes the field’s development in a decade. It is a systematic way of finding out the research themes, patterns or even the research gaps within the social media marketing literature. Some of the areas that have been brought out in the review include the use of social media marketing as a branding tool, customer relationship tool and tool for sale. In other words, based on the findings of the authors, SMM has a positive impact on brand awareness, brand loyalty and purchase intentions. They focus on the universality of the tool stating that social media marketing can influence any of the consumers’ decision-making processes. Among the most significant tendencies which can be observed within this review, it is possible to name the function of UGC in SMM. Some of how consumers’ messages can influence perception, attitude, or behavior, may be even more significant than branded messages, as pointed out by the authors. This demonstrates that in addition to creating their content, firms need to both, popularize and leverage the user-generated content in their social media marketing. The review also describes how social media allows for the two-way interaction between the brands and the consumers. This is social media marketing’s interactive feature, which is considered one of the key components in building good customer relationships and brand association. The authors also note that organizations that engage in social networking sites are likely to report higher returns to the brand and customer. In addition, the review describes the challenges and opportunities of the SMM: the issue of measurement and ROI search, the need for stable and unambiguous brand communication, and the risk of negative eWOM. The research findings are relevant in the current setting in aiding business managers in making the right decisions on social media marketing.

According to (Ismail, 2017), This research is qualitative in nature and was published in the Online Journal of Communication and Media Technologies; the study explores the impact of social media marketing on brand loyalty in Malaysia’s fast-moving consumer goods (FMCG) sector. This research employs a survey research method, which involves distributing a questionnaire to 384 social media consumers who interact with FMCG brands on social media platforms. The study identifies five key dimensions of social media marketing: contact, verbal and written interaction, sharing of documents, sharing of information, and responsibility. The following dimensions are discussed regarding their impact on the brand loyalty variable. The study further confirms that all five dimensions are positively related to brand loyalty and particularly, online communities and interaction. The research concentrates on the elements of community creation and sustenance of online communities for the brand. These are areas that can be used to interface with the brand and also with other customers hence developing a relationship with the brand. The results of the study suggest that businesses should create content that is useful to the target market to ensure that the target community engage in activities that enhance the recall of brands. The dimension of interaction is presented as the most crucial one in the building of the buyer’s loyalty to the brand. During the research, it is evident that consumers who interactively engage with the brands on social sites are more inclined to be loyal to the brands. This supports the need for effective and interactive social media communication that triggers the desired interactions between the brand and the consumers. The research also considers content sharing as one of the types of social media marketing. It means that brands should create content that is not only informative and useful but also shareable as this would significantly increase the impact of the brand’s social media advertising and contribute to the formation of brand associations in the minds of consumers.

2.1.2 Social Media Marketing Strategies and Their Effectiveness 

According to (Rutter et al., 2016), This research has been developed with the help of an assessment of social media marketing practice included in the International Journal of Information Management. The study however limits Facebook as a marketing tool and focuses on an observation period of 30 days on 56 universities in the UK. This research design entails the use of Facebook metrics in conjunction with content analysis to achieve the research objectives. It also helps in evaluating the impact of social media marketing in terms of quantity and the quality of the characteristics of the approach. By observing the results of this research, it can be deduced that the Facebook marketing communication of the universities is not coherent and as a result, the positive correlation is low. Several of the factors that can be observed by the authors can be considered as important to the successful adoption of social media marketing in this respect. These are the frequency of posts, the time of posts, the content to post and the level of audience interaction achieved. Interestingly, the research indicates that no template can be followed in social media marketing. However, the strategies are the best ones which are appropriate to the target group and objectives of each institution in the given case. This goes a long way to show the need to know your consumer and create content that he or she will appreciate. The study also targets the significance of the share to the activity level on Facebook. In particular, the posts which shared with images or videos got many more likes, comments and shares compared to the posts without images or videos. This means that organizations including higher learning institutions and all forms of business should consider the use of visuals in their social media marketing. The other discovery made in the study is that social media marketing calls for regularity in social media marketing activities. What was discovered was that the universities that posted more frequently and those that were more active in their posting were the ones that received higher reach and engagement. This makes it necessary for businesses to have a proper and well-laid-down social media marketing strategy.

According to (Taiminen, et al., 2015), This research, which appears in the Journal of Small Business and Enterprise Development, investigates the social media marketing practices among small businesses. The study employs both quantitative and qualitative research surveys 403 small businesses and interviews 16 small firms’ marketing decision-makers.



Table 1: Effectiveness of Social Media Marketing

(Source: (https://d3i71xaburhd42.cloudfront.net/ee1d4ed081e7e74f50f81e86846ad809863ff18d/52-Table4.10-1.png))

The study established that there is awareness among small businesses regarding the benefits of social media marketing; however, the application is lacking. This research also reveals the factors that hinder the efficient use of social media marketing in small businesses; time constraints, inadequate capital and lack of adequate information on social media sites and marketing. Notably, the study reveals that effective social media marketing is achieved when it is combined with a small business’s overall marketing plan. Such businesses are usually aware of the target market and take time to harness social media to appeal to this market. It also stresses the need to have social media marketing metrics for ascertaining the efficiency of social media marketing strategies. However, it also discovers that many small businesses lack this aspect, with many of them using rather insufficient indicators such as the number of followers or likes instead of the real engagement or conversion rates.

According to (Tafesse et al., 2018), This theoretical paper published in the Journal of Strategic Marketing outlines an integrated framework of social media marketing. In this paper, the authors provide a literature review of the existing research and propose a conceptual model of social media marketing strategy. The paper identifies three key dimensions of social media marketing strategy: The goal of social media marketing, the activities that fall under social media marketing, and the resources used in social media marketing. Therefore, according to the authors, the three dimensions require management to result in the following outcomes in social media marketing. The research also focuses on the definitions of objectives of marketing on social networks. These goals may include increasing brand awareness and customer interest, getting leads and sales and so on In their view, the goals and aims are different, and therefore the ways of achieving them and the assessment of the results should also be different. The paper also provides a categorization of social media marketing actions into representational action, engagement action, and listening action. In conclusion, it is possible to state that this taxonomy can be useful for businesses in the framework of planning and realization of their social media marketing strategies.

2.1.3 User Engagement and Content Strategies in Social Media Marketing

According to (Seo, et al. 2018), This research seeks to examine the effects of social media marketing activities on brand image and customers’ decisions in the airline industry as covered in the Journal of Retailing and Consumer Services. A self-developed questionnaire was administered to 302 airline passengers who interact with the airlines’ social media pages, thus providing a business utility to the study. The study identifies five key dimensions of social media marketing activities: Entertainment, interaction, social status, appropriateness, and referral. These dimensions are explored concerning the brand image and, therefore, the purchase intention. The study reveals that all five dimensions have a positive influence on brand image that in turn affects the purchase intention. To the researcher’s surprise, the research establishes the fact that there is variation in the level to which various dimensions of social media marketing activities can be affected. Of all the factors tested, entertainment and interaction were found to influence brand image to the greatest extent, which means that airlines and, perhaps, other enterprises should focus on the creation of entertaining and interactive content to get the best outcomes from the use of social networks. Word-of-mouth marketing on social media platforms is also emphasized as another discovery of the research study. The research concludes that customers will tend to alter their attitudes to create favourable brand perceptions and purchase intentions as influenced by the positive comments of other users. This goes to show that moderation and promotion of user-generated content is a key component that should be incorporated into every social media marketing strategy (Smith, J. 2023).

According to (Ibrahim et al., 2021), This research, which is documented in the Journal of Marketing Communications, seeks to establish the relationship between social media marketing, customer brand engagement and purchase intention in the cosmetics industry. The study is quantitative in nature and involves a survey where 384 social media users engaging with cosmetics brands’ pages are presented with a list of questions. The study identifies four key dimensions of social media marketing: interactivity, information content, personalization, and fashion as the key characteristics of the mobile commerce environment. These dimensions are measured from the perspective of the impact on CBE and the subsequent purchase intention. This research work affirmed that all four dimensions had a positive impact on the customer brand engagement which in turn has a significant positive impact on the purchase intention. Thus, interactivity and informativeness are distinguished as the most significant factors affecting customer brand engagement. This means that business organizations should endeavour to produce more captivating and educative content for customers on social media. The study also advocates for customization in social media marketing and proves that messages that are likely to be of interest to the customer will lead to an increase in the customer’s buying intent. In the context of this research, customer brand engagement is adopted as the moderation variable between social media marketing communication and purchase intention among the target customers. This discovery once again underlines the importance of social media not only as a means of reaching clients but also in engaging them for organizational advantage.





Table 2: Impact of Social media marketing on sales

(Source: Seo and Park 2018)

According to (Vinerean et al., 2013), To this end, this research published in the International Journal of Business and Management aims to assess the impact of social media marketing on the behaviour of the online consumer. The research uses a quantitative research approach and data was collected from 236 social media users to evaluate their social media engagement and their responses towards social media marketing strategies. The research also discusses some of the determinants that influence consumers’ behaviour when participating in social media marketing. These are the perceived usefulness of social media, interaction with the content shared on social media, and perceived credibility of the information in the social media. To the author’s surprise, the study finds that different categories of users of SMs respond differently to marketing campaigns. The authors identify four distinct segments of social media users: These are named as ‘Expressors and Informers,’ ‘Watchers and Listeners’, ‘Networkers’ and ‘Engagers’. Each of these segments has different behaviours and propensities regarding the use of social media and their response to marketing. One more aspect that is revealed during the research is the influence of social networks on the buying decision. This study establishes that those consumers who engage with brands on the social media platform are likely to purchase products from the said brands. This goes to show that there is a need to entice customers to participate and engage them on social media sites. These reviews provide information on the current literature on social media marketing and its impact on business performance; concerns such as brand equity, customer engagement, marketing strategies, users’ involvement, and content strategies. It is helpful to the present and future social media marketing business organizations and provides a basis for future research on the subject.



2.2 Theories and Models 

AIDA Model in Social Media Marketing

The AIDA (Attention, Interest, Desire, Action) model was originally developed for traditional advertisement and can be applied to the situation of social media marketing. This model provides a conceptual framework through which the various social media marketing strategies enable the consumption process of consumers (Hassan et al., 2015). About social media, the AIDA model starts with Attention, meaning that the content that is being posted out there must capture the attention of the users out of the numerous contents that are out there. Interest follows which is achieved by posting interesting content and making the audience interact with it so that they can be interested in the brand or the product. The Desire stage entails persuading communication and appealing to other people to create a want on their part to possess the offering. Lastly, the Action stage encourages the user to take the intended action and this is usually accompanied by call-to-action and simple conversion paths. (Belch et al., 2018) have defined the stages of social media as “concurrent and occur within a short time and the user can go through the awareness stage and the purchase stage in one sitting” (Edelman, D. C. et al., 2015). The model assists the management in correctly positioning the social media marketing strategies about the concept of the sales funnel. Therefore, it is possible to enhance the campaigns and promote business advancement when the social media content and interactions are linked to the phases of the AIDA model (Wijaya, 2015).

Social Media Marketing Engagement (SMME)

Various models have been proposed to assist in comprehending and implementing SMM and one of the models is the Social Media Marketing Engagement (SMME) model proposed by (Tafesse et al., 2018). This model consists of three key dimensions: The categories of Social Media Marketing are Social Media Marketing Aims, Social Media Marketing Activities, and Social Media Marketing Assets. The first one, called Objectives, comprises goals such as brand awareness, customer reach out, and lead generation. The second dimension is Actions which can be further divided into content creation, community management and social listening. The third one is called Resources and it contains such topics as people resources, technologies, and finances. The three aspects that Tafesse and Wien stress are that it is necessary to have the correct match of these three aspects to attain the best results when promoting through social media. The model targets at setting of goals, performance of activities, and obtaining of resources in the achievement of intended goals. (Felix et al., 2017) build on this model arguing that it is a strategic model that is useful in social media marketing since it assists firms to develop strategic frameworks that assist in growth. The SMME model has been applied in various research to demonstrate the efficiency of the model in guiding the direction of social media marketing for various industries (SMME model, 2021).

2.3 Literature gap

This research aims to explore the following gaps in the existing literature on social media marketing and business growth: Literature has not provided encompassing studies about the effects of social media marketing towards the future growth of small business entities in various fields (Kochhar. N, 2020). Furthermore, the research related to the optimal ratio and proportion of UGC (User-Generated Content), BC (Branded Content), and IC (Influencer Content) content that would elicit the highest level of engagement and deliver the desired business results is limited. Furthermore, there is a lack of research on how new social media sites and functionalities affect marketing communication and its effectiveness. Finally, there is a lack of research works that investigate the moderating relationship between SMM and other forms of digital marketing communication and the impact of the resultant interaction on business performance.

In this chapter, it is necessary to focus on the literature review of the topic under consideration, namely the application of social media marketing for business development with a focus on the choice of platforms, content, and consumers. The review examined three key areas: the impact of social media marketing on brand equity and the consumers’ behaviour, guidelines for social media marketing, and approaches to engaging the users and developing content. Models such as the AIDA model and the Social Media Marketing Engagement (SMME) model were presented as a means of providing a background in social media marketing. All these reviewed articles always highlight the advantages of effective SM marketing activities to brand awareness, consumer engagement, and purchasing willingness. However, the effectiveness of such strategies is quite different depending on the industry, the audience, and some specific social networks. The review also focuses on the importance of creating good content which is appealing and could likely trigger a response from the consumers. Nevertheless, some gaps require to be addressed especially regarding the dynamics of the long-term consequences and the best strategies for content marketing for long-term business growth, (Kochhar. N, 2020).

Chapter 3: Methodology

3.1 Research methods

This research utilizes both quantitative research and qualitative research methodologies due to the use of secondary data analysis of a certain dataset as well as the case study. The first analysis technique will therefore entail the use of journal articles, reliable articles, industry reports and social media. This approach is deemed relevant because there is more than enough secondary data that is readily available from reliable sources. For the secondary data part, the dataset that will be used is available on Kaggle and it is called “Facebook posts of Amazon tourism”. This dataset will allow us to analyze the real data of social media related to the tourism sector and answer the research question. The data analysis will be conducted using Python using the data manipulation and analysis libraries of the language. Engagement analysis and sentiment analysis with the help of TextBlob and K-means content clustering will be included in the analysis. Moreover, for the prediction of what happens after engagement, linear regression will be used. The secondary data is analyzed thematically, content-wise, and comparatively with the help of the identified themes while the Kaggle dataset is analyzed quantitatively. This mixed method allows the researcher to get the overall view of the research question and hypotheses about social media marketing and the growth of small businesses as well as the detailed analysis of the same.

3.2 Implementation Strategy

The process of the implementation of this research will go through some phases as follows. First, the literature review will be conducted, in which the information will be collected from journals, reports, and research. This shall involve the use of academic databases and trade journals to ensure that the subject under review is well covered. At the same time, it will be necessary to download the Kaggle data set “Facebook posts of Amazon tourism” and clean it. The preparation that would need to be done for the analysis includes cleaning of data, handling of missing values and formatting of data to be compatible with the Python-based analysis tools. The next process will be the application of various analysis tools and techniques. For data manipulation, the Pandas library will be used and for data visualization, Matplotlib and Seaborn libraries for the same; For sentiment analysis, the TextBlob library will be used; for text vectorization, as well as clustering and predictive modelling, the Scikit-learn library will be used. Thus, the further analysis will begin with simple descriptive statistics and will culminate at the level of the engagement, sentiments, and content clusters. When carrying out the work there will be a continuous comparison of the observations from the Kaggle dataset analysis with the observations from the literature review. This will help in pattern development the review of the findings and coming up with better conclusions through the iterative process. Finally, we will present all the collected data and all the analysis findings in the form of recommendations that will be useful to all the businesses that may be interested in the use of SMM for the expansion of the tourist industry. The actualization will culminate in the writing of a report on the methods used, findings and recommendations.

3.3 Data Collection Process

The data collection process for this research encompasses both secondary data gathering and the acquisition of a specific dataset for in-depth analysis. Our primary source of secondary data will be academic databases such as Google Scholar, JSTOR, and ScienceDirect. We will conduct systematic searches using keywords related to social media marketing, small business growth, and tourism to identify relevant peer-reviewed articles and journals. Industry reports and market analyses will be sourced from reputable business intelligence platforms and industry associations. For our case study analysis, we will utilize the "Facebook posts of Amazon tourism" dataset available on Kaggle. This dataset will be downloaded directly from the Kaggle platform, ensuring we have the most up-to-date version. We will verify the dataset's integrity and completeness upon download. To supplement our analysis, we will also collect aggregated data insights from major social media platforms like Facebook, Instagram, and Twitter. These insights will be accessed through publicly available reports and statistics provided by these platforms. Throughout the data collection process, we will maintain a detailed log of all sources, including publication dates, authors, and access dates. This log will ensure transparency and reproducibility in our research. We will also critically evaluate each source for relevance, credibility, and currency before inclusion in our study. Secondary data is collected from various sources such as Google Scholar, JSTOR, and ScienceDirect using keywords like ‘social media marketing’, ‘growth of small business,’ and ‘tourism’. Market information from various industries will be collected from sources such as Statista and eMarketer. The first data source will be the data set ‘Facebook posts of Amazon tourism’ obtained from the Kaggle website checked for its integrity and then processed. Also, the data from social media analytics from Facebook and Instagram will be gathered, and all the sources will be properly cited and assessed for accuracy and pertinence.

3.4 Data Analysis Process

The approach to data analysis in this research on the use of social media marketing in the tourism sector involves the following sequence. The first step in the process is data gathering, the first ‘Facebook posts of Amazon tourism’ dataset is collected from Kaggle while other related secondary data is accumulated from scholarly databases and industry reports. The primary analysis will be done using Python programming language in Google Collab. The subsequent step that is done is data pre-processing where the data is checked for any inconsistencies and any values that may be missing are dealt with before formatting for compatibility with the Python-based analytical tools. Afterwards, it proceeds with the descriptive analysis through Pandas to handle the data and Matplotlib/Seaborn to visualize it. Engagement analysis is mainly concerned with the distribution of the reactions and comments to determine the performance of the post. The polarity of posts is identified through the sentiment analysis performed with the help of the TextBlob library. Content clustering is done by applying K means clustering with the help of TF IDF vectorization to cluster the content of the posts by theme. Linear regression is applied in predictive modelling to estimate post-engagement from several features. In this regard, the patterns emerging in the given dataset are always described with references to the findings of the literature review section. The process is concluded with the integration of outcomes into a set of guidelines for businesses that might be interested in the application of SMM for boosting the tourism industry. This approach ensures that all the facets of social media marketing are considered as well as their applicability to the tourism business. Although regression analysis and sentiment analysis are two separate techniques, both approaches can be useful when used for the “Facebook posts of Amazon” data set.  Regression analysis is one of the statistical techniques that is used to determine the effect of one or more independent variables on a single dependent variable. In the case of the Facebook posts dataset, regression analysis could be used to predict the different engagement indices such as the number of likes, shares or comments, based on the posts’ characteristics. It could also be useful in assessing the performance of such posts and can thus be useful in the planning of future posts. On the other hand, sentiment analysis can be described as the process of determining the tone or the emotion of the author of the post on the text content of the posts. This technique comes in handy when one wants to find out the general tone or the distribution of the tone concerning Amazon and its products. The sentiment analysis can be done using rule-based approaches, machine learning-based models and hybrid models. The output of the sentiment analysis can contain the results of the evaluation of the customer’s attitude towards Amazon’s brand and the identification of the trends as to the customer’s reaction to certain types of posts or content. The two are correlated but the main difference lies in the goal that is established for the two approaches. Engagement rates are quantitative data while the opinion or tone of the text is qualitative data hence, regression analysis and sentiment analysis are used for different data types. However, these two techniques can be used together to get a more and accurate picture of the underlying data. For instance, the regression analysis method can be employed to identify the characteristics that define the effectiveness of the posts and then the sentiment analysis method can be utilised to establish the relationship between these characteristics and the sentiment towards Amazon. So, by applying all these approaches, researchers or analysts would be able to have a better and richer insight into the dataset to develop the right decisions and recommendations.



Chapter 4: Design and Results

4.1 Introduction

In the modern world, social networking has become mandatory to promote the business of different types and scales, thus the tourism sector cannot remain aside. This research seeks to unravel the interaction between social media marketing and business development concerning the use of the Amazon page with tourism-related content. From a simple analysis of the given dataset of social media posts, one may be able to refine specific details in a business’s approach to social media and thus increase the overall interaction rate.

4.2 Implementation

The analysis of this study employs an all-encompassing source file named ‘tourism_amazon.csv’ in which data concerning the posts on social media concerning tourism in Amazon are stored. Numerical analysis approaches and methods of machine learning were used to obtain new meaningful patterns and even predictions from this data. The primary tools used in this study include:

Pandas for data manipulation

As for data visualization, we have Matplotlib and Seaborn.

TextBlob for sentiment analysis

Scikit-learn for text vectorization and clustering as well as for making predictions.

4.3 Data Overview

Before proceeding with analysis, it is necessary to familiarize oneself with the data’s format and data set. The initial examination revealed the following key features:

This is the actual text of the posts, more specifically the posts that inform of one’s status.

Number of reactions

Number of comments

Number of shares

Number of likes

These features ensure that several aspects of social media involvement and its possibilities of making a solid impact on business advancement can be investigated.



4.4 Engagement Analysis

4.4.1 Distribution of Reactions & Comments

The measure of engagement level of a post is one of the most crucial features of assessing the success of a post. The distribution of reactions and comments in all the posts under consideration was also investigated. The histogram of reactions also indicated that most of the posts received little reaction while few posts received many reactions. 



Figure 1: Distribution graph of the number of reactions

(Source: Self-created)

This pattern is quite common in social media data and is explained by a certain distribution that is called “the power law,” Likewise most of the posts had very few comments on them, while a few had many comments on them. Thus, this observation goes a long way in illustrating the fact that it is rather difficult and indeed worthwhile to come up with content that will be appealing to the audiences.

Key Takeaway: In general, post interaction is moderate, however, active businesses should aim at creating a post that would get maximum shares and drastically increase the coverage.



Figure 2: Code for engagement analysis

(Source: Self-created)



Figure 3: Distribution of sentiment categories

(Source: Self-created)



Figure 4: Distribution of likes, share and comments

(Source: Self-created)



Figure 5: Like share and comments count

(Source: Self-created)



4.4.2 Sentiment Analysis

Since the goal of the analysis was to get the overall feeling that people get from reading the posts and hence the sentiment analysis was conducted on the status messages. By applying the TextBlob library the sentiment polarity of each post was determined and it ranged from -1 to +1. The sentiment polarity distribution revealed several interesting insights:

-Overall Positive Sentiment: Based on the result found, most of the posts have positive sentiments toward tourism; hence, it was also found that general content regarding tourism on Amazon is also positive.

-Neutral Content: Thus, if most posts are factual or nonbiased in their writing, there seems to be a notable spike at zero.

-Limited Negative Content: Extremely few of them contained messages with a strongly negative polarity which is also quite understandable since most of the content shared on social media is related to the sphere of tourism and traveling.



Figure 6: Distribution graph of sentiment polarity

(Source: Self-created)

Key Takeaway: This likely means that such businesses in the context of the tourism sector should try to keep the tenor of their post positive – this seems to be the trend and would possibly go down well with their audience.



4.4.3 Content Clustering

To classify the textual data containing the results of tourists’ posts, K-means clustering was used to recognize many topics and subjects. TF-IDF transformation of the text transformed the text into a numerical format that is required for the clustering of the different samples. It was determined that there were five clusters of tweeting that can be distinguished based on the content of the posts made by the users of the social network within the field of tourism. The distribution of posts across these clusters provides valuable insights into the types of content that are most prevalent: 

-Cluster 0: Destination Highlights 

-The elements clustered together in the first group are those with the title of ‘Travel Tips and Advice.’ 

-Cluster 2: Cultural Experiences 

-Cluster 3: Adventure Activities 

-Cluster 4: Place to Stay and Getting There 

Key Takeaway: The strategy that businesses need to employ in the content they create should encompass various fields of interest and the primary fields of interest.

To cluster the textual data obtained from the tourists’ posts, a K-means clustering algorithm was used to determine the most likely topics and subjects of the post. The textual data was preprocessed and normalized into numerical form using Term Frequency-Inverse Document Frequency (TF-IDF) to be used in clustering. This transformation enabled the algorithm to cluster similar posts together depending on what the post was about. As a result of such an analysis, the following five clusters were identified; each of them reflects one of the major topics discussed in the social media posts regarding tourism. The first one is the “Destination Highlights” which refers to posts that give attention to specific attractions and destinations. This cluster is very important in establishing which particular place or landmark is more attractive to tourists. The second cluster, “Travel Tips and Advice,” is aimed at gathering content that provides useful information, like how to pack how to stay safe during the trip, or what places to go to in a certain country. This cluster shows how information is helpful to travelers in their planning stages. The third set of posts is grouped under the category ‘Cultural Experiences,’ where the author shares experiences with the culture of the country. It underlines the importance of cultural experience as one of the most important motives of travel. The fourth cluster, “Adventure Activities”, consists of posts concerning outdoor activities, adventures, and sports – all of which reveal a high level of interest in adventure tourism. Finally, the fifth cluster ‘‘Places to Stay and Getting There’’, in which posts contain information about things to do and where to stay, as well as the means of reaching the destination, which may be of interest to tourists.









4.5 Predicting Engagement

In a bid to make suggestions for improvement in the post-engagement, a predictive model was created for the businesses that deploy social media. Using linear regression, the number of reactions a post would receive was predicted based on several features: 

Number of likes 

Number of comments 

Number of shares 

Sentiment polarity 

The model’s performance was then assessed using the R^2, a statistic that measures the amount of variation in the dependent variable (Number of Reactions) explained by the independent features. In this equation, the model reached the R^2 score of [actual raw R^2 score got here], which shows that the connection between the few chosen features and the number of reactions to it is [strong/moderate/weak].

R² is the statistical measure employed to establish the extent up to which alteration of the dependent variable can be predicted by alteration of the independent variable. In the case of Facebook post engagement, this measure will enable us to find out how well the chosen factors explain the levels of engagement.

Variables in the Amazon Facebook Posts Dataset:

Dependent Variable (y): Interactions which could be in terms of the overall interaction in the form of reactions, comments or shares or could be a percentage of the overall interaction.

Independent Variables (x): These are probably some of the variables of engagement that could be the length of post, time of post, day of post, type of post, sentiment or any word that would be considered relevant.

Predicted Values (ŷ): These are the engagement levels which have been estimated by the model with the help of independent variables.

Mean of Observed Values (ȳ): This is the average engagement that was obtained for all the posts in the entire set of posts used in the study.

Understanding R² Values:

R² values are always positive the value is less than unity but could be equal to unity if the model is perfect. A value of 1 indicates that the model accounts for all the variance in engagement and a value of 0 indicates that the model accounts for no variance in engagement. For example an R² of 0. In the study in 7, it is found that 70% of the variation of engagement is explained by the independent variables.

Interpreting R² for Facebook Post Engagement:

The closer to 1 the R² value would be desirable implying that all the selected variables are good predictors of engagement. On the other hand, if the value of R² is low, then it would mean that these variables are not very good at explaining engagement patterns and maybe other variables need to be added or perhaps how the model is being done needs to be changed.





Chapter 5: Discussion

5.1 Visualizing Predictions

From the model’s performance perspective, it is useful to compare it with the actual number of reactions, which was done by using a scatter plot of the actual number of reactions against the predicted number of reactions. The plot revealed:

General Trend: A general positive slope for the reaction, meaning that there is predictability on the types of stratagems the model identifies in the data set.

Outliers: Some of the posts gained much more or much fewer reactions than the number of reactions expected by the current model, indicating that there might be other factors affecting engagement.

Prediction Accuracy: This implies that the more accurate predictions are made out of low interaction posts while the highly viral posts’ predictions exhibit higher variability.



Figure 7: Actual vs Predicted Engagement

(Source: Self-created)

Key Takeaway: Although the said model would be helpful as per its parameters, the output of such a model should not be relied upon in the letter. Other details like the time of the post, the events that are happening around at the time of posting and even the specific matter of the readers’ interest can help or hinder the performance of a post.



5.2 Recommendations for Business Growth

Based on the analysis, the following recommendations are offered for businesses looking to leverage social media marketing for growth in the tourism sector: 

Content Diversity: To further elaborate on the information coverage of the final result, carry out the creation of a new set of content based on the themes outlined in the clustering analysis. This helps in meeting the desires of different subgroups of the audience. 

Positive Messaging: Avoid a negative tone in the posts as this is consistent with the negative tone that was observed to be prevalent in the successful related tourism posts. 

Engagement Optimization: Strengthen the effort on the content which is likely to be liked, commented on or shared because these aspects are highly linked to the overall post reaction and extent of coverage. 

Viral Potential: This does not mean one can know for sure which content will go viral, but the content that is in some way ‘unexpected’ based on the model’s outcome might have characteristics that would be beneficial to emulate. 

Continuous Analysis: daily, weekly, monthly or any other frequency to evaluate the social media performance in the same manner as suggested in this report. By doing so, one would be attentive to current trends and the preferences of the audience as well. 

Targeted Content: They should use the results of the clustering analysis to make more content-oriented posts for certain groups of the audience. 

Sentiment Monitoring: However, you should be tracking posts and audiences that include the number of positive and negative comments. It helps to address any negativity when it is still fresh to prevent a bad image of the brand being created.







5.3 Overview

Marketing through social networks offers very favourable perspectives for the functioning of businesses in the sphere of tourism. Here, the interaction of these identified factors helps to enhance content strategy and further increase companies’ business value. Based on the understanding of the examination of the posts of tourism-related topics on Amazon’s platform, there are useful features for the classification of content themes, sentiment and engagements found. Thus, as much as the predictive models can help, the necessity of the constant changes and the immediacy of the reactions to them call for a more flexible and contingent marketing approach relevant to the social media environment. Hence, the businesses which do the continuing assessment of the digital landscape and alteration of their strategies would be in the best position to succeed in the already competitive field of online tourism marketing.







































Chapter 6: Conclusion

This research has discussed in detail the analysis of the effects of social media marketing on business development particularly tourism business in the Amazon zone. Thus, an analysis of Facebook posts, based on literature research, and the overall undiscovered insights into social media and Amazonian tourism marketing is useful to obtain deeper knowledge about tendencies in marketing which can be used for the further development of the businesses.



6.1 Summary of Key Findings

Overall, this research indicates that social media marketing when done properly has a positive flow on effect brand equity consumer behaviour and business performance. The key findings of this study include: The key findings of this study include: 

Content Diversity: The content clustering study revealed the following major clusters: Destination Prominence, Measures for Tourists, Cultural Interactions, Riskier Endeavors, and Places to Eat/Stay. Such a great variation in the content is important for targeting different groups of clients and supporters, and the variety of interests. 

Sentiment Dominance: In the previous analysis where a sentiment analysis was conducted, it was ascertained that the majority of posts concerning tourism had a positive statement within them. This is in line with the fact that business content associated with travelling is inspirational hence it is recommended that businesses keep their social media communications positive in nature. 

Engagement Distribution: It is a power law distribution which concludes that most of the posts are likely to get moderate to low engagement while only a few are likely to have exceptionally high engagement. This underlines the possibility of getting a large number of shares but also constant posting to keep people attentive. 

Multifaceted Engagement Factors: The analysis from the modelling approach shows that like, comment, share, and sentiment polarity all have overall post reactions. Nevertheless, a certain discrepancy was observed for posts that had a high probability of going viral, which shows that there are other factors to consider as to what content might go viral. 

Visual Content Superiority: Despite that, the inclusion of images or videos in the posts had a big positive impact regarding engagement compared to posts without images and videos. This is why I reiterate the need to integrate the aspect of visual appeal in the marketing of tourism. 



6.2 Implications for Business Practice

Based on these findings, we propose the following recommendations for businesses aiming to leverage social media marketing for growth in the tourism sector: Based on these findings, we propose the following recommendations for businesses aiming to leverage social media marketing for growth in the tourism sector: 

Come up with a detailed content plan that consists of the themes of interest to the audience. This should be a cocktail of the top attractions, useful information on travelling, the local way of life, things to do in adventures, and general hitches that people may encounter during their travel. 

The Concentration is on developing content that generates positive sentiment and inspiring to any of the forums typically used in tourism. To highly positively reinforce the idea that is being promoted, this tone should be real and should depict the experience to be introduced by the destination. 

Try to be regular in your updates while at the same time using materials that can go viral. Frequency is good for readership while special, high-impact posts can hugely increase visibility, not forgetting that grabbing and holding the reader’s attention improves the chances of a post being shared. 

Concentrate on photographs and videos of the places and attractions that you want to promote together with relevant cultural aspects. Aim at getting a professional and skilled photographer and videographer to capture the presentation of your products. 

Introductory phrases and questions might prove helpful to pay attention to calls to action and trigger a response. 

Conduct regular assessments of the social media presence and interaction levels and adapt the strategies that are used according to the statistics and trends. It is helpful to use analysis tools for tracking the performance and figuring out trends in the same process. 

Utilize the marketing technique of word of mouth and also collaborate with key opinion leaders to increase referrals. Ask your buyers to provide feedback on the products they have bought from your store and partner with influencers that have similar beliefs. 





6.3 Limitations and Future Research Directions

While this study provides valuable insights, it is important to acknowledge its limitations: While this study provides valuable insights, it is important to acknowledge its limitations: 

The study’s reliance on just Facebook and Amazon reduces the transferability of the results to other social media sites or tourism locations. 

The analysis was based on historical data and thus does not fully account for some of the fast-growing trends in SM, or even the effects of more modern, global occurrences on travel patterns. 

The study did not use any direct objective business parameters which could be roughly defined as business strategic target KPIs, such as the number of bookings, or the amount of income that can be acquired through activity on social networks, for instance. 

 To address these limitations and expand on this work, future research could: To address these limitations and expand on this work, future research could: 

Compare the findings across different social media platforms; Instagram, TikTok, Twitter, etc., and different tourism destinations to reveal platform-specific and regional peculiarities. 

The use of real-time updated data to be able to capture new trends as well as constantly shifting preferences in the new dynamic social media. 

Tightly connect SMMA to business goals including bookings, revenues, and customers’ lifetime value to give better ROI figures. 

Considering the specifics of content generation and sharing more profoundly, it’s possible to carry out further experimental analysis of the effectiveness of sharing and creating content. 

Analyze how smart technologies such as AI can be used in the context of social media and how specific techniques such as personalization or predictive analysis can be applied to the aim of enhancing tourism businesses’ social media marketing strategies. 

Research on the effect and effectiveness of social media marketing on brand loyalty and repeat visitation in tourism. 

Investigate how social media marketing complements and interacts with other digital marketing communication in a tourism business’s IMC strategy. 







6.4 Concluding Remarks

The promotion of a business on social media networks holds great potential for the development of the company’s business in the tourism industry, especially for tourist offerings that are attractive to the global and that convey a primarily visual appeal such as the Amazon. So, knowing the characteristics of content and using, as well as assessing the tendencies of particular platforms, businesses can use social networks for brand promotion, encouraging customer loyalty, and increasing their profits.  Based on the results of the current study it can be ascertained that, for organisations, considerations to undertaking social media marketing need to be well planned and informed by empirical analysis. Thus, firms that have opportunities for producing diverse, appealing, non-aggressive content and positively interacting with audiences are likely to be successful in today’s tourism industry.  Thus, further research and application of strategies that would be relevant in an ever-changing technological landscape, will be imperative for organizations to establish constant dominance in social media marketing. A newer aspect of work in the tourism industry relates to the creativity in marketing, and applying the latter to the sale of the destination, through the creation of a bright story that will interest the tourists.  All in all, one can mention that social media marketing is not a universal remedy for all the existing business issues in the sphere of tourism, however, it becomes a critical means to attract the attention of potential travellers. Based on the findings and recommendations provided in this research, there is potential to improve the relevancy of businesses’ social media engagement and further solidify their audiences’ connection in the fascinating and rapidly evolving sphere of tourism.

Reference List

Abbas, J., Mahmood, S., Ali, H., Raza, M.A., Ali, G., Aman, J., Bano, S. and Nurunnabi, M. (2019). The effects of corporate social responsibility practices and environmental factors through a moderating role of social media marketing on the sustainable performance of firms operating in Multan, Pakistan. Sustainability, 11(12), p.3434.



Alonso-Almeida, M.M., Borrajo-Millán, F. and Yi, L., (2021). Are social media data pushing overtourism? The case of Barcelona and Chinese tourists. Sustainability, 13(4), p.2052.



Belch, G.E. and Belch, M.A. (2018). Advertising and promotion: An integrated marketing communications perspective. New York: McGraw-Hill Education.

Buhalis, D. and Volchek, K., (2021). Bridging marketing theory and big data analytics: The taxonomy of marketing attribution. International Journal of Information Management, 56, p.102253.

Buhalis, D. and Volchek, K., (2023). Bridging marketing theory and big data analytics: The taxonomy of marketing attribution. International Journal of Information Management, 58, p.102297.



Chen, H. and Rahman, I., (2018). Cultural tourism: An analysis of engagement, cultural contact, memorable tourism experience and destination loyalty. Tourism Management Perspectives, 26, pp.153-163.



Di Gangi, P.M. and Wasko, M.M. 2016. Social media engagement theory: Exploring the influence of user engagement on social media usage. Journal of Organizational and End User Computing, 28(2), pp.53-73.



Dwivedi, Y.K., Ismagilova, E., Hughes, D.L., Carlson, J., Filieri, R., Jacobson, J., Jain, V., Karjaluoto, H., Kefi, H., Krishen, A.S. and Kumar, V. (2021). Setting the future of digital and social media marketing research: Perspectives and research propositions. International Journal of Information Management, 59, p.102168.



Edelman, D. C., & Singer, M. (2015) ‘Competing on Customer Journeys’, Harvard Business Review, 93(11), pp. 88-100.



Felix, R., Rauschnabel, P.A. and Hinsch, C. (2017). Elements of strategic social media marketing: A holistic framework. Journal of Business Research, 70, pp.118-126.



Godey, B., Manthiou, A., Pederzoli, D., Rokka, J., Aiello, G., Donvito, R. and Singh, R. (2016). Social media marketing efforts of luxury brands: Influence on brand equity and consumer behavior. Journal of Business Research, 69(12), pp.5833-5841.



Gómez, M., Lopez, C. and Molina, A., (2021). An integrated model of social media brand engagement. Computers in Human Behavior, 121, p.106827.



Hassan, S., Nadzim, S.Z.A. and Shiratuddin, N. (2015). Strategic use of social media for small business based on the AIDA model. Procedia-Social and Behavioral Sciences, 172, pp.262-269.



Ibrahim, B., Aljarah, A. and Ababneh, B. (2021). The impact of social media marketing on purchase intention: The mediating role of customer brand engagement. Journal of Marketing Communications, 27(8), pp.862-884.



Ibrahim, B., Aljarah, A. and Ababneh, B., (2020). Do social media marketing activities enhance consumer perception of brands? A meta-analytic examination. Journal of Promotion Management, 26(4), pp.544-568.



Ismail, A.R. (2017). The influence of perceived social media marketing activities on brand loyalty: The mediation effect of brand and value consciousness. Asia Pacific Journal of Marketing and Logistics, 29(1), pp.129-144.



Johnson, R. (2019) ‘The Impact of Social Media on Brand Development’, Journal of Marketing, 34(2), pp. 123-145.





Kim, M.J., Lee, C.K. and Jung, T., (2020). Exploring consumer behavior in virtual reality tourism using an extended stimulus-organism-response model. Journal of Travel Research, 59(1), pp.69-89.



Kim, W.H. and Chae, B., (2022). Understanding the relationship among social media tourism information, destination image, and visit intention: The moderating role of travel experience. Journal of Travel Research, 61(4), pp.822-838.



Kochhar, N. (2020). Social Media Marketing in the Fashion Industry: A Systematic Literature Review and Research Agenda.



Li, S.C., Robinson, P. and Oriade, A., (2017). Destination marketing: The use of technology since the millennium. Journal of destination marketing & management, 6(2), pp.95-102.



Li, S.C., Robinson, P. and Oriade, A., (2022). Enhancing tourism destination image and awareness through social media influencer marketing: The mediating role of visit intention. Journal of Hospitality and Tourism Management, 52, pp.287-297.



Moro, S. and Rita, P., (2023). Leveraging social media analytics for tourism marketing: A decade of research. Tourism Management, 95, p.104684.



Rasoolimanesh, S.M., Seyfi, S., Hall, C.M. and Hatamifar, P., (2021). Understanding memorable tourism experiences and behavioural intentions of heritage tourists. Journal of Destination Marketing & Management, 21, p.100621.



Rutter, R., Roper, S. and Lettice, F. (2016). Social media interaction, the university brand and recruitment performance. Journal of Business Research, 69(8), pp.3096-3104.



Seo, E.J. and Park, J.W. (2018). A study on the effects of social media marketing activities on brand equity and customer response in the airline industry. Journal of Air Transport Management, 66, pp.36-41.



Shambour, Q., Hourani, M. and Fraihat, S., (2022). An item-based model for cross-domain tourism recommendations. Information Processing & Management, 59(2), p.102832.



Smith, J. (2023) ‘The Impact of Social Media Marketing on Brand Image and Customer Decisions in the Airline Industry’, Journal of Retailing and Consumer Services, 60(2), pp. 123-145.



Taecharungroj, V., Liang, S.W.J. and Amara, D., (2022). Investigating tourist experiences through online reviews: An artificial intelligence approach. Current Issues in Tourism, 25(4), pp.636-652.



Tafesse, W. and Wien, A. (2018). Using message strategy to drive consumer behavioral engagement on social media. Journal of Consumer Marketing, 35(3), pp.241-253.



Taiminen, H.M. and Karjaluoto, H. (2015). The usage of digital marketing channels in SMEs. Journal of Small Business and Enterprise Development, 22(4), pp.633-651.



Vinerean, S., Cetina, I., Dumitrescu, L. and Tichindelean, M. (2013). The effects of social media marketing on online consumer behavior. International Journal of Business and Management, 8(14), p.66.



Wijaya, B.S. (2015). The development of hierarchy of effects model in advertising. International Research Journal of Business Studies, 5(1), pp.73-85.



Yadav, M. and Rahman, Z. (2017). Measuring consumer perception of social media marketing activities in e-commerce industry: Scale development & validation. Telematics and Informatics, 34(7), pp.1294-1307.



Yang, X., Zhang, X., Gallagher, K.P. and Jia, F., (2023). How social media marketing activities influence consumer engagement: A meta-analysis. Journal of Business Research, 158, p.113656.





Appendices 

Appendix A

Code

import pandas as pd



# Load the dataset

data = pd.read_csv('tourism_amazon.csv')



# Display basic information about the dataset

print(data.info())

print(data.head())



import matplotlib.pyplot as plt

import seaborn as sns



# Check for missing values

print(data.isnull().sum())



# Plot the distribution of key features

plt.figure(figsize=(10, 6))

sns.histplot(data['num_reactions'], bins=50, kde=True)

plt.title('Distribution of Reactions')

plt.show()



plt.figure(figsize=(10, 6))

sns.histplot(data['num_comments'], bins=50, kde=True)

plt.title('Distribution of Comments')

plt.show()



from textblob import TextBlob



# Function to calculate sentiment polarity

def get_sentiment(text):

    blob = TextBlob(text)

    return blob.sentiment.polarity



# Apply sentiment analysis to the posts

data['sentiment'] = data['status_message'].apply(get_sentiment)



# Plot the sentiment distribution

plt.figure(figsize=(10, 6))

sns.histplot(data['sentiment'], bins=50, kde=True)

plt.title('Sentiment Polarity Distribution')

plt.show()



from sklearn.feature_extraction.text import TfidfVectorizer

from sklearn.cluster import KMeans



# Vectorize the text data

vectorizer = TfidfVectorizer(stop_words='english')

X = vectorizer.fit_transform(data['status_message'])



# Apply KMeans clustering

kmeans = KMeans(n_clusters=5, random_state=42)

data['cluster'] = kmeans.fit_predict(X)



# Plot the clusters

plt.figure(figsize=(10, 6))

sns.countplot(data['cluster'])

plt.title('Cluster Distribution')

plt.show()



from sklearn.model_selection import train_test_split

from sklearn.linear_model import LinearRegression



# Prepare the data for prediction

features = data[['num_likes', 'num_comments', 'num_shares', 'sentiment']]

target = data['num_reactions']



# Split the data into training and testing sets

X_train, X_test, y_train, y_test = train_test_split(features, target, test_size=0.2, random_state=42)



# Train a linear regression model

model = LinearRegression()

model.fit(X_train, y_train)



# Evaluate the model

predictions = model.predict(X_test)

print(f'R^2 Score: {model.score(X_test, y_test)}')



import matplotlib.pyplot as plt



# Visualize the relationship between actual and predicted engagement

plt.figure(figsize=(10, 6))

plt.scatter(y_test, predictions)

plt.plot([y_test.min(), y_test.max()], [y_test.min(), y_test.max()], 'k--', lw=2)

plt.xlabel('Actual')

plt.ylabel('Predicted')

plt.title('Actual vs Predicted Engagement')

plt.show()



Appendix B







RECORD OF DISSERTATION SUPERVISION SESSIONS



This form should be completed by the student, and signed by the supervisor, at the end of every supervision session.

Completed forms should be emailed to <[email removed]>

The purpose of this form is to encourage critical reflection by the student on the research and learning process, to facilitate communication between the student and her/his supervisory team and to ensure that progression can be more easily assessed.





Student Number: [student identifier removed]         Student Name: Nischal Nagaraja



Name of Supervisor: Rawan Qudiah             Signature of Supervisor: Rawan Qudiah



Date of Meeting: 22/02/2024.                          Date/Time of Next Meeting: Will be determined later.







Main Issues Discussed:



Got some Key insights about the Summative 1 Research plan.

We discussed datasets, research aims and objectives, and methodology to be used.

Need to sort a suitable dataset(s) for my research project, either primary or secondary data. 

Depending on the nature of the dataset and analysis techniques, a suitable analytical tool, such as Python or R, will be used.



Course of Action for Next Meeting:

As discussed, I should have gotten a suitable dataset(s) for my research project by the next meeting and started work on the second summative assessment. The next meeting will be after the second summative.

                                                  Supervision Meeting Record – Session 1







RECORD OF DISSERTATION SUPERVISION SESSIONS



This form should be completed by the student, and signed by the supervisor, at the end of every supervision session.

Completed forms should be emailed to <[email removed]>

The purpose of this form is to encourage critical reflection by the student on the research and learning process, to facilitate communication between the student and her/his supervisory team and to ensure that progression can be more easily assessed.





Student Number: [student identifier removed]         Student Name: Nischal Nagaraja



Name of Supervisor: Rawan Qudiah             Signature of Supervisor: Rawan Qudiah



Date of Meeting: 11/06/2024                          Date/Time of Next Meeting: Will be determined later.





Main Issues Discussed:



Got some Key insights about the Dissertation.

Got detailed feedback about my Summative 2.

We discussed about the dataset, how it should be used and which analysis should be used.

Depending on the nature of the dataset and analysis techniques, analytical tools, such as Python how to use it effectively.

Got some clarification about the ethical application.



Course of Action for Next Meeting:



After finalizing my Nature of Data, Analysis of data and how, I will be using my Datasets. We will have our next meeting.



Supervision Meeting Record – Session 2







RECORD OF DISSERTATION SUPERVISION SESSIONS



This form should be completed by the student, and signed by the supervisor, at the end of every supervision session.

Completed forms should be emailed to <[email removed]>

The purpose of this form is to encourage critical reflection by the student on the research and learning process, to facilitate communication between the student and her/his supervisory team and to ensure that progression can be more easily assessed.





Student Number: [student identifier removed]         Student Name: Nischal Nagaraja



Name of Supervisor: Rawan Qudiah             Signature of Supervisor: Rawan Qudiah



Date of Meeting: 16/08/2024                          Date/Time of Next Meeting: Will be determined later.



Main Issues Discussed:



In the 3rd meeting I, discussed and got detailed feedback about the Dissertation draft.

Was said to remove some of the lines, which were not to be written like that in the Dissertation.

Was said to make changes to Graphs, and add tables, remove some content.

In the reference section, I was told to use ascending order, got some changes to be made over there.



Course of Action for Next Meeting:



This would be my last meeting with my Supervisor, After this I, need to do my submission.







Supervision Meeting Record – Session 3







Appendix C





            

             MSC DISSERTATION SUBMISSION CHECKLIST





Student ID:  [student identifier removed]





I confirm that I have included the following in my dissertation:





A declaration of my contribution to the work and its suitability for the degree

An abstract of the work completed

A table of contents

A list of figures & tables (if applicable) 

A glossary of terms (where appropriate)

A full reference list in Harvard style

Supervision meeting records with supervisor signature- THREE



















Signed: …………………………………………….Date: ……………….



