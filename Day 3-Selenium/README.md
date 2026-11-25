1. What is Selenium?

Selenium is an open-source automation testing tool used to automate web browsers. It helps testers perform actions on web applications automatically instead of manually interacting with them.

Why Selenium?

Automates web browsers.

Reduces repetitive manual testing.

Helps test web applications efficiently.

Supports multiple browsers such as Chrome, Firefox and Edge.

Supports programming languages such as Python, Java, C# and JavaScript.


2. What is Browser Automation?

Browser automation means using a program to control a web browser and perform actions automatically.


3. Selenium WebDriver

Selenium WebDriver is used to programmatically control a browser and interact with webpage elements.

Selenium Automation Flow

Python Script → Selenium WebDriver → Browser → Web Application

The Python script sends instructions to Selenium WebDriver, which controls the browser to perform the required actions.

4. What is a Web Element?

A Web Element is an individual component present on a webpage.

Examples:

Textbox

Button

Checkbox

Radio button

Dropdown

Link

Image

5. What is a Locator?

A Locator is a mechanism used to identify and locate web elements on a webpage so that Selenium can interact with them.

Locators help Selenium find specific elements such as textboxes, buttons, links and other webpage components.

Why are Locators needed?

A webpage may contain multiple elements. Selenium needs a way to identify the correct element before performing an action.

For example:

Find the username textbox.

Find the Login button.

Find the Forgot Password link.

6. Types of Locators in Selenium

Selenium WebDriver provides 8 traditional locator strategies.

1. ID

Used to locate an element using its ID attribute.

HTML:

<input id="username" type="text">

Python:

driver.find_element(By.ID, "username")

2. Name

Used to locate an element using its name attribute.

HTML:

<input name="email" type="text">

Python:

driver.find_element(By.NAME, "email")

3. Class Name

Used to locate an element using its class attribute.

HTML:

<input class="input-field" type="text">

Python:

driver.find_element(By.CLASS_NAME, "input-field")

4. Tag Name

Used to locate an element using its HTML tag.

HTML:

<button>Login</button>

Python:

driver.find_element(By.TAG_NAME, "button")

5. Link Text

Used to locate a hyperlink using its complete visible text.

HTML:

<a href="/forgot">Forgot Password</a>

Python:

driver.find_element(By.LINK_TEXT, "Forgot Password")

6. Partial Link Text

Used to locate a hyperlink using a part of its visible text.

HTML:

<a href="/support">Contact Customer Support</a>

Python:

driver.find_element(By.PARTIAL_LINK_TEXT, "Customer")

7. CSS Selector

Used to locate elements using CSS selector syntax such as IDs, classes and attributes.

Using ID:

<input id="username">

driver.find_element(By.CSS_SELECTOR, "#username")

Using Class:

<input class="input-field">

driver.find_element(By.CSS_SELECTOR, ".input-field")

Using Attribute:

<input name="email" type="text">

driver.find_element(By.CSS_SELECTOR, "input[name='email']")

CSS Selector symbols:

# → ID

. → Class

[attribute='value'] → Attribute selector

8. XPath

XPath stands for XML Path Language.

It is used to navigate through the HTML structure and locate elements using attributes, text or relationships between elements.

Using ID:

<input id="username">

driver.find_element(By.XPATH, "//*[@id='username']")

Using Tag and Attribute:

<input name="email">

driver.find_element(By.XPATH, "//input[@name='email']")

Using Text:

<button>Login</button>

driver.find_element(By.XPATH, "//button[text()='Login']")

Using Partial Text:

<button>Login to Your Account</button>

driver.find_element(By.XPATH, "//button[contains(text(),'Login')]")

7. Difference Between CSS Selector and XPath

CSS Selector

XPath

Uses CSS selector syntax

Uses XPath expressions

Uses # to identify ID

Can identify ID using attributes

Uses . to identify Class

Can identify class using attributes

Useful for selecting elements using attributes and CSS structure

Useful for attributes, text and relationships between elements

Example: #username

Example: //*[@id='username']

8. Important Selenium Methods

find_element()- Finds one matching element

find_elements()- Finds all matching elements

click()- Clicks an element

send_keys()- Enters text into an input field

clear()- Clears the text in an input field

is_displayed()- Checks whether an element is visible

is_enabled()- Checks whether an element is enabled

is_selected()- Checks whether an element is selected

9. Difference Between find_element() and find_elements()

find_element()

Returns the first matching element.

Raises an exception if no matching element is found.

find_elements()

Returns a list of matching elements.

Returns an empty list if no matching elements are found.

10. Basic Selenium Login Example

HTML:

<input id="username" type="text">

<input id="password" type="password">

<button id="login">Login</button>

Python:

from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()

driver.get("https://example.com")

driver.find_element(By.ID, "username").send_keys("student")

driver.find_element(By.ID, "password").send_keys("12345")

driver.find_element(By.ID, "login").click()

Explanation

webdriver.Chrome() → Opens Chrome browser.

driver.get() → Opens the specified website.

find_element() → Locates the required element.

send_keys() → Enters text.

click() → Clicks the element.
