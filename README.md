# Summary of the project

**Overall Sentiment Distribution Text Based Sentiment Distribution** The majority of reviews (approximately 140,000) are classified as Positive based on text analysis using VADER. Negative reviews number around 20,000, while Neutral reviews account for about 25,000. This indicates a strong positive bias in the text content of the reviews, suggesting that customers tend to express favorable opinions in their written feedback.

**Rating Based Sentiment Distribution** Similarly, the sentiment derived from star ratings (mapped as 4-5 stars = Positive, 3 stars = Neutral, 1-2 stars = Negative) shows a dominant Positive category (around 140,000 reviews), with Neutral (approximately 20,000) and Negative (around 30,000) categories significantly lower. This alignment suggests that higher star ratings (4-5) are prevalent, consistent with the text-based findings.

**Text-Based Sentiment by Star Rating The distribution of text-based sentiment across star ratings reveals interesting patterns:**

1-Star Ratings: Predominantly Negative (around 15,000), with minor Positive (a few thousand) and Neutral (a few thousand) classifications. This suggests that 1-star reviews align well with negative text sentiment, though some may contain sarcasm or mixed feedback misclassified as Positive or Neutral.

2-Star Ratings: Mostly Negative (around 10,000), with small Positive and Neutral counts, indicating a similar trend of negative sentiment in lower ratings.

3-Star Ratings: A balanced mix, with Positive (around 15,000), Negative (around 5,000), and Neutral (around 5,000) sentiments. This reflects the neutral nature of 3-star ratings, where text sentiment varies widely.

4-Star Ratings: Dominated by Positive sentiment (around 40,000), with minor Negative and Neutral contributions, showing a strong correlation between 4-star ratings and positive text.

5-Star Ratings: Overwhelmingly Positive (around 80,000), with negligible Negative and Neutral counts, reinforcing that 5-star reviews are highly likely to contain positive text.

Observation: There’s a notable discrepancy where lower ratings (1-2 stars) occasionally yield Positive or Neutral text sentiment, possibly due to sarcasm, ambiguous language, or VADER’s limitations with Hinglish/slang. Higher ratings (4-5 stars) show strong alignment with Positive text sentiment.

**Text-Based Sentiment by Top 10 Products**

The analysis of the top 10 products by review count shows a consistent trend of Positive sentiment dominating across all products:

Products like "MILTON Thermosteel Flip Lid 500 ml Flask (Pack of 1 Silver Steel)" and "Cello Pack of 18 Opalware Cello Dazzle Lush Fiesta Opalware Dinner Set 18 Pieces Dinner Set, White Microwave Safe" have the highest review counts (over 7,000 and 6,000 respectively), with the vast majority classified as Positive.

Other products, such as "Kadio Analog 20 cm x 20 cm Wall Clock Beige with Glass Standard" and "Mi 31 10000 mAh Power Bank Fast Charging 18W Blue Lithium Polymer," also lean heavily toward Positive sentiment (around 3,000-4,000 reviews each).

Negative and Neutral sentiments are present but minimal across all products, with counts typically below 1,000 per product.

Observation: The strong Positive bias across top products suggests either high customer satisfaction with these items or a potential presence of biased reviews (e.g., promotional or fake reviews). Neutral sentiment appears more in products with moderate review counts, possibly indicating mixed but not strongly negative feedback.

**Implications and Insights**

Positive Bias: The overwhelming Positive sentiment in both text and ratings indicates that the dataset may be skewed toward satisfied customers or that Flipkart’s review system encourages positive feedback. This could also reflect a selection bias where only satisfied customers leave detailed reviews.

Neutral Review Significance: The relatively low Neutral count (both text- and rating-based) suggests that customers either tend to express strong opinions (Positive or Negative) or that neutral experiences are underrepresented. The neutral word cloud (not shown but implied) could reveal terms like “okay,” “average,” or “decent,” highlighting products that meet basic expectations without exciting customers.

Discrepancy Analysis: The mismatch between low ratings (1-2 stars) and occasional Positive/Neutral text sentiment warrants further investigation. It might indicate sarcasm, cultural nuances (e.g., Hinglish), or limitations in VADER’s ability to capture context, suggesting a need for advanced models like BERT or manual review of such cases.

Product-Specific Trends: Top products with high Positive sentiment are likely popular or well-received items, but the low Negative/Neutral counts might mask underlying issues (e.g., delivery delays) that don’t significantly impact ratings.

**Recommendations**

Refine Neutral Analysis: Generate and analyze the neutral word cloud to identify specific terms or themes (e.g., “delivery,” “price”) that might indicate subtle dissatisfaction or mediocrity, which could guide product improvements.

Address Discrepancies: For 1-2 star reviews with Positive/Neutral text, consider sampling these reviews for manual analysis or applying a more context-aware model (e.g., BERT) to better capture sarcasm or mixed sentiments.

Explore Bias: Investigate the dataset for potential review bias (e.g., fake reviews or selective posting) given the strong Positive skew, possibly by cross-referencing with external data or analyzing review timestamps. Product Focus: Target products with moderate Neutral sentiment for enhancement, as they might represent untapped potential to shift customers to Positive feedback.

The RNN model performs good with an overall accuracy of 0.90, particularly excelling with Positive reviews due to the dataset’s imbalance. However, its weakness with Neutral reviews (F1-score 0.28) suggests room for improvement, likely requiring techniques to address class imbalance and enhance model sensitivity to neutral text.

This model can be improved by increasing the robustness i.e increasin the number of epochs, using a pre-trained model like BERT, which might better handle neutral sentiment due to its contextual understanding.

**The sentiment analysis of the Flipkart product review dataset was conducted using two methods: text-based sentiment analysis with VADER and rating-based sentiment analysis with star ratings, supplemented by an RNN-based approach for deeper evaluation. Both VADER and rating-based methods offer quick, interpretable insights with a positive skew, while the RNN enhances accuracy for dominant classes but needs refinement to handle neutral sentiment effectively. Combining these methods provides a comprehensive view, with the RNN offering potential for future improvement pending imbalance correction.**
