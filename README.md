# Investigate Hotel Business using Data Visualization

## Background
The hospitality industry is a highly competitive sector that requires continuous analysis to maintain profitability and customer satisfaction. With the rise of digital booking platforms and large datasets, we can leverage data visualization to gain deeper insights. Our focus is to understand customer behavior in hotel bookings and its relationship to booking cancellation rates.

## Questions:
1. What type of hotel is most frequently visited by customers?
2. Does the duration of stay affect the rate of hotel booking cancellations?
3. Does the lead time between hotel booking and guest arrival affect the rate of hotel booking cancellations?

## Objectives:
1. Data Preprocessing
2. Monthly Hotel Booking Analysis Based on Hotel Type: Analyze monthly booking trends based on different types of hotels.
3. Impact Analysis of Stay Duration on Hotel Booking Cancellation Rates: Examine how the duration of stay influences hotel booking cancellation rates.
4. Impact Analysis of Lead Time on Hotel Booking Cancellation Rates: Investigate how the lead time between booking and guest arrival affects the rate of booking cancellations.

## Data Preprocessing
- There are 119,390 entries data with 29 columns/features.
- The data types include object, int64, and float64.
- There are 33,261 duplicate data.
- There are missing values in the dataset: Children: 4, City: 488, Agent: 16,340, Company: 112,593.

### How to Handle Missing Values?
- Children (4) — Null values are replaced with 0, indicating that guests did not bring any children.
- Agent (16,340) — Null values are replaced with 0, indicating that guests made reservations independently or not through an agent.
- Company (112,593) — Null values are replaced with 0, indicating that guests did not come from a company.
- City (488) — Null values are replaced with ‘Undefined’, as the city is not specifically known.

### How to Handle Duplicate Data?
Approximately 27.86% of the data is duplicated. Removing these duplicate records may affect the statistical values in the analysis. Since the dataset lacks a unique ID or unique booking ID and date, duplicate data might contain important information. There could be identical bookings occurring at different times.

### How to Handle Inconsistent and Extreme Values?
Meal Category is divided into two:
- With Meal: Includes Breakfast, Full Board, and Dinner
- No Meal: Includes No Meal and Undefined

### Anomalous Data:
- Negative values and outliers that are significantly far from the data distribution in the “adr” feature.
- There are 180 booking records that do not have any guests.

### How to handle these issues?
- Drop or remove these rows.

## Monthly Hotel Booking Analysis Based on Hotel Type

![Screenshot 2024-08-17 122941](https://github.com/user-attachments/assets/2f57fb56-9ecc-42cf-b740-d2e111939556)

City Hotels hold a larger share of total bookings compared to Resort Hotels, with City Hotels at 66.41% and Resort Hotels at 33.59%.

This strong preference for City Hotels can be attributed to their prime locations and excellent accessibility, making them perfect for business travelers or visitors exploring urban attractions and shopping districts. The allure of City Hotels is further enhanced by their modern amenities, such as fitness centers, fine dining restaurants, and comprehensive room services, catering to guests who prioritize comfort and convenience.

In contrast, Resort Hotels might see lower demand due to higher prices or limited availability, particularly during peak holiday seasons. However, guests who choose Resort Hotels are often seeking a unique vacation experience and relaxation. Located in picturesque settings such as beaches, mountains, or tranquil rural areas, Resort Hotels offer an escape from the hustle and bustle, with facilities designed to fulfill their guests’ holiday desires.

![Screenshot 2024-08-17 123315](https://github.com/user-attachments/assets/82921c6d-59f3-45f1-8664-4a77bcb5e88f)

During the holiday season, hotel booking demand typically surges. The period from May to August is the busiest for both types of hotels, especially City Hotels, which experience a significant spike in bookings. This is driven by school holidays and numerous national holidays, such as collective leave days and religious celebrations like Ramadan and Eid between 2017–2019, providing many opportunities for people to take vacations and book hotels. The October to December holiday season, coinciding with Christmas and New Year, also sees increased bookings.

The period from January to March records the lowest booking levels, mainly due to the lack of national holidays, the start of a new academic year for students, and generally less busy business travel activity at the beginning of the year.

## Impact Analysis of Stay Duration on Hotel Bookings Cancelation Rate

![Screenshot 2024-08-17 124328](https://github.com/user-attachments/assets/d1c522c0-e0c0-4c62-88a4-082c14a9b9b3)

![Screenshot 2024-08-17 124452](https://github.com/user-attachments/assets/aded9944-b1f7-4da1-97cc-a6d9dfdcda4b)

The higher cancellation rate at City Hotels (41.79%) compared to Resort Hotels (27.77%) indicates that guests are more likely to cancel their reservations at City Hotels. Several factors might contribute to this trend:

1. City Hotels are often located in bustling city centers with numerous accommodation options nearby. Guests may find it easier to cancel their bookings and switch to another hotel in the vicinity.
2. Many City Hotel guests are business travelers, whose plans can frequently change or be canceled at short notice.
3. Resort Hotels exhibit a lower cancellation rate (27.77%), suggesting that guests are generally more committed to their plans when booking these accommodations.

- Resort Hotels are typically chosen for vacations planned well in advance. Guests are usually more certain about their holiday schedules, which reduces the likelihood of cancellations.
- These hotels are often situated in exclusive locations such as beaches or mountains, making it harder for guests to find comparable alternatives, thereby increasing their commitment to their booking.

![Screenshot 2024-08-17 124843](https://github.com/user-attachments/assets/1a0c1763-f427-4c57-af5c-3dcb1be5d2f4)

The high cancellation rate for longer stays at City Hotels indicates a greater level of uncertainty and changes in guests’ plans, which may often involve business travel. On the other hand, Resort Hotels exhibit a lower overall cancellation rate, reflecting a higher commitment from guests who are planning vacations.

## Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate

![Screenshot 2024-08-17 125255](https://github.com/user-attachments/assets/a3533059-3892-4152-9966-29d3d4a3c26a)

City Hotels dominate in terms of cancellations, with cancellation rates increasing as the lead time approaches one year. Conversely, cancellations remain low for lead times of less than one month. Given this trend, the company might consider implementing a maximum booking lead time to reduce the risk of cancellations due to plan changes or the discovery of more appealing hotel options by customers.

## CONCLUSION

### Which type of hotel is most frequently visited by customers?

City Hotels are the most frequently visited, as they represent a larger share of the total bookings compared to Resort Hotels.

### Does the duration of stay affect the hotel booking cancellation rate?

Yes, it does. City Hotels experience a higher cancellation rate with longer stays. This may be due to factors such as changes in plans, urgent needs, or unforeseen situations.

### Does the time gap between booking and guest arrival affect the hotel booking cancellation rate?

Yes, it does. In City Hotels, cancellations tend to increase as the lead time approaches one year. Conversely, cancellations remain low for lead times of less than one month.

