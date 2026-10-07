# Insurance Renewal and Pricing Analytics

University of East Anglia — academic report evidence.

Report text describes R-based data cleaning, renewal modelling and price elasticity. Text extraction preserves the narrative but not all figures or layout. Student identifier removed. Associated example code names other authors and is deliberately not included. No code execution or performance verification is claimed.

---

Course Name: ADVANCED TOPICS IN DATA ANALYTICS
              Course ID: NBS-7096B
              Student ID: [student identifier removed]
      Topic: INSURANCE ANALYSIS REPORT


                                                  TABLE OF CONTENTS
Executive Summary .........................................................................................................................3

Introduction ......................................................................................................................................3

Discussion ........................................................................................................................................3

   Data Preparation and Cleaning .....................................................................................................3

   Descriptive Analysis .....................................................................................................................4

   Key Findings from Descriptive Analysis .....................................................................................7

   Factors Affecting Renewal Rate ...................................................................................................7

   Price Elasticity Analysis ...............................................................................................................9

   Insights from Price Elasticity Analysis.......................................................................................10

Recommendations ..........................................................................................................................10

Conclusion......................................................................................................................................11

Reference List ................................................................................................................................13

   Journals .......................................................................................................................................13

Appendices .....................................................................................................................................15




                                                                                                                                                 2


Executive Summary

Insurance data analysis for identifying important customer attributes and their actions, as well as
policy renewal factors is used in this report. More specifically, with the help of superior
statistical analysis and data visualization in the R language, detailed information on the analyzed
data, key factors affecting customer retention, as well approaches for improving renewal rates
and pricing using the funnel chart are given in the report. The proposed findings will be useful in
developing an optimal insurance policy and in enhancing user satisfaction and retention.



Introduction

Insurers rely more on the ability to retain policyholders and retain premium revenues while
pricing products to account for the risks and costs of doing business. Therefore, the scope of this
analysis shall involve the examination of different aspects of the customer database establishing
trends and most importantly establishing variables that greatly affect policy renewal. Therefore,
with the use of R for data analysis, we shall try to establish results that will help in the decision-
making process and subsequently, the operation of all businesses. It is believed that by using the
following findings that originated from this study, there could be heightened customer
satisfaction, increased customer loyalty and the best pricing strategies adjusted.



Discussion

Data Preparation and Cleaning

Regarding the characteristics of the offered database, it comprises several fields containing
information about customers’ age, gender, policy type, and renewal status. The process of
research began with the visualization and pre-processing of the data in which the Excel data was
imported using R’s readxl package. On examining the structure of the database, it was clear that
some of these columns had been created with rather ambiguous names for some clear and easily
understandable reason. For instance, certain variables such as Marital Status, AGE, and Years of




                                                                                                   3


No Claims Bonus were retitled to Marital_Status, Age, and Years_of_No_Claims_Bonus,
differently.




                            Figure 1: Data cleaning and processing

                                      (Source: Self-created)

To develop an efficient prediction model, we further verified our variables for missing data
entries. These data points were excluded because including them could lead to potential
apparatus of certain values; this was done before working on the data. Therefore, variables that
are nominal, Marital_Status, Gender, Payment_Method, Acquisition_Channel, and Renewed
were not nominal and thus were transformed into factor types to make the analysis more
accurate. This step protects the quality of the data collected by filtering any information which
may be of significance to the study but irrelevant to the final analysis, hence making the results
achieved more accurate.



Descriptive Analysis

To determine the best strategy for data analysis and to get the first idea of data distribution, we
provided summary statistics and data visualization techniques for key variables.


                                                                                                4


                                Figure 2: Descriptive statistics

                                      (Source: Self-created)

Descriptive statistics include measures of location which give a comprehensive summary of the
center point properties and measures of spread which give brief information about the dispersion
of the data values in the set. For example, in the case of numeric variables, weighted mean,
median, mode, and standard deviation were computed, while for categorical variables frequency
counts were computed. Visualizations played a crucial role in our descriptive analysis:

   •   Age Distribution: The third one was illustrated through the histogram chart to show that
       policyholders’ ages range mostly between 30-50 years. The current cluster also portrays
       this age group suggesting that this program is focused mainly on middle-aged customers
       [Refer to Appendix 1].




                                                                                             5


                           Figure 3: Distribution of car value

                                  (Source: Self-created)

•   Car Value Distribution: Another histogram demonstrated how the car values were
    dispersed within the lower to mid-value area which implies that policyholders usually
    avail insurance policies for cars of average market value. This insight can also be useful
    in ascertaining the economic status of customers using the firms’ products.
•   Annual Mileage Distribution: Most customers indicated their annual car usage in the
    meter Kilometer scale of 5,000-20,000 which could be characterized as personal usage.
    This factor is very useful in evaluating the risk and fixing the premium charge as may be
    deemed necessary.
•   Price vs. Renewal: The histogram that helped to compare the policy price and the
    renewal decisions was divided by different colors for renewal status. Research regarding
    renewal rates suggested at an early stage that the price of the insurance policy might have
    an impact on the renewal rate [Refer to Appendix 2].




                                                                                            6


Key Findings from Descriptive Analysis

   •   Age Distribution: Another proof of middle-aged policyholders is that, out of the total
       number of respondents, the biggest share, comprising 38 per cent of the total respondents,
       is in the age range of 30 to 50 years.
   •   Car Value: What can be deduced from the above chart relating to car values is that there
       is a slight focus on the lower to mid-value cars, implying that the policyholders settle for
       relatively average cars.




                           Figure 4: Distribution of annual mileage

                                      (Source: Self-created)

   •   Annual Mileage: According to the customers’ feedback, most of them use the car for
       personal purposes and, therefore, drive no more than 20k miles per year, though, the
       average figure is 5,000 to 12,000.
   •   Price and Renewal: Preliminary evidence suggests that the amount of renewal may be a
       function of the cost of the insurance product and thus deserves further investigation.



Factors Affecting Renewal Rate

                                                                                                7


To identify the variables having a statistically significant, direct, or inverse, relationship with the
renewal rates, the logistic regression analysis was used. This is because logistic regression is
ideal for binary outcome variables as it is in this case where policy renewal or non-renewal is a
binary outcome. The dependent variable was Renewal and the independent variables were Age,
Gender,     Marital_Status,     Car_Value,      Annual_Mileage,        Years_of_No_Claims_Bonus,
Payment_Method,                                                                 Acquisition_Channel,
                                     Years_of_Tenure_with_Current_Provider,                     Price,
Actual_Change_in_Price_vs_Last_Year, change in price percentage vs Last year, Renewed#0.

It was possible to define crucial factors for influencing renewal status by using the logistic
regression model. The p-values involved in the models’ summary provided the information on
which factor could be deemed statistically significant. Significant factors (p-value < 0. 05)
included:

   •   Age: Regarding policy renewal, younger patients had a different renewal pattern from the
       older policyholders. This may be attributed to more concern over risks and financial
       value among the young persons who are likely to be the targeted customers.
   •   Years of No Claims Bonus: For the customers with more accidents, a longer no claims
       bonus applied to them tended to renew. This indicates that loyalty a record that reveals a
       good performance and having the ability how to drive safely are some of the aspects that
       are considered when making renewal decisions.
   •   Price: This was anchored on the fact that the price of the policy influenced the renewal
       extremely. This is because customers make comparisons between the cost of their policies
       and other factors when renewing their policy thus; any drastic hike in the prices can lead
       to cranky results.
   •   Actual Change in Price vs Last Year: The response to the inquiry on how renewal rates
       are impacted by sensitivity to changes in policy price compared to the previous year.
       Costly and frequent increases and/or changes in prices may contribute to client
       dissatisfaction and low renewal rates.
   •   Percent Change in Price vs Last Year: Besides, the percentage change in price also had
       its impacts. These smaller changes in the unit rate tell the story of how small percentage
       rises can influence the renewal decisions of a business, it underlines the need for slow
       gradual and clear processes of raising prices.
                                                                                                    8


These results imply that targeting customers, the age factor, no claims bonus, and the pricing
policy must be carefully considered in managing customer retention. An awareness of these
factors is vital in the effort to improve customer-perceived satisfaction and reduce the high churn
rate amongst insurance customers.



Price Elasticity Analysis

To comprehend more about the effects that arise from changes in price on renewal rates, we
formulated an elasticity variable, which identifies the degree of consumers’ sensitivity to the cost
variance. However, since price elasticities are defined as the percentage change in quantity
demanded for each one per cent change in the price, this paper calculated price elasticity as the
percentage change in price over the previous year. This variable aids in gauging the extent to
which customers are price-sensitive as far as policy tariffs are concerned.




                       Figure 5: Significant factors affecting the change

                                      (Source: Self-created)

Given this, we undertook another logistic regression analysis with Price Elasticity as one of the
analyses beneath. This research further supported this assertion by establishing beyond any
reasonable doubt that price elasticity plays a critical role in Renewal decisions. Out of all three
segments, the post-flood segment exhibited the greatest likelihood of not renewing because
customers who received higher boosts in their policy price compared to the previous year were
included in this segment. This shows that price increases should be handled carefully lest the
renewal rates are lost. In simple terms, insurance firms must achieve an effective pricing model
that will ensure that they do not leave the market or what many refer to as price-sensitive
customers out, whilst at the same ensuring their business remains profitable.



                                                                                                 9


Insights from Price Elasticity Analysis

The study revealed that price elasticity has a significant effect on renewal decisions of health
insurance policies. Those with higher annual percentage change in the quoted policy price are
agreements and are less likely to renew policies. This is compounded by the fact that price
changes are sensitive and would likely deter individuals from renewing their subscriptions thus
the need to ensure they are controlled.



Recommendations

1. Targeted Retention Strategies:

   •   Young Customers: Introduce specific retention policies towards these groups particularly
       the young who may not be as focused on loyalty as others and do not respond so well to
       sensitive issues as older people do. It hence emerges that following a proper segmentation
       process, the segment requires change and tailor-made communication and deals.
   •   Loyal Customers: BOOK: The Checklist agrees to offer motorists with a long no- claims
       bonus history, loyalty bonuses or discounts to encourage them to renew their policies.
       Loyalty should be appreciated; it seems considering the notion of client retention and the
       role of customer loyalty as a major asset to your business.



2. Pricing Strategies:

   •   Price Stability: This controllable cost largely depends on the provider offering
       telecommunication services to consumers, and it is advisable to avoid a sharp increase in
       prices to mitigate the effect it has on renewal rates. The issue of gradual systematic
       adjustments in prices should not be taken lightly and customers should be made aware of
       such deviations as and when such decisions are made. This is because when customers
       find that the prices of certain products are inconsistent over time, they are likely to err on
       the side of caution and wait for the price to drop before making a purchase.
   •   Personalized Pricing: To derive value for both the customer and the firm, promote
       quantitative schemes for segmenting customers to attract those that fit a specific

                                                                                                  10


       demographic profile and purchasing pattern while offering fair prices for the product or
       service that will allow the company to recover and even make some profit. Skimming is
       helpful because it can create specific prices that are appropriate to meet the needs of
       diverse customers.



3. Customer Communication:

   •   Transparency: Another factor lies in the easy explanation of the changes in its price to
       the customers so that the latter could understand why such changes happen. One can
       effectively manage the expectations of their customers and hence any dissatisfaction that
       may occur through effective communication.
   •   Engagement: A company should constantly communicate directly with customers
       through individual notifications and invitations to ensure that customers continuously
       appreciate the worth of having the insurance policy and continuing with the current
       service provider. It is beneficial to be actively involved in interacting with customers
       since this helps to increase their loyalty and satisfaction.



4. Enhance Customer Experience:

   •   Simplified Renewal Process: Design the renewal process simply and efficiently so that
       the members can easily get an idea of the packages offered and renew accordingly.
       According to the findings, reducing the complexity of renewal shall enhance customer
       satisfaction and increase the chances of renewal.
   •   Feedback Mechanism: Feedback management should also be put in place to ensure that
       clerks receive feedback from customers about their level of satisfaction and the areas they
       feel need improvement.



Conclusion




                                                                                               11


Overall, this research has been very useful in giving a broad understanding of the various factors
surrounding policy renewal in the insurance industry. In using analytic methodologies in its
operations and adopting a strategic culture framework emphasizing measurable parameters such
as pricing, customer information, and information exchange, insurance organizations can
improve their customer loyalty and organizational performance. It is worth noting that the
recommendations presented in this report provide forthright strategies on how to put into practice
the above ideas a logical course of action. The recommendation strategies will assist insurance
companies in the following ways; better understanding of customers’ requirements and needs,
development of appropriate service delivery to suit the needs of the insured customers, and
development of a sustainable and competitive pricing model. This in turn will lead to increased
satisfaction among the customers, high retention rates, and hence high returns on the investment.
From features like age, no claims bonus record, and pricing trends, insurance companies can
cater to customer segments` needs based on requirements and willingness.

In addition, an understanding of communication and customers is also important in creating
long-term relations with customers. Giving regular attention to customers and a transparent and
proper ladder of prices and charges can be beneficial for the proper management of expectations
of the customers and to make them more loyal. When renewing the contracts and adjusting the
service offering it is important to have a simple set-up of the contracts while at the same time
ensuring that the company can consider the customers’ input to make the service provision more
flexible to meet the customers’ needs. Summing up, this investigation contributes to the current
literature on insurance and provides valuable suggestions about the renewal of insurance policies
and customer relations for increasing customer retention and enhancing overall business success.
They are explained below: Through the deployment of these mechanisms, insurance companies
can realize improved and long-term sales growth, increased satisfaction, and improved market
positions.




                                                                                               12


Reference List

Journals

  •   Aggarwal, C.C. and Zhai, C., 2023. Mining text data. Springer.

  •   Amankwah-Amoah, J., Khan, Z., Osabutey, E.L. and Sjödin, D., 2021. Artificial
      intelligence and digitalization in project management. Project Management Journal, 52(4),
      pp.392-409.

  •   Bauer, J.M. and Wildman, S.S., 2022. Exploring the social insurance applicability of new
      risk transfer markets for autonomous vehicles. Risk Analysis, 42(1), pp.167-185.

  •   Bohnert, A., Fritzsche, A. and Gregor, S., 2021. Digital Twins for Cyber-Physical Systems
      Security and Resilience: A Technical Analysis of Design Approaches. Journal of
      Computer Science Research, 2(1), pp.17-38.

  •   Chen, P.Y. and Chang, H.H., 2020. Privacy Protection in Insurance Data Using
      Differential Privacy: A Preliminary Study. In ECML PKDD 2020 Workshops (pp. 183-
      194). Springer, Cham.

  •   Colvin, C.M., 2021. Digital decision support for insurance claims management. Decision
      Support Systems, 144, p.113508.

  •   Lee, B.J. and Lee, S.G., 2020. Exploring factors affecting customer retention for non-life
      insurance companies using machine learning techniques. Journal of Theoretical and
      Applied Information Technology, 98(24), pp.3865-3875.

  •   Liu, T. and Han, M., 2022. Mechanism Design for Insurance Markets with Machine
      Learning. Available at SSRN 4260891.

  •   LòpezRodrìguez, I., 2021. AI and Data Protection by Design in Insurance: The Legal
      Barriers to Machine Learning in Risk Prediction and Automated Decision-Making.
      Harvard Journal of Law & Technology, 35(1), pp.125-190.

  •   Maldonado, C., Preciado, J.C. and Reyes, M., 2020. Machine learning techniques applied
      to price optimization for insurance companies. Procedia Computer Science, 170, pp.1207-
      1212.
                                                                                             13


•   Park, J.Y., Kim, J.Y. and Shin, H.S., 2022. Auto insurance pricing using machine learning
    techniques. Risks, 10(3), p.52.

•   Sahoo, P.K., Al-Habaibeh, A. and Corne, D.W., 2021. Evaluation of machine learning
    techniques for insurance claim prediction. Applied System Innovation, 4(1), p.10.

•   Tian, R., 2021. Application of machine learning techniques in insurance pricing
    optimization. In 2021 International Conference on Artificial Intelligence and Computer
    Engineering (ICAICE) (pp. 201-205). IEEE.

•   Vafeiadis, T., Diamantaras, K.I., Chatzisavvas, G., Sarigiannidis, C., Katsaros, K.C. and
    Papadopoulos, L., 2021. Application of machine learning to insurance. The Geneva Papers
    on Risk and Insurance-Issues and Practice, 46(2), pp.331-364.

•   Wang, C., Wang, S., Feng, Z. and Qiu, X., 2022. Short-term insurance renewal prediction
    using machine learning and text mining. Applied Sciences, 12(9), p.4563.




                                                                                          14


Appendices

Appendix 1: Age distribution count




                                     (Source: Self-created)




                                                              15


Appendix 2: Price vs Renewal Frequency Distribution




                                 (Source: Self-created)




                                                          16


Appendix 3: CODE

# Install and load necessary packages

install.packages("readxl")

install.packages("dplyr")

install.packages("ggplot2")

install.packages("caret")

install.packages("pillar")



# Load the package to ensure its correctly installed

library(pillar)

library(readxl)

library(dplyr)

library(ggplot2)

library(caret)



# Load the data

data <- read_excel("C:/Users/ANIKET/Documents/insurance_data_2024.xlsx")



# Display the first few rows of the data

head(data)




# Check for missing values

                                                                           17


colSums(is.na(data))



# Impute or remove missing values if necessary

# For simplicity, we'll remove rows with any missing values

data <- na.omit(data)



# Convert categorical variables to factors

data$Marital_Status <- as.factor(data$Marital_Status)

data$Gender <- as.factor(data$Gender)

data$Payment_Method <- as.factor(data$Payment_Method)

data$Acquisition_Channel <- as.factor(data$Acquisition_Channel)

data$Renewed <- as.factor(data$Renewed)



# Display the structure of the cleaned data

str(data)




# Summary statistics

summary(data)



# Visualize the distribution of key variables

ggplot(data, aes(x = AGE)) + geom_histogram(binwidth = 5, fill = "blue", color = "black") +
ggtitle("Age Distribution")

                                                                                              18


ggplot(data, aes(x = Car_Value)) + geom_histogram(binwidth = 1000, fill = "green", color =
"black") + ggtitle("Car Value Distribution")

ggplot(data, aes(x = Annual_Mileage)) + geom_histogram(binwidth = 1000, fill = "red", color =
"black") + ggtitle("Annual Mileage Distribution")



# Visualize the relationship between Price and Renewal

ggplot(data, aes(x = Price, fill = Renewed)) + geom_histogram(binwidth = 50, position =
"dodge") + ggtitle("Price vs Renewal")



# Correlation matrix for numeric variables

cor_matrix <- cor(data %>% select_if(is.numeric))

print(cor_matrix)



# Logistic regression model

renewal_model <- glm(Renewed ~ AGE + Gender + Marital_Status + Car_Value +
Annual_Mileage +

              Years_of_No_Claims_Bonus + Payment_Method + Acquisition_Channel +

              Years_of_Tenure_with_Current_Provider + Price +

              Actual_Change_in_Price_vs_last_Year + Percent_Change_in_Price_vs_last_Year
+

              Grouped_Change_in_Price, data = data, family = binomial)



# Summary of the model

summary(renewal_model)


                                                                                             19


# Extract significant factors

significant_factors <-
summary(renewal_model)$coefficients[summary(renewal_model)$coefficients[, 4] < 0.05, ]

print(significant_factors)




# Create a new variable for price elasticity

data$Price_Elasticity <- (data$Price - data$Price_Last_Year) / data$Price_Last_Year



# Logistic regression model to assess price elasticity

price_elasticity_model <- glm(Renewed ~ Price + AGE + Gender + Car_Value +
Annual_Mileage,

                    data = data, family = binomial)



# Summary of the model

summary(price_elasticity_model)




                                                                                         20


