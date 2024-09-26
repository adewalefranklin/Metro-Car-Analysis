Project Overview



Project Background

🚗 About Metrocar
Metrocar's business model is based on a platform that connects riders with drivers through a mobile application. Metrocar acts as an intermediary between riders and drivers, providing a user-friendly platform to connect them and facilitate the ride-hailing process.
 
📶 Metrocar’s Funnel
The customer funnel for Metrocar typically includes the following stages:
App Download: A user downloads the Metrocar app from the App Store or Google Play Store.
Signup: The user creates an account in the Metrocar app, including their name, email, phone number, and payment information.
Request Ride: The user opens the app and requests a ride by entering their pickup location, destination, and ride capacity (2 to 6 riders).
Driver Acceptance: A nearby driver receives the ride request and accepts the ride.
Ride: The driver arrives at the pickup location, and the user gets in the car and rides to their destination.
Payment: After the ride, the user is charged automatically through the app, and a receipt is sent to their email.
Review: The user is prompted to rate their driver and leave a review of their ride experience.
Similar to other customer funnels, there will be drop-offs at every stage of the funnel, which is why funnel analysis can be helpful in identifying areas for improvement and optimization. For example, Metrocar may analyze the percentage of users who download the app but do not complete the registration process, or the percentage of users who request a ride but cancel before the driver arrives.
 
🔎 Business questions

1.What steps of the funnel should we research and improve? Are there any specific drop-off points preventing users from completing their first ride?

2.Metrocar currently supports 3 different platforms: ios, android, and web. To recommend where to focus our marketing budget for the upcoming year, what insights can we make based on the platform?
3.What age groups perform best at each stage of our funnel? Which age group(s) likely contain our target customers?

4.Surge pricing is the practice of increasing the price of goods or services when there is the greatest demand for them. If we want to adopt a price-surging strategy, what does the distribution of ride requests look like throughout the day?

5.What part of our funnel has the lowest conversion rate? What can we do to improve this part of the funnel?

Dataset structure

You can find a description of each table and its columns below.
app_downloads: contains information about app downloads

app_download_key: unique id of an app download

platform: ios, android or web

download_ts: download timestamp

signups: contains information about new user signups

user_id: primary id for a user

session_id: id of app download

signup_ts: signup timestamp

age_range: the age range the user belongs to

ride_requests: contains information about rides

ride_id: primary id for a ride

user_id: foreign key to user (requester)

driver_id: foreign key to driver

request_ts: ride request timestamp

accept_ts: driver accept timestamp

pickup_location: pickup coordinates

destination_location: destination coordinates

pickup_ts: pickup timestamp

dropoff_ts: dropoff timestamp

cancel_ts: ride cancel timestamp (accept, pickup and dropoff timestamps may be null)

transactions: contains information about financial transactions based on completed rides:

ride_id: foreign key to ride

purchase_amount_usd: purchase amount in USD

charge_status: approved, cancelled

transaction_ts: transaction timestamp

reviews: contains information about driver reviews once rides are completed

review_id: primary id of review

ride_id: foreign key to ride

driver_id: foreign key to driver

user_id: foreign key to user (requester)

rating: rating from 0 to 5

free_response: text response given by user/requester

This project analyzed the customer funnel of Metrocar, a ride-sharing app (similar to Uber/Lyft) as stated above, to identify areas for improvement and optimization. SQL was used for data collection and Pandas(Python) was used for further analysis and visualisation. 
The stakeholders have asked several business questions that can uncover valuable insights for improving specific areas of the customer funnel. A funnel analysis was conducted and the analysis as well as business recommendation was provided accordingly based on the outcome of the analysis. 

