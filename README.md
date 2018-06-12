# QA - creating a test plan

**Goal:** to test a large, content-focused website like CNN.com 

Create a test plan for the site, which should include steps to identify both visual and functional defects on multiple browsers, devices, and platforms. 


##  Questions Before Testing
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


## QA Types

### Functional:

* Obtain list of requirements + list of browser/device/OS's in scope + native devices and/or simulators
* Develop test strategies, cases and plans based on requirements + pages/features/flows
* Evaluate and test (performance, regulatory, expected behavior, etc.)
* Mark requirements as resolved or create tickets for failures

### Design:

* Obtain approved designs + list of browser/device/OS's in scope + native devices and/or simulators
* Proofread all content and check that the language matches the approved copy
* Check for visual consistency between approved designs and web pages on ALL viewport sizes
* Check for hoverstates, animations, and other dynamic visuals not represented in static designs 
* Validate or create tickets for failures

### Accessibility:

* Obtain list of browser/device/OS's in scope + native devices and/or simulators + assistive technology
* Validate HTML
* Run automated tests (e.g. [HTML_CodeSniffer](https://squizlabs.github.io/HTML_CodeSniffer/))
* Attempt all user flows and navigation using
  * only the keyboard
  * screen readers (e.g. JAWS, VoiceOver, NVDA)
* Check for contrast issues, readable font sizes, and consistent & intuitive styling
* Check for correct usage of heading levels, informative link text, usage of HTML5 and ARIA attributes
* Check ALL web content (media: images, video, audio, PDFs, etc.) for accessibility
* Document successes/failures on the WCAG 2.0 checklist


## Creating Tickets
* **Title:**`````<type>[optional scope]: <description>````` - clearly define *feature/location* + *issue* in the title
* **Labels:**
  * Bug type (functional, design or accessibility bug)
  * Priority
  * Environment 
  * Date
  * URL|
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

## Questions

*What research did you do to prepare for this exercise?*
*  Reading blogs:
  * [Katrina the Tester](http://katrinatester.blogspot.com/)
  * [Ministry of Testing: The Doji](https://www.ministryoftesting.com/dojo)
* Reviewed QA tester job descriptions
* Reached out to QA friends
* Reviewed Think Company's QA development standards
* Looked up my old work

*What assumptions did you make about the work?*
* Content-only, no authentication required

*What is the process for communicating defects back to the development team that will be responsible for fixing them?*
* Logging issues
* Chatting via messenger or in-person about any questions that arise during QA
* Calling a meeting to run-through issues found during QA

*What tools would be useful to you in performing and tracking your work?*
* Performing QA test:
  * Devices or simulators, platforms (on computer or via VM), screen-readers, monitors
  * Screen-capture software, giphy capture or video recording (like Loom)
  * Accessibility: screen-readers (VoiceOver, JAWS, NVDA), automated testers like HTML_CodeSniffer, browser extensions
* Tracking: 
  * JIRA for recording issues
  * Confluence for recording QA standards + device/browser/OS per project, ADA reviews, copy docs, etc.
  * Spreadsheet as a scratch pad

*How would testing a site like this differ from testing something like your bank’s website?*
* Content-focused sites that doesn't require authentication means less functionality to test
* Financial services require added security, transactions, account information - a MUCH greater level of functionality to test
* Requires a different test plan
