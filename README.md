# Home Price Prediction

## Overview

This project aims to predict home prices using machine learning techniques. The dataset contains various features related to properties, such as the number of bedrooms, bathrooms, car spaces, property size, and location details. The goal is to build a predictive model that estimates the price of a property based on these features. The project is divided into two phases: **Data Exploration & Preprocessing** and **Model Building**.

---

## Column Details (Meta Description)

The dataset contains the following columns:

- **Suburb**: The suburb where the property is located.
- **Address**: The address of the property.
- **Rooms**: The number of rooms in the property.
- **Price**: The price of the property in Australian dollars (target variable).
- **Method**: The auction method used to sell the property:
  - S: Property sold
  - SP: Property sold prior
  - PI: Property passed in
  - PN: Sold prior not disclosed
  - SN: Sold not disclosed
  - NB: No bid
  - VB: Vendor bid
  - W: Withdrawn prior to auction
  - SA: Sold after auction
  - SS: Sold after auction price not disclosed
  - N/A: Price or highest bid not available
- **Type**: Type of the property:
  - br: Bedroom(s)
  - h: House, cottage, villa, semi, terrace
  - u: Unit, duplex
  - t: Townhouse
  - dev site: Development site
  - o res: Other residential
- **SellerG**: Real Estate Agent or Seller Group.
- **Date**: Date the property was sold.
- **Distance**: Distance from the Central Business District (CBD) in kilometers.
- **Regionname**: General region (e.g., West, North West, North, North East).
- **Propertycount**: Number of properties that exist in the suburb.
- **Bedroom2**: Scraped number of bedrooms (from a different source).
- **Bathroom**: Number of bathrooms.
- **Car**: Number of car spots.
- **Landsize**: Land size in square meters.
- **BuildingArea**: Building size in square meters.
- **YearBuilt**: Year the property was built.
- **CouncilArea**: Governing council for the area.
- **Latitude**: Latitude of the property.
- **Longitude**: Longitude of the property.

---

## Project Phases

### Phase 1: Data Exploration and Preprocessing

In this phase, the dataset is explored and cleaned:
- The dataset is loaded, and columns are examined to understand the data.
- Irrelevant columns such as **Address**, **Date**, **Postcode**, **YearBuilt**, **Latitude**, and **Longitude** are dropped.
- Null values in key columns like **Property count**, **Distance**, **Bedroom2**, **Bathroom**, and **Car** are filled with `0`, while the **Land size** and **Bidding area** columns are filled with the mean of their respective values.
- Categorical data is encoded into dummy variables to prepare for the model.

### Phase 2: Model Building

In this phase, a regression model is built:
- The target variable (**Price**) is separated from the features data.
- A **Linear Regression** model is trained to predict property prices based on the features.
- Model performance is evaluated to check for overfitting or underfitting.
- If the model shows signs of overfitting, **Ridge** and **Lasso Regression** techniques are applied to improve model accuracy.
- Various evaluation metrics like **Mean Squared Error**, **Mean Absolute Error**, **Root Mean Squared Error**, and **R2 Score** are calculated to assess the model’s prediction accuracy.

