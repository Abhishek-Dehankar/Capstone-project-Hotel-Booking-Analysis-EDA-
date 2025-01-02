# Hotel-Booking-Analysis
The project contains the real world data record of hotel bookings of a city and a resort hotel containing details like bookings, cancellations, guest details etc. from 2015 to 2017. In this project we are going to analyze Hotel Booking Data in order to find out valuable insights and give suggestions to increase revenue of hotels.

**Programming Language** : Python

**Libraries used** : Pandas, Numpy, Matplotlib, Seaborn

**NoteBook** : Google Colab

**Dataset Source** : Provided by Almabetter themself.

## Objective
We are provided with a hotel bookings dataset.

The main purpose of this study is to perform EDA on the given dataset and draw useful conclusions about the trends in hotel bookings and how factors that control hotel bookings influence each other.

## Dataset 
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.
```
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.
```

- Total number of rows in data: 119390
- Total number of columns: 32

## Data Cleaning and Feature Engineering

### (1) Handling null values
- Null values in columns `company` and `agent` were replaced by 0.
- Null values in column `country` were replaced by 'others'.
- Null values in column `children` were replaced by the mean of the column.

### (2) Removing Duplicate rows
All duplicate rows were dropped.

### (3) Converting columns to appropriate data types

- Changed data type of `children`, `company`, `agent` to int type.
### (4) Renaming the columns

- The `adr` column was renamed for better understanding to `average_daily_rate`

### (4) Removing outliers
- One outlier was found in the `average_daily_rate` column. Dropping them.

### (5) Creating new columns
- Creating new column `Total_stay` by adding `stays_in_weekend_nights`+`stays_in_week_nights`.
- Creating new column `Total_members` by adding `adults`+`children`+`babies`.

## Exploratory Data Analysis

Performed EDA and tried answering the following questions:
 1) Which type of hotel is mostly prefered by the guests?
2) hotel booking percentage of guests?
3) What is the most prefered room type by the customers?
4) What type of food is mostly prefered by the guests?
5) In which month most of the bookings happened?
6) which year had highest bookings?
6.1) Which country guests more come from?
7) Which distribution channel is mostly used for hotel booking?
8) percent of repeated hotel booked by guest?
9) Which hotel type has the highest ADR?
10) which hotel has longer waiting time?
11) Which distribution channel contributed more to adr in order to increase the income?
12) What is optimal stay length in both types of hotel?
13) Data in histgram format?
14) create correlation heatmap?
15) create pair plot?
 
 
Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:
   - Bar Plot.
   - Pie Chart.
   - Line Plot.
   - Heatmap.

Analysis:
Performed analysis and made following conclusions:
   1) To increase hotel business some factors are important like high revenue, generation, customers 
   satisfaction, facilities provided by hotel etc.
   2) I am able to achieve the same things by showing to client which hotel is most preferred , percentage of 
    repeated guests, mostly preferred food by guests, then which hotel has highest adr etc.
   3) Most preferred room type is achieved by countplot so the client can be well prepare in advance and this 
    insight help client for further enhancement of their hospatility.
   4) I am able to show which food type is mostly preferred so client can offer the mostly preferred food to 
    the guests.
   5) Most preferred month are shown by barplot so client can be well prepared in advanced so that minimum 
     grivances would be faced by client.
   6) Using barplot I am able to show which hotel type has high adr so client can analyse which hotel has 
     high income.
   7) I am able to show which hotel is busiest hotel sp client can do relatable changes in facilities in less 
    busy hotel type.
   8) I am able to show the relationship between repeated guests and previous bookings not cancelled so 
      client can preferred repeated guests.
   9) Using barplot relationship between adr and total number of people is shown so client can preferred 
      maximum number of people.

Conclusion
1) City Hotel seems to be more preferred among travellers and it also generates more revenue & profit.

2) Most number of bookings are made in July and August as compared rest of the months.

3) Room Type A is the most preferred room type among travellers.

4) Most of the guest stays for 1-4 days in the hotels.

5) Most guest are from Portugal and other Europian contries.

       PRT: Portugal
       
       GBR: United Kingdom
       
       FRA: France
       
       ESP: Spain
       
       DEU: Germany
       
       ITA: Italy
       
       IRL: Ireland
       
       BEL: Belgium
       
       BRA: Brazil
       
       NLD: Nrlandsethe

6) City Hotel retains more number of guests.

7) Around one-fourth of the total bookings gets cancelled. More cancellations are from City Hotel.

8) New guest tends to cancel bookings more than repeated customers.

9) Lead time, number of days in waiting list or assignation of reserved room to customer does not affect cancellation of bookings.

10) Corporate has the most percentage of repeated guests while TA/TO has the least whereas in the case of cancelled bookings TA/TO has the most percentage while Corporate has the least.

11) The length of the stay decreases as ADR increases probably to reduce the cost.

It's was Great EDA Project to enhance my skills.
    
Challenges
   1) Lot of null values were present in the dataset.
   2) Data type of some Data was in wrong format.
   3) Lot of duplicate data.
   4) Which visualization techniques to use was a challenge? 
