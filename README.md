# Data-Science-Supervised-Learning-Classification-Project-INN-Hotels

**Context**

A significant number of hotel bookings are called-off due to cancellations or no-shows. The typical reasons for cancellations include change of plans, scheduling conflicts, etc. This is often made easier by the option to do so free of charge or preferably at a low cost which is beneficial to hotel guests but it is a less desirable and possibly revenue-diminishing factor for hotels to deal with. Such losses are particularly high on last-minute cancellations.

The new technologies involving online booking channels have dramatically changed customers’ booking possibilities and behavior. This adds a further dimension to the challenge of how hotels handle cancellations, which are no longer limited to traditional booking and guest characteristics.

The cancellation of bookings impact a hotel on various fronts:

Loss of resources (revenue) when the hotel cannot resell the room.
Additional costs of distribution channels by increasing commissions or paying for publicity to help sell these rooms.
Lowering prices last minute, so the hotel can resell a room, resulting in reducing the profit margin.
Human resources to make arrangements for the guests.

**Objective**

The increasing number of cancellations calls for a Machine Learning based solution that can help in predicting which booking is likely to be canceled. INN Hotels Group has a chain of hotels in Portugal, they are facing problems with the high number of booking cancellations and have reached out to your firm for data-driven solutions. You as a data scientist have to analyze the data provided to find which factors have a high influence on booking cancellations, build a predictive model that can predict which booking is going to be canceled in advance, and help in formulating profitable policies for cancellations and refunds.

**Data Description**

The data contains the different attributes of customers' booking details. The detailed data dictionary is given below.

**Data Dictionary**

Booking_ID: unique identifier of each booking
no_of_adults: Number of adults
no_of_children: Number of Children
no_of_weekend_nights: Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
no_of_week_nights: Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel
type_of_meal_plan: Type of meal plan booked by the customer:
Not Selected – No meal plan selected
Meal Plan 1 – Breakfast
Meal Plan 2 – Half board (breakfast and one other meal)
Meal Plan 3 – Full board (breakfast, lunch, and dinner)
required_car_parking_space: Does the customer require a car parking space? (0 - No, 1- Yes)
room_type_reserved: Type of room reserved by the customer. The values are ciphered (encoded) by INN Hotels.
lead_time: Number of days between the date of booking and the arrival date
arrival_year: Year of arrival date
arrival_month: Month of arrival date
arrival_date: Date of the month
market_segment_type: Market segment designation.
repeated_guest: Is the customer a repeated guest? (0 - No, 1- Yes)
no_of_previous_cancellations: Number of previous bookings that were canceled by the customer prior to the current booking
no_of_previous_bookings_not_canceled: Number of previous bookings not canceled by the customer prior to the current booking
avg_price_per_room: Average price per day of the reservation; prices of the rooms are dynamic. (in euros)
no_of_special_requests: Total number of special requests made by the customer (e.g. high floor, view from the room, etc)
booking_status: Flag indicating if the booking was canceled or not.

**Actionable Insights and Recommendations**

The model built using Logistic regression with the threshold of 0.37 can be used to predict if the INN Hotels booking is going to get canceled or not and can correctly identify 73% of the booking cancelations and gives a F1 score of 0.70.

The model built using Decision tree with Post-Pruning can be used to predict if the INN Hotels booking is going to get canceled or not and can correctly identify 85% of the booking cancelations and gives a F1 score of 0.80.

The Decision tree algorithm gives better results than the Logistic regression.

Lead time, market segment type Online, average price per room and number of special requests are some of the important features that can predict booking cancelations of the INN Hotels.

From the decision tree, it has been observed that If the lead_time is <=151.0, no.of.special requests is <=0.5, market_segment_type_online is <= 0.5, lead time is <=90.0, no.of weekend nights is <= 0.5, average price per room is <=196.5, market_segment_type_offline is <=0.5,lead_time is <=16.5, average price per room is >68.5,arrival_date is <=29.5, no_of_adults is <=1.5 then the booking is likely to be canceled.

The INN Hotels should give more importance to the above mentioned features and the corresponding values in order to predict booking cancelations.

The INN Hotels should fetch more data for the analysis in order to get more precise and reliable results.
The INN Hotels should have a boundary on the lead time while the customer makes the reservation as higher the lead time more likely the customer cancels the booking. Hence the INN Hotels can set the bound on the lead time of less than an year.

The INN Hotels gets more bookings during the month of October, September and August but the number of bookings getting canceled are also high during these months. Hence the INN Hotels must have a vigilant eye during these months on the factors that might impact the cancelations and can provide dicsountable rates on the room price and assign more resources and funds towards their marketing campaign during this peak season in order to attract customers so as to reduce the number of cancelations and also be competitive on the market.

During the initial months of the year January and February the number of bookings is very less. The INN Hotels can attract more customers during this time by reducing the price of the room compared to other hotels and also giving reward points for the customers booking during this time so that the INN Hotels will get repeated customers.
