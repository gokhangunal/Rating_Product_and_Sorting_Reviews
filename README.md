# Rating Product & Sorting Reviews in Amazon

## Business Problem

One of the most significant challenges in e-commerce is accurately calculating the scores given to products after sales. Solving this problem means more customer satisfaction for the e-commerce site, prominence for the products for the sellers, and a seamless shopping experience for the buyers. Another issue is correctly sorting the reviews given to products. Misleading reviews coming to the forefront will directly affect the product's sales, leading to financial losses and customer loss. Solving these two fundamental problems will increase sales for the e-commerce site and sellers while customers complete their purchasing journey smoothly.

## Data Set Story

This dataset contains Amazon product data, including various product categories and metadata. It has user ratings and reviews for the most reviewed product in the electronics category.

### Variables

- reviewerID
- asin
- reviewerName
- helpful
- reviewText
- overall
- summary
- unixReviewTime
- reviewTime
- day_diff
- helpful_yes
- total_vote

### Data

- 4915 Observations
- 71.9 MB

Includes user ID, product ID, user name, helpful review rating, evaluation, product rating, evaluation summary, evaluation time (UNIX and raw), days since review, number of times the review was found helpful, and the number of votes given to the review.

## Project Tasks

### Task 1: Calculate the Average Rating based on recent reviews and compare it with the existing average rating.

#### Step 1:
Calculate the product's average rating.

#### Step 2:
Calculate the weighted average rating based on the date.

#### Step 3:
Compare and interpret the average of each time period in the weighted rating.

### Task 2: Determine 20 reviews to be displayed on the product detail page.

#### Step 1: Generate the helpful_no variable.

- total_vote is the total number of up-down votes a review receives.
- up means helpful.
- There is no helpful_no variable in the dataset; it needs to be generated from existing variables.
- Subtract the number of helpful votes (helpful_yes) from the total vote count (total_vote) to find the number of unhelpful votes (helpful_no).

#### Step 2: Calculate and add the scores for score_pos_neg_diff, score_average_rating, and wilson_lower_bound to the data.

- Define functions for score_pos_neg_diff, score_average_rating, and wilson_lower_bound to calculate these scores.
- Create scores according to score_pos_neg_diff, then save them in the dataframe as score_pos_neg_diff.
- Create scores according to score_average_rating, then save them in the dataframe as score_average_rating.
- Create scores according to wilson_lower_bound, then save them in the dataframe as wilson_lower_bound.

#### Step 3: Determine the top 20 reviews and interpret the results.

- Sort and identify the top 20 reviews according to wilson_lower_bound.
- Interpret the results.
