# Megaline-SDA-Project
In this statistical data analysis project for telecom operator Megaline, we will determinie which prepaid plans, Surf and Ultimate, brings in more revenue in order to determine their budget for their advertising team.

I will analyze the clients' behavior by using data from 500 Megaline customers. The data includes which plan the clients use, where they are from, who the clients are, the number of calls made, and the text messages sent from 2018. Based on this data, I will then conclude which prepaid plan brings in more revenue by using hypothesis.

- Null Hypothesis: No difference in average revenue between Ultimate and Surf Plans
- Alt. Hypothesis: Difference in average revenue between Ultimate and Surf Plans

# Description 
The `users` table (data on users):

- user_id — unique user identifier
- first_name — user's name
- last_name — user's last name
- age — user's age (years)
- reg_date — subscription date (dd, mm, yy)
- churn_date — the date the user stopped using the service (if the value is missing, the calling plan was being used when this database was extracted)
- city — user's city of residence
- plan — calling plan name

The `calls` table (data on calls):

- id — unique call identifier
- call_date — call date
- duration — call duration (in minutes)
- user_id — the identifier of the user making the call

The `messages` table (data on texts):

- id — unique text message identifier
- message_date — text message date
- user_id — the identifier of the user sending the text

The `internet` table (data on web sessions):

- id — unique session identifier
- mb_used — the volume of data spent during the session (in megabytes)
- session_date — web session date
- user_id — user identifier

The `plans` table (data on the plans):

- plan_name — calling plan name
- usd_monthly_fee — monthly charge in US dollars
- minutes_included — monthly minute allowance
- messages_included — monthly text allowance
- mb_per_month_included — data volume allowance (in megabytes)
- usd_per_minute — price per minute after exceeding the package limits (e.g., if the package includes 100 minutes, the 101st minute will be charged)
- usd_per_message — price per text after exceeding the package limits
- usd_per_gb — price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 megabytes)



# Conclusion
*Usage Patterns:*

- Call Duration: Surf users have a higher mean call duration and greater variability in call lengths compared to Ultimate users.

- Text Messages: Surf users send more messages on average than Ultimate users.

- Data Usage: Surf users consume more data on average and exhibit a higher rate of exceeding their data limits compared to Ultimate users.

*Overage Charges:*

- Surf Plan: Despite having a lower base monthly charge, Surf users often incur higher costs due to overage charges, especially for data. This is due to Surf users' higher data consumption and the higher per-GB charge for excess data.

- Ultimate Plan: The higher base monthly charge is offset by lower overage charges. This plan is more suited to heavy users as the cost of exceeding allowances is lower.

*Revenue Generation:*

- Ultimate Plan: Generates more consistent revenue due to its higher base charge, making it more predictable.

- Surf Plan: Potentially generates higher revenue from users who frequently exceed their included allowances, particularly in data usage.

*Statistical Significance:*

- There is a statistically significant difference in average revenue between the Ultimate and Surf plans, with a p-value of 0.0186, which is less than the alpha value of 0.05.

- There is also a significant difference in revenue between users in the NY-NJ area and those from other regions.

The Ultimate Plan is more stable and predictable in terms of revenue due to its higher base charge. It suits users with high but manageable usage, providing a lower cost for additional usage. The Surf Plan, while offering a lower base charge, may result in higher revenues from users with heavy or inconsistent usage patterns due to frequent overages, particularly in data.

To adjust the advertising budget effectively, consider focusing on promoting the Ultimate Plan to attract users with high and consistent usage, while leveraging the Surf Plan's potential for higher revenue from heavy users who exceed their allowances.
