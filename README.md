# Dataset-Investigation

## Dataset Description
The 'No-show appointments' dataset collects information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment. A number of characteristics about the patient are included in each row. These characteristics are the following:

PatientId: The national ID of each patient scheduled an appointment.
AppointmentID: The appointment ID assigned automatically and uniquelly by the system for each appointment.
Gender: The gender (M / F) of each patient schecduled an appointment.
ScheduledDay: The date and time of scheduling an appointment.
AppointmentDay: The date of the patient's appointment.
Age: The age of each patient schecduled an appointment.
Neighborhood: The neighborhood of each patient schecduled an appointment. This indicates the location of the hospital.
Scholarship: Indicates whether or not (1 / 0) the patient is enrolled in Brasilian welfare program Bolsa Família.
Hipertension: Indicates whether or not (1 / 0) the patient has a high blood pressure disease.
Diabetes: Indicates whether or not (1 / 0) the patient has a diabetes disease.
Alcoholism: Indicates whether or not (1 / 0) the patient is alcoholic.
Handicap: Indicates whether or not (1 / 0) the patient has any disability.
SMS_received: Indicates whether or not (1 / 0) the patient received a reminder SMS.
No-show: Indicates whether or not (Yes / No) the patient missed the appointment. it shows ‘No’ if the patient attended the appointment, and ‘Yes’ if they did not attend.

## Question(s) for Analysis
After reviewing the dataset, check it's attributes and the main context, several questions could be asked to explore the data. Here, we will focus on the following main questions:

What factors are important to predict if a patient will show up for their scheduled appointment?
How does the time difference between the scheduled date and the appointment date (waiting time) affect the no-show rate?

## Conclusions
In order to answer the first question, we started exploring the relation between each feature and the no_show rate, this exploration is done through the following:

First, the overall no_show rate represented in the statistical calculation and the pie chart, shows that the no_show rate is lower than the show rate, with almost %20 to %80.
The gender characteristic is not an important factor, and couldn't be used to predict if a female or a male patient will affect the rate show up for their appointment, since there is no sufficient difference in the no_show rate for male and female.
After grouping patients in age groups, the age feature could be one of the factors that may affect the no_show rate, and consider the younger patients may miss their appoints more than elder patients.
All appointments made in the neighborhood "ILHAS OCEÂNICAS DE TRINDADE" were missed. This will lead to predict that most of the future appointments in the mentioned neighborhood may be missed. On the other hand, all appointments from other neighborhoods have a moderate no_show rate.
The scholarship characteristic may not be an important factor, and may not be useful to affect the no_show rate, where the no_show rate difference is moderate.
The four health conditions ['hypertension', 'diabetes', 'alcoholism', 'handicap'] have no sufficient difference in the no_show rate whether having health condition or not. So, these features may not have an efficient effect on the no_show rate, and may not be useful to predict the show up rate in the future appointments.
The reminder sms is sent to remind patients with their appointments and to reduce the no_show rate, but through the statistics it have the opposite result, which lead to not considering it in predecting the no_show rate for the future appointment.
To answer the second question, the time difference between the scheduled date and the appointment date is calculated, and a statistics are computed in order to calculate the relationship between the waiting time and no_show rate. Referring to these statistics and charts represented, it's obvious that the no_show rate is getting a higher rate for longer waiting time (over 130 days), and it may be better to decrease the waiting time through preventing the far schedule of appointments to reduce the no_show rate.

The main limitation faced during exploring and anlyzing this dataset, is the limited time frame for the appointmentday, which is covering appointments from the last week of April 2016 till the first week of June 2016. This may not cover different seasons, so we recommend to involve a distributed time frames to cover different seasons and to have a wider dataset.
