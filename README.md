# plant-watering-reminder-system
IoT-based Plant Watering Reminder System using AWS IoT Core, Lambda, and SNS
---

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


- ## 📐 Architecture Diagram

The architecture of the Plant Watering Reminder System follows a serverless and event-driven cloud model.

### 🔄 Architecture Explanation
- The soil moisture sensor (simulated using MQTT) sends data to AWS IoT Core.
- AWS IoT Core receives and processes the incoming data securely.
- An IoT Rule triggers the AWS Lambda function automatically.
- AWS Lambda checks the soil moisture threshold.
- If the moisture level is low, Amazon SNS sends an email alert to the user.



