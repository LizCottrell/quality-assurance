# QA - creating a test plan

**Goal:** to test a large, content-focused website like CNN.com 

Create a test plan for the site, which should include steps to identify both visual and functional defects on multiple browsers, devices, and platforms. 


## Questions

*What research did you do to prepare for this exercise?*
*  Read blogs:
   * [Katrina the Tester](http://katrinatester.blogspot.com/)
   * [Ministry of Testing: The Doji](https://www.ministryoftesting.com/dojo)
* Googled [Sample QA Test Plan](https://www.softwaretestinghelp.com/wp-content/qa/uploads/2014/02/Live_Project_Test_Plan_SoftwareTestingHelp.pdf), QA tester job descriptions, QA tools, etc.
* Looked up my old work on ADA auditing
* Reviewed Think Company's QA development standards
* Reached out to QA + UX friends to get their feedback 

*What assumptions did you make about the work?*
* Performance testing, development QA (unit, end-to-end) is not considered for this test plan
* I am not using testing tools like Selenium, Webdriver, Websockets, Cucumber, Postman, Ghost Inspector, Watir
* Environment: I'm testing production
* Purpose: this is a *comprehensive* QA audit of CNN.com
* Constraints: None, I have unlimited time and budget. This is a best-case scenario. But in reality, what’s the scope? Can I delegate some of these QA tasks to the UI-developer, the UX-developer, the Designer?

*What is the process for communicating defects back to the development team that will be responsible for fixing them?*
* Logging issues **clearly** with appropriate labels
* Asking questions during QA to clear up any grey-areas early ("Is this a bug?")  
* Providing status reports (daily, weekly)
* Calling a meeting to run-through issues found if neccessary

*What tools would be useful to you in performing and tracking your work?*
* Performing a QA test:
  * Wireframes, sitemap, or list of URLs to help determine the scope of the project, identify components and aid in creating a testing strategy
  * Devices or simulators ([BrowserStack](https://www.browserstack.com/)), platforms (on computer or via VM), screen-readers, monitors
  * Screen-capture software, giphy capture
  * Accessibility: screen-readers (VoiceOver, JAWS, NVDA), automated testers like HTML_CodeSniffer, browser extensions
* Tracking issues: 
  * JIRA for recording issues
  * Confluence for recording QA standards + device/browser/OS per project, ADA reviews, copy docs, etc.
  * Spreadsheet

*How would testing a site like this differ from testing something like your bank’s website?*
* Content-focused sites that doesn't require authentication means less functionality to test
* Financial services require added security, transactions, account information - a MUCH greater level of functionality to test
* Requires a different test plan
