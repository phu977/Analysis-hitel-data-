# Analysis-hotel-data-
<p>
In this study, the author would like to present how to handle datasets with many variables to be classified. This is a small study to understand more about machine learning and how to set up input data for it.</p>
<p>Our dataset includes the following features:</p>
<li>Booking_ID: unique identifier of each booking</li>
<li>no_of_adults: Number of adults</li>
<li>no_of_children: Number of Children</li>
<li>no_of_weekend_nights: Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel</li>
<li>no_of_week_nights: Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel</li>
<li>type_of_meal_plan: Type of meal plan booked by the customer:</li>
<li>required_car_parking_space: Does the customer require a car parking space? (0 - No, 1- Yes)</li>
<li>room_type_reserved: Type of room reserved by the customer. The values are ciphered (encoded) by INN Hotels.</li>
<li>lead_time: Number of days between the date of booking and the arrival date</li>
<li>arrival_year: Year of arrival date</li>
<li>arrival_month: Month of arrival date</li>
<li>arrival_date: Date of the month</li>
<li>market_segment_type: Market segment designation.</li>
<li>repeated_guest: Is the customer a repeated guest? (0 - No, 1- Yes)</li>
<li>no_of_previous_cancellations: Number of previous bookings that were canceled by the customer prior to the current booking</li>
<li>no_of_previous_bookings_not_canceled: Number of previous bookings not canceled by the customer prior to the current booking</li>
<li>avg_price_per_room: Average price per day of the reservation; prices of the rooms are dynamic. (in euros)</li>
<li>no_of_special_requests: Total number of special requests made by the customer (e.g. high floor, view from the room, etc)</li>
<li>booking_status: Flag indicating if the booking was canceled or not.</li>
<p>In this data analysis, the author will use a function available in the pandas library of the Python language, which is pandas.get_dummies() and Label Encoding.</p> 
<p> pandas.get_dummies() is used for data manipulation. It converts categorical data into dummy or indicator variables.</p>
<p> Label Encoding refers to converting the labels into a numeric form so as to convert them into the machine-readable form. Machine learning algorithms can then decide in a better way how those labels must be operated. It is an important pre-processing step for the structured dataset in supervised learning</p>
<p>In conlusion,Although the above small analysis is quite simple according to the author, from this article we have learned more about some ways to process data with categorical features so that we can improve the level of data processing. data and an accurate view of all future data to come</p>
