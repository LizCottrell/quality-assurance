* [Preface](#preface)
* [Pre-QA questions](#pre-qa-questions)
* [Assumptions](#assumptions)
* [Scope](#scope)
* [Testing Strategy](#testing-strategy)
    * [Exploratory QA](#exploratory-qa)
    * [Design QA](#design-qa)
    * [Functinal QA](#functional-qa)
    * [Accessibility QA](#accessibility-qa)
* [Examples](#examples)
    * [Test Cases](#test-cases)
    * [Tickets](#tickets)
* [Questions](#questions)

# Preface
QA Exercise - creating a test plan

**Purpose:** to test a large, content-focused website like CNN.com 

**Instructions:** create a test plan for the site, which should include steps to identify both visual and functional defects on multiple browsers, devices, and platforms. 

## Pre-QA questions:
* What is the scope and timeline/budget?
  * What features, flows or pages need to be tested?
  * Is there a list of user flows?
  * What browsers (+versions) are in scope?
  * What devices (+versions) are in scope?
* Is this for functional, design and/or accessibility quality assurance?
  * What are the functional requirements?
  * Where are the approved designs?
  * Is this for WCAG 2.0 compliance or accessibility?
* What environment is being tested?
* Will I need test accounts, credit cards or other credentials?
* How do developers expect to receive bugs for failures? *e.g. JIRA tickets, verify necessary info*
* Who do bugs get assigned to?  *e.g. back to project manager*

# Assumptions

* Performance testing, development QA, stress testing, API testing, etc. are not considered for this test plan
* This test plan covers functional and design QA (additions: exploratory and accessibility QA)
* QA is not using testing tools or test case management tools like Selenium or Zephyr
* Purpose: this is a *comprehensive* QA audit of CNN.com
* Constraints: None, I have unlimited time and budget. This is a best-case scenario. But in reality, what’s the scope? Can I delegate some of these QA tasks to the UI-developer, the UX-developer, the Designer?

# Tasks
* Determine scope
* Create test cases
* Test the site
* Report issues (log bugs)
* Regression testing

# Scope

## Pages, features & flows
Break down CNN.com into pages, features and user flows.  

Examples:
* Pages
    * Home page (navigation, article sections, ad-space, footer, etc.)
    * Travel
    * Money
    * Video
* Features
    * Search
    * Video
    * Sharing articles
* User flows
    * Using search to find articles on topics of interest
    * Browsing news, clicking into articles and getting back to home screen
    * Using CNN.com to watch TV and videos
    * Sharing articles via Facebook, Twitter and Email

## Browsers, platforms & devices
List everything within scope.

## Out of scope
List all out-of-scope features and functionality.

Examples:
* advertisements
* cable provider log-in

# Testing Strategy

## Exploratory QA 
* Test for usability
* Check all internal and external links, phone numbers, and spelling
* HTML validation
* Test form validation. Some examples:
   * What is required vs. optional? 
   * Can you enter anything in the email address or zip code field? 
   * If the application stops you from advancing, is there clear direction?
* Click through all navigation, including breadcrumbs
* Keep visual consistency in mind
  * e.g. look at how buttons and links are styled, compare from page to page or tool to tool
* Test atypical scenarios and for error checking
  * e.g. what happens if you don’t enter a search term and click Search?
* Ask questions like “Is this intuitive?” or “How much do I need to read or remember to move forward?”

## Design QA
* Obtain approved designs
* Proofread all content and check that the language matches the approved copy
* Check for hoverstates, animations, and other dynamic visuals not represented in static designs 
* Check for visual consistency between approved designs and web pages on ALL viewport sizes (desktop, tablet, mobile)
* Cross-browser testing
* Validate or create tickets for failures

## Functional QA
* Obtain list of requirements
* Develop test strategies and cases based on requirements + pages/features/flows
* Run test cases
* Mark requirements as resolved or create tickets for failures

## Accessibility QA
* Accessibility or compliance?
* Validate HTML
* Run automated tests (e.g. [HTML_CodeSniffer](https://squizlabs.github.io/HTML_CodeSniffer/))
* Attempt all user flows and navigation using
  * only the keyboard
  * screen readers (e.g. JAWS, VoiceOver, NVDA)
* Check for contrast issues, readable font sizes, and consistent & intuitive styling
* Check for correct usage of heading levels, informative link text, usage of HTML5 and ARIA attributes
* Check ALL web content (media: images, video, audio, PDFs, etc.) for accessibility
* Document successes/failures on the WCAG 2.0 checklist (see ADA audit report)

Regression testing (make sure no other features were unintentionally broken after fixes)

# Examples

## Test Cases

### Searching for a topic of interest on CNN Tech 
* **Page:** CNN Tech
* **Feature:** Search
* **Flow:** Search for a topic of interest
* **Steps:**
   * Step 1: Navigate to CNN Tech
   * Step 2: Click on the search icon
   * Step 3: Search for a topic of interest
   * Step 4: *need requirements to write expected result*
* **Edge Cases**
   * Enter nothing in the search bar and click search

### Sharing an article on CNN Travel using Twitter
* **Page:** CNN Travel
* **Feature:** Share an article
* **Flow:** Share an article using Twitter
* **Steps:**
   * Step 1: Navigate to CNN Travel
   * Step 2: Click into an article
   * Step 3: Click on the Twitter share icon under the headline
   * Step 4: Share article
   * Step 5: Check Twitter account to verify article is shared


## Tickets
* [bug-UI (global - links): inconsistent hover state on link text [Firefox]](https://github.com/LizCottrell/quality-assurance/issues/2)
* [bug-ADA (global - footer): insufficient contrast on footer text + links](https://github.com/LizCottrell/quality-assurance/issues/1)
* [bug (home page - navigation) spelling error](https://github.com/LizCottrell/quality-assurance/issues/4)
* [bug-UX (home page - search): search button too close to hamburger nav](https://github.com/LizCottrell/quality-assurance/issues/3)


Include the following information for every new issue:
* **Title:**`````<type>[optional scope]: <description>````` - clearly define *feature/location* + *issue* in the title
* **Labels:**
  * Bug type (functional, design or accessibility bug)
  * Priority
  * Environment 
  * Date
  * URL
* **Description:**
  * Device (native or simulator), OS, browser combination
  * User info: credentials used, account, account state, credit card used, etc
  * Steps to Recreate
  * Expected Result
  * Actual Result
* **Screenshots** or gif/video
* **Links:** 
  * to failed requirement
  * to approved design

# Questions

#### *What research did you do to prepare for this exercise?*
*  Read blogs:
   * [Katrina the Tester](http://katrinatester.blogspot.com/)
   * [Ministry of Testing: The Doji](https://www.ministryoftesting.com/dojo)
* Googled 
* Reviewed old work on ADA auditing
* Reviewed Think Company's QA development standards
* Reached out to QA + UX friends to get their feedback 

#### *What assumptions did you make about the work?*
* Performance testing, development QA (unit, end-to-end), security testing, etc. is not considered for this test plan
* Not using testing tools like Selenium, Webdriver, Websockets, Cucumber, Postman, Ghost Inspector, Watir
* Environment: I'm testing production
* Purpose: this is a *comprehensive* QA audit of CNN.com
* Constraints: None, I have unlimited time and budget. This is a best-case scenario. But in reality, what’s the scope? Can I delegate some of these QA tasks to the UI-developer, the UX-developer, the Designer?

#### *What is the process for communicating defects back to the development team that will be responsible for fixing them?*
* Logging issues **clearly** with appropriate labels
* Asking questions during QA to clear up any grey-areas early ("Is this a bug?")  
* Providing status reports (daily, weekly)
* Calling a meeting to run-through issues found if neccessary

#### *What tools would be useful to you in performing and tracking your work?*
* Performing a QA test:
  * Wireframes, sitemap, or list of URLs to help determine the scope of the project, identify components and aid in creating a testing strategy
  * Devices or simulators ([BrowserStack](https://www.browserstack.com/)), platforms (on computer or via VM), screen-readers, monitors
  * QA software (e.g. test case management tools, automated testing tools)
  * Accessibility: screen-readers (VoiceOver, JAWS, NVDA), automated testers like HTML_CodeSniffer, browser extensions
* Tracking issues: 
  * JIRA for recording issues
  * Confluence for recording QA standards + device/browser/OS per project, ADA reviews, copy docs, etc.
  * Screen-capture software, giphy capture

#### *How would testing a site like this differ from testing something like your bank’s website?*
* Financial services require added security, transactions, account information - a MUCH greater level of functionality to test
* Requires a different test plan + strategy
