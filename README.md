**Selenium TestNG Automation Framework
A Java‑based automation framework using Selenium 4, TestNG, and Maven, designed for web UI testing with data‑driven capabilities via Config.properties.**

📦 Features
Selenium 4 + Java + TestNG + Maven structure.

Page Object Model (POM) with reusable page classes.

Data driven using Config.properties (no external Excel dependency).

Extensible logging and explicit‑wait‑ready page objects.

Simple test‑case design with testBase for driver and configuration management.

📁 Project Structure
text
src
 ├── main
 │   └── java
 │       └── pageObjectRepository    → page classes (LoginPage, MicrosoftLoginPageObjects, etc.)
 └── test
     └── java
         └── testCases              → TestNG test classes (e.g., MicrosoftLoginFromConfig_TestCases)
         └── testBase               → Base class with driver and config setup
         └── utils                  → utilities (PropertiesOperations, DateUtil, logging)
🛠 Prerequisites
Java 11 / 17

Maven

Google Chrome or Microsoft Edge

Eclipse (or any Java IDE)

🔧 Setup & Run
1. Clone the project
bash
git clone https://github.com/yourusername/baseautomation.git
cd baseautomation
Replace yourusername/baseautomation with your actual username and repo name.

2. Install dependencies
bash
mvn clean test-compile
3. Configure Config.properties
Update src/test/resources/Config.properties:

text
url=https://yourapp.com/
browser=chrome

active-username=test@example.com
password=yourPassword123
Replace https://yourapp.com/ with the actual site you are testing.

4. Run Tests
From command line (Maven):

bash
mvn test
From Eclipse:

Right‑click your test class → Run As → TestNG Test.

This executes the login‑first test (and any follow‑on methods if you add them).
