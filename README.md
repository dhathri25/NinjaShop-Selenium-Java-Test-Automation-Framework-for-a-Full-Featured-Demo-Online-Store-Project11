# NinjaShop Automation Framework

## Project Overview
NinjaShop is a Selenium-Java automation test framework developed to automate end-to-end testing of the demo e-commerce application located at: [https://tutorialsninja.com/demo](https://tutorialsninja.com/demo).

The framework is designed using the Page Object Model (POM) pattern and follows industry best practices, including reusable components, data-driven testing, and structured reporting.

---

## Project Structure
```
NinjaShop/
├── src/
│   ├── main/java/com/srm/ninjashop/
│   │   ├── config/
│   │   │   └── ConfigReader.java
│   │   ├── driver/
│   │   │   └── DriverFactory.java
│   │   ├── listeners/
│   │   │   └── TestListener.java
│   │   ├── pages/
│   │   │   ├── BasePage.java
│   │   │   ├── HomePage.java
│   │   │   ├── LoginPage.java
│   │   │   ├── RegisterPage.java
│   │   │   └── ... (Other Page Classes)
│   │   └── utils/
│   │       ├── ExtentReportManager.java
│   │       └── ScreenshotUtils.java
│   └── test/java/com/srm/ninjashop/
│       └── tests/
│           ├── LoginTest.java
│           ├── RegisterTest.java
│           └── ... (Other Test Classes)
├── testng.xml
├── pom.xml
├── config.properties
├── screenshots/
└── README.md
```

---

## Objectives
* Automate key e-commerce workflows.
* Implement a scalable test framework using the Page Object Model.
* Ensure maintainability and reusability of locators and methods.
* Generate detailed execution reports for stakeholders.
* Capture high-resolution screenshots automatically on test failure.

---

## Test Coverage

### Authentication
* Login with valid and invalid credentials.
* User account registration.
* Logout functionality and session termination.

### Product Module
* Product search by keyword.
* Navigation through product categories.
* Validation of product details and pricing.

### Cart Module
* Add products to the shopping cart.
* Update item quantities and remove products.
* Validation of cart subtotals and totals.

### Checkout Module
* End-to-end checkout process.
* Delivery details and payment method selection.
* Order confirmation and success page validation.

### Form Validations
* Mandatory field validation.
* Email format and password length validation.
* Checkout field error handling.

---

## Framework Design

### Page Object Model (POM)
* Each web page is represented by a dedicated Java class.
* WebElements and page actions are encapsulated within these classes.
* Test classes interact only with page methods, keeping test logic separate from locators.

### Core Components
* BasePage: Contains common reusable methods and synchronization logic.
* DriverFactory: Manages WebDriver initialization and browser specific configurations.
* ConfigReader: Handles reading environment data from the config.properties file.
* TestListener: Implements ITestListener to trigger screenshots upon failure.
* ExtentReportManager: Manages the generation of interactive HTML reports.

---

## Tech Stack
* Language: Java
* Automation: Selenium WebDriver
* Test Management: TestNG
* Build Tool: Maven
* Driver Management: WebDriverManager
* Reporting: ExtentReports

---

## Setup and Configuration
Configuration values are managed in the config.properties file:
* browser: Specify chrome or firefox.
* baseUrl: Application URL under test.
* timeout: Explicit wait timeout values.

---

## Execution Instructions
Tests can be executed via the TestNG suite:
* Right-click the testng.xml file in the project root.
* Select Run As -> TestNG Suite.

Alternatively, execute via Maven Command Line:
```bash
mvn clean test
```

---

## Reporting and Artifacts
* Extent Reports: Generated in the test-output or reports folder after execution. Reports include pass/fail status, execution logs, and embedded failure screenshots.
* Screenshots: Automatically stored in the /screenshots directory with a naming convention including the test name and timestamp.

---

## Key Features
* Clean separation of concerns via POM.
* Data-driven testing capability using TestNG.
* Environment-based execution via properties files.
* Synchronized execution using Explicit Waits.
* Automated HTML report generation.

---

## Author
Dhathri Putty