# Orange Jellyfish Challenge

## Table of Contents
- [What is the purpose of this repo?](#what-is-the-purpose-of-this-repo)
- [Task](#task)
- [Mockup](#mockup)
- [Approach](#approach)

## What is the purpose of this repo?

This repo houses my response to the Orange Jellyfish Challenge issued through Founders and Coders bootcamp. It contains: 
 - This README outlining the challenge scenario and my approach
 - Mockup imagery
 - [GitHub Issues](https://github.com/malcolmwilson8/orange-jellyfish-challenge/issues) which explain concerns for the team to address within the challenge

## Task

As a software developer for an e-commerce site, my team is working on a new web application which will allow customers to complete their shopping online.

For this app, I need to deliver the following frontend functionality:

<em>"We need to display our products on a page for customers to view. They should be able to add and
remove these products from their shopping basket.</em>

<em>The backend team have just completed work on a 'getProducts' API which will return product
information from the database."</em>

I have a mockup image for the app (below) which I will use, along with the above information, to break the business requirements down into a series of tasks (via GitHub Issues) for the development team to work through.

Things to consider:
- Is there any further information that you as a developer require from the business before starting the development work?
- Think about potential errors that could occur when this new functionality is running in production, how would you handle/mitigate these?

## Mockup

![mockup](https://user-images.githubusercontent.com/117777716/226719178-112f4fb0-ef21-4f76-b94e-1d468ca84b0a.PNG)

The mockup contains a number of standout elements:

- A search field, likely allowing users to look for other products on site
- A nav bar, with 'Home', 'About' and 'Help' links, as well as a 'Your Basket' link featuring a basket SVG style icon
- A 'Product Results' section; the most detailed part of the page. This section contains individual product images, names, prices and star ratings for 6 products
- A 'Basket' pane to the right of the page, featuring a basket icon. This would likely be updated with relevant product information as the user selects their products


## Approach

First off, I want to address the 'Things to consider' elements of the task.

<em>Is there any further information that you as a developer require from the business before starting the development work?</em>

In bullet points below, I will list out the information I require, splitting it into **Technical** and **Non-technical** areas:

### Technical
    
- API Information
    - I would need some supplementary information on the 'getProducts' API:
        - Any supporting documentation which I could read to gain a better understanding of the API
        - If any keys or tokens need to be validated before the data gets sent to the frontend
        - Endpoint details which I would use to interact with the API on the frontend

- What tech stack, libraries and frameworks will I be using to complete the functionalities required? 
    - Alongside HTML, CSS and JavaScript, it is worth asking this as there are different ways to approach the challenge from a framework and library perspective. For example, would I need to use React, Angular or Vue.js to work on the components and build of the page itself? Also, it is worth asking:
        - What version control software would I be using?
        - What package management software would the project use?
        - Are there any requirements outside of the frontend functionalities listed? I.e. will I need to work directly on the backend side of the application also?

- Are there any functionalities the business would want to implement in the future?
    - If the business has an idea of work they want to be completed on the web application in the future, I could take this into account in my current work, and potentially even get a head start on some of the work for them. 
    
### Non-technical

- Are there any supplementary objectives that I might be asked to deliver on in addition to the functionalities required?
    - Some of the features I listed in the [Mockup](#mockup) section (search field, nav bar), do not necessarily relate to displaying products on the page, the API, or the shopping basket, but it would be good to know if I'd be asked to complete any functionality for those elements. It would be very useful to have objectives like these to mind before starting on the task so I know what I can push myself to achieve as an added bonus.

- What does the business expect from the web application by the end of my development work?
    - It is necessary to find out if I am only expected to deliver on a minimum viable product (MVP) version of the web application, or if I am being tasked with delivering the complete, production-ready solution. I would want to ask the business what exactly they expect from me, and I would do so within the context of the SMART framework (Specific, Measurable, Achievable, Realistic, Timebound), establishing clear goals for myself.

- What time frame am I working to within the project?
    - Within this process, it would be crucial to find out what important dates I would be working to. Finding out what the deadline for the completed app is, alongside any dates I would be required to give updates on my work would greatly influence the focus of my coding and my time management.

- Who would be responsible for signing off on the final functionalities I have delivered, and what influence do they have on the project overall?
    - I would need to find out if the way I work on the functionalities will be completely my own choice, or if I would be expected to follow a specific set of the business' practices for them. Also, it would be necessary to know who I would be submitting my code to, and to what extent they would be able to change the direction of my work. Knowing this ensures that I have clearly defined relationships with those I am working with, and helps ensure that any serious issues are avoided at the end of the development process.


<em>Think about potential errors that could occur when this new functionality is running in production, how would you handle/mitigate these?</em>

There are a number of potential errors that could occur when this functionality is running in production. Below I have listed these out, alongside how I would address them:

- Failure to retrieve API information, meaning that product information does not get rendered on the page correctly
    - This could occur as result of invalid API keys or authorisation on the API itself. If these issues arise within the frontend, steps could be taken to ensure that this is addressed:
        - On the frontend, parameters within the code itself could be looked over again to ensure they are returning the expected product information. This includes things like checking headers, endpoint details and ensuring that any promises used are working properly and returning the results needed. Additionally, token refreshes could be updated if these are required to access the app itself.

- Basket not updating with correct information
    - This could occur again due to errors and oversights within the codebase, and due to a lack of due diligence when testing the functionality for updating the basket itself. To address and mitigate these errors, a number of failsafes could be implemented:
        - Ensure testing functions are returning the intended results before committing functions into the codebase and deploying them: 
            - Making use of Unit Testing or Integration Testing would help ensure the basket updating function, and other functions on the page return the information needed. Iplementing suitable error handling within tests will assist with function issues by showing:
            - When the error happened first
            - The error type and message associated with it
            - Which line of code caused the error
            
            Taking the above information into account can help ensure code in production regarding basket updates or any other function on the page runs smoothly.

- Slow response times on the web app due to high usage
    - Due to a large amount of information being parsed from the backend, an excessively large CSS or JavaScript file, or a large amount of page traffic, page load times can greatly suffer, causing negative user experiences. Excessive fetch requests to an API can equally create adverse impacts to the response time on site. These factors can cause increased bounce rates, and can lead consumers to remember the negative experiences they have with the site, causing them to never visit again. Thankfully there are a few steps that can be taken to avoid these issues:
        - Testing the web app and its load times prior to deploying will give the best indication of what a user will experience when they are using the site. By reviewing load times after each change to the codebase, I would be able to identify which parts of code cause issues to load times, and work on refactoring these respectively.
        - Stress testing the web app before pushing code into production could help to identify excessive site load times, as well as other issues. For example, continuously reloading a page, or simulating a heavy load on the server or the API using a tool like https://loader.io/, could expose app-breaking load time issues and help identify if code needs to be refactored. 
        - Combining CSS and JavaScript files into one main CSS or JavaScript file may be a way to reduce overall app size, and thus reduce the need for the browser to make multiple requests to the server, making load times quicker.

With the two considerations addresssed, please see my [GitHub Issues](https://github.com/malcolmwilson8/orange-jellyfish-challenge/issues) which break the above business requirement down into a series of tasks for the development team to work through.


