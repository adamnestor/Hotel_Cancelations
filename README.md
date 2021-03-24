# Reducing Hotel Revenue Loss by Identifying Drivers to Cancelations

### Overview
  * For a hotel, the goal is for bookings to turn into actual stays instead of cancelations.
  * Stays are a main source of income for hotels; and they open the door to additional income streams (food, drink, etc)
  * While cancelations aren't ideal, the positive spin is that the hotel had the potential guests attention for some period of time. 
  * **Therefore, our purpose is to use booking data to determine any behavior patterns within bookings that are eventually cancelations**

### Tools and Resources Used  
  **Dataset** https://www.kaggle.com/jessemostipak/hotel-booking-demand   
  **Analytics Tool** Python, matplotlib, pandas, numpy  
  **Analytic Methodologies** Descriptive and Inferential Statistics  
  **Data Visualization** Tableau  

### YouTube Project Walk-Through

### Tableau Presentation
https://public.tableau.com/shared/7KNGBC339?:display_count=y&:origin=viz_share_link

### Data Cleaning
  * Dataset has 119390 rows of data, each representing an individual booking.
  * Lead time column, which is the amount of time from the booking until the scheduled date of arrival, sparked curiousity about cancelation notice, which is the amount of time before a scheduled date of arrival that a booking is canceled. Therefore, this column was created.
  * After initial exploration of the data by using our Issue Tree, it was found that there were some bookings that were may more common than others. These eventually lead to the creation of 3 subsets...
      1. Noncancelations - Bookings that resulted in a Stay
      2. "Filtered Subset" - Bookings that were Cancelations, City Hotels, Travel Agent, Room Type A - This were 20% of all bookings.
      3. Other Cancelations - Bookings that were Cancelations but in other categories than the above.
  * Eventually, a column was created with sorted bookings into their respective fiscal year, instead of the calendar year.

### EDA
  * I compared the variablity of boxplots between the 3 subsets for any noticable differences that could drive a cancelation.
  * I used correlation to identify possible relationships between cancelation and other variables.
  * After identifying 5-6 potential drivers, I used descriptive statistics such as mean and median to compare between the 3 subsets.

### Key Insights
1. **The Timing of the Booking** - It was found that Bookings within the Filtered Subset occured with more lead time than Other Cancelations and Noncancelations. Lead time is defined as the amount of days between the booking and expected arrival date (the advance notice of the booking in days). 
 ![Lead Time Boxplots](https://user-images.githubusercontent.com/79426455/112389753-a33f0c80-8ccb-11eb-8d63-dd3a65f07bf1.png)
2. **Special Requests** - A negative correlation between Cancelations and Special Requests suggested the more special requests made the less likely the booking would be canceled. The data showed this to be particularly true within the Filtered Subset.   
 ![Special Request Boxplots](https://user-images.githubusercontent.com/79426455/112389832-bf42ae00-8ccb-11eb-9ff2-0ef15c7a902e.png)
3. **First-Time Guests** - The Filtered Subset was majority first-time guests, i.e. no previous cancelations or previous noncancelations. First-time guests represent a huge opportunity to make a first impression and establish customer loyalty.   
 ![Filtered Repeated Guest](https://user-images.githubusercontent.com/79426455/112389930-e305f400-8ccb-11eb-9081-e944d18fa599.png)
