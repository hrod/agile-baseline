##Implementation Methods

- Code Review
- Quality Assurance and Automated Testing
- Web Performance 

## Development 

We believe at CivicActions that we are not just responsible for architecting a site, but rather a complete site experience. Our site building reflects a careful and thorough approach to all site user needs so that users can perform their tasks without the system getting in the way. 

Some strategies we employ to improve the backend user experience include:
* decluttering the user interface
* presenting as few options as necessary and hiding additional options in vertical tabs, * crafting important help text
* providing customized dashboards
* configuring rules and workflow options
* creating administrative views to perform common bulk content operations. 

Our mission is to implement a content management experience that empowers all users of the system, not just technical administrators. While we strive to put important site configuration in code so that it can be tested before release, versioned in repositories, and easily deployed, content remains in the database so that users can make changes without needing to call their local site admin.

As for our front end development approach, CivicActions uses a design component driven approach in order to implement our designs. Developers and designers work together to identify reusable design patterns to code once and extend as needed to minimize code complexity and size, reduce negative performance impacts, allow for easy maintainability and scalability, and also ensure that design changes can be made once and reflected throughout the site. We utilize a SMACSS-based approach (Scalable and Modular Architecture for CSS) for writing our CSS and organizing our files, as well as the Sass CSS preprocessor in order to write cleaner, more maintainable code. 

## Code Review 

To ensure that our code is as stable and scalable as possible, we adopt a rigorous code review and automated testing process that is designed to prevent bugs from entering the system. Each developer that touches the site works on his or her own local computer and pushes code to their own branch of the project’s Git repository. Once they submit a merge request to contribute code to the main project, a Tech Lead or fellow engineer will review the code for any errors, syntax, and potential performance impacts. After the code review is complete, a Jenkins build will verify whether the code is stable before it can be pulled into a development environment, where internal QA will be performed before the final client signoff. These multiple layers of workflow ensure that code and its subsequent functionality have been reviewed substantially before impacting a production environment.

## Quality Assurance and Automated Testing 

CivicActions is committed to code quality and our Quality Assurance (QA) processes are rigorous, having been formed throughout our longstanding attention to this area. We practice continuous QA during product delivery by making QA and testing part of the development process, and not reserving them until code has been pushed to the live environment.  Our workflow includes checks and balances to ensure that we meet expectations for the entire process through to the end product. This includes communication between all members of the team and stakeholders along with quality written and commented code.

CivicActions incorporates both automated and manual testing processes to ensure code compliance. Our process advocates for careful requirements gathering, definition of acceptance criteria, and multiple forms of validation. The specific website goals and functionality are assessed to identify the most appropriate testing method(s), including:

**Manual Testing**: The development team performs smoke testing and involves other stakeholders, like the product owner, for validation.

**Systematic Testing**: Systematic tests are driven by explicit QA goals and/or instructions contained in each individual implementation ticket. An implementation ticket could contain all or a portion of work needed to fulfill a project requirement.

**Automated Testing**: Types of tests include:

* Verifying compliance of W3C standards.
* Selenium/Behat testing - tests that need to be repeated often can be scripted using Selenium or the Behat frameworks. These tasks can include common actions as logging in or creating a new user, and can also be more robust to include high risk areas of the site that often get tested in regression testing. 
* Automated browser testing - using a combination of Cross Browser Testing and/or Browsers to check all pages on the site for browser compatibility against browser matrix -IE7, IE8, IE9, Safari, Chrome, FF - exact device and browser matrix for the project are discussed and agreed at project kick off.
* Security script testing - Besides relying on Drupal's high quality code, good coding practices and a code review by our Engineering Manager, we are also able to run the coder module to look for security issues any place that there is text entry.
* 508 compliance leveraging tools like QUAIL and WAVE to meet both Web Content Accessibility Guidelines (WCAG) and Authoring Tool Accessibility Guidelines (ATAG).

**Regression testing**: This testing is typically carried out at the end of a formal round of QA and includes regression testing to assess ALL site functionality to ensure no items that were previously functional have been “broken.” 

## Web Performance 

Another essential ingredient of web development at CivicActions is web performance. We at CivicActions take a holistic approach to web performance, utilizing opportunities to optimize through front-end development, backend development, hardware configuration, caching, content delivery networks, etc. To optimize web performance, we:
* use as few modules as possible
* concatenate and minify all code
* losslessly compress image assets
* use reverse-proxy caching such as Varnish to cache all static content
* serve files and pages from a CDN
* implement backend solutions such as Memcache. 

We frequently scan page speed times using tools such as Page Speed, YSlow, and server and application monitoring tools. Image assets are generally eschewed in favor of icon fonts and/or sprites when necessary. Instead of using unnecessary Javascript, we use CSS3 animations with appropriate fallbacks when available. 


