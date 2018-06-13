# Test Plan - CNN.com

1. Objectives
1. Tasks
1. Assumptions or Dependencies
1. Scope
1. Testing Strategy


## Objectives
Must answer these questions before beginning QA: 
* What is the scope and timeline/budget?
  * What features, flows or pages need to be tested?
  * Is there a list of user flows?
  * What browsers (+versions) are in scope?
  * What devices (+versions) are in scope?
* Is this for functional, design and/or accessibility quality assurance?
  * What are the functional requirements?
  * Where are the approved designs?
  * Is this for WCAG 2.0 compliance or accessibility?
* Request site run-through
* What environment is being tested?
* Will I need test accounts, credit cards or other credentials?
* How do developers expect to receive bugs for failures? *e.g. JIRA tickets, verify necessary info*
* Who do bugs get assigned to?  *e.g. back to project manager*

## Tasks
* Testing
* Reporting issues

### Creating tickets:
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

## Assumptions or dependencies

* Performance testing, development QA (unit, end-to-end) is not considered for this test plan
* Not using testing tools like Selenium, Webdriver, Websockets, Cucumber, Postman, Ghost Inspector, Watir
* Environment: testing production
* Purpose: this is a *comprehensive* QA audit of CNN.com
* Constraints: None, I have unlimited time and budget. This is a best-case scenario. But in reality, what’s the scope? Can I delegate some of these QA tasks to the UI-developer, the UX-developer, the Designer?

## Scope

### Pages/components/features
Create a document breaking down CNN.com:
* Home page (navigation, article sections, ad-space, footer, etc.), Travel, Money, Video, etc.

### Key user flows
* Using search to find articles on topics of interest
* Browsing news, clicking into articles and getting back to home screen
* Using CNN.com to watch TV

### Browsers/platforms/devices
List everything within scope

## Testing Strategy

### Exploratory QA (testing for *usability*)
* Check all internal and external links, phone numbers, and spelling
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

### Design QA
* Obtain approved designs
* Proofread all content and check that the language matches the approved copy
* Check for visual consistency between approved designs and web pages on ALL viewport sizes
* Check for hoverstates, animations, and other dynamic visuals not represented in static designs 
* Validate or create tickets for failures

### Functional QA
* Obtain list of requirements
* Develop test strategies, cases and plans based on requirements + pages/features/flows
* Evaluate and test 
* Mark requirements as resolved or create tickets for failures

### Accessibility QA
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
