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

<h> UPDATE</h>
<p>Random is random, Forest is forest, so in Random Forest algorithm I will build many decision trees using Decision Tree algorithm, but each decision tree will be different (with random factor). The prediction results are then aggregated from the decision trees.</p>
<h>Decision Tree Algorithm</h>
<p>Decision Tree algorithm belongs to the family of supervised learning algorithms. Unlike other supervised learning algorithms, the decision tree algorithm can be used for solving regression and classification problems too.

The goal of using a Decision Tree is to create a training model that can use to predict the class or value of the target variable by learning simple decision rules inferred from prior data(training data).

In Decision Trees, for predicting a class label for a record we start from the root of the tree. We compare the values of the root attribute with the record’s attribute. On the basis of comparison, we follow the branch corresponding to that value and jump to the next node</p>

<h>Important Terminology related to Decision Trees</h>
<li>Root Node: It represents the entire population or sample and this further gets divided into two or more homogeneous sets</li>
<li>Splitting: It is a process of dividing a node into two or more sub-nodes</li>
<li>Decision Node: When a sub-node splits into further sub-nodes, then it is called the decision node</li>
<li>Leaf / Terminal Node: Nodes do not split is called Leaf or Terminal node</li>
<li>Pruning: When we remove sub-nodes of a decision node, this process is called pruning. You can say the opposite process of splitting</li>
<li>Branch / Sub-Tree: A subsection of the entire tree is called branch or sub-tree</li>
<li>Parent and Child Node: A node, which is divided into sub-nodes is called a parent node of sub-nodes whereas sub-nodes are the child of a parent node.</li>


<img src='https://user-images.githubusercontent.com/65645365/227258267-4eff97ae-b6b5-451f-b417-e02a83d9d1e3.png' width='600'>

<h>Building the Random Forest algorithm</h>
<p>Suppose my dataset has n data (sample) and each data has d attributes (feature)</p>
<p>To build each decision tree I would do the following:</p>
<li>Randomly take n data from the dataset with Bootstrapping technique, also known as random sampling with replacement. That is, when I sampled 1 data, I did not remove that data but kept it in the original data set, and then continued to sample until the sample had n data. When using this technique, our new data set n may have duplicate data.</li>

<img src='https://user-images.githubusercontent.com/65645365/227260549-ad5f92ea-f594-4a30-8871-9d3967dc6727.png' width='600'>

<li>After sampling n data from step 1, I randomly select k attributes (k < n). Now I have a new dataset consisting of n data and each data has k attributes.</li>
<li>Use Decision Tree algorithm to build decision tree with data set in step 2</li>

<p>Random Forest algorithm will include many decision trees, each tree is built using Decision Tree algorithm on different data sets and using different set of attributes. Then the prediction results of the Random Forest algorithm will be aggregated from the decision trees.

When using the Random Forest algorithm, I often pay attention to attributes such as: the number of decision trees to build, the number of attributes used to build the tree. In addition, there are still properties of the Decision Tree algorithm to build a tree such as the maximum depth, the minimum number of elements in a node to be split.</p>
