                  # plant-watering-reminder-system
IoT-based Plant Watering Reminder System using AWS IoT Core, Lambda, and SNS
---
 ### Structure:
  plant-watering-reminder-system/
 ├── lambda/
 │   └── soil_moisture_check.py
 ├── report/
 │   └── Plant_Watering_Reminder_System_Report.pdf
 ├── images/
 │   └── architecture.png
 └── README.md
 
  ### Sensors:
  *Sensor → IoT Core → Lambda → SNS → Email

  ###Lamda code:
  if moisture < 30:
    sns.publish(...)
   * Here, I check the moisture value. If it is below 30, an email alert is sent.


## 🔧 Implementation Steps

### Step 1: AWS Account Setup
- Created AWS Free Tier account
- Configured IAM user for secure access

### Step 2: Amazon SNS Configuration
- Created an SNS topic for plant watering alerts
- Subscribed an email endpoint
- Confirmed the email subscription

### Step 3: AWS Lambda Function
- Created a Lambda function using Python 3.10
- Implemented logic to check soil moisture values
- Integrated Lambda with Amazon SNS to send email alerts
- Tested the function using sample JSON events

### Step 4: AWS IoT Core Setup
- Created an IoT Thing and certificates
- Configured IoT policy and attached it to the Thing
- Created an IoT rule to trigger Lambda
- Tested data flow using MQTT messages

### Step 5: Testing and Results
- Low moisture values triggered email alerts
- Higher values did not trigger alerts
- System worked in real time





