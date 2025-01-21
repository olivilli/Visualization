## **British Airways Review Dashboard**

This Tableau dashboard provides an analysis of 1,325 British Airways customer reviews from the years 2016 to 2023.

![british_airways_dashboard](https://github.com/olivilli/Visualization/blob/main/PowerBI/Salaries/british_airways.png)

## **About the Dataset**
The dataset consists of two tables:
- ba_reviews – Contains detailed review data with fields such as: route, aircraft, traveler type and ratings across multiple categories (cabin staff service, entertainment, food, etc.)
- countries – Provides geographical data for mapping review locations.

## **Project Details**

All visualizations and calculations were created across four separate sheets and later combined into the final dashboard

- ### **Metric Selection with Parameter:**  
  A `Pick a metric` parameter was created to allow dynamic switching between different review aspects. A calculated field was used to handle the metric selection logic:

  ```sql
  CASE [Pick a metric]
    WHEN 'Overall rating' THEN [rating]
    WHEN 'Cabin staff service' THEN [cabin_staff_service]
    WHEN 'Entertainment' THEN [entertainment]
    WHEN 'Food' THEN [food_beverages]
    WHEN 'Ground service' THEN [ground_service]
    WHEN 'Seat comfort' THEN [seat_comfort]
    WHEN 'Value' THEN [value_for_money]
  END
  ```

- ### **Aircraft Grouping:**  
  To improve visualization clarity, all aircraft types with fewer than 50 reviews were grouped together.

## **Dashboard Features**

![british_airways_screen_record](

- A line chart visualizing the average overall metric over time.
- A map showing average metric by country.
- A bar chart displaying average metric by aircraft, alongside the number of reviews.

---
