## Catering-Department-Business-Tools

After I finished designing a business tool for a restaurant to solve inventory management inefficiency, It left me with an intense new interest about automation and new edge technology implementation to streamline processes that could and should reduce the cost of products affecting positively to the cost of living. After all this is the utopical goal of a society that uses A.I. to its fullest potential. ( or maybe not that utopical)


###  Plan

##### Problem:
There is a current issue with items orders not requested and availability of wine, specially for the catering department. Also there is a prevalent ignorance of the daily or event consumption of alcohol to properly understand the inventory stock of the business.

##### Initial Explanation:
The inventory system in place lacks centralization and proper management with a clear visual of the numbers and key points of the inventory stock. This causes mistakes and struggle when reporting the numbers and availability levels to satisfy upcoming events beverage requirements.

Inventory is done in a mixture of excel file input, manual recording, and the use of their existing POS system (toast). Different input sources cause the data to be unreliable. Also there is a lack or poor understanding of inventory management techniques.

##### Proposed Solution:
Initial and progressive implementation of an appropriate system to the size of the business demands that properly and seamlessly allows the input of the number of items and allows a clear visualization of the quantities and consumption. Also the system will gradually scalate and integrate with other areas like the catering department, transforming into a centralized and progressive data environment that will make business processes more efficient, fast, reliable, clear, speeding up decisions, reducing errors and waste, and of course improving the reputation of a service with quality and professionalism.

I envision a ETL pipeline that will integrate the system that the restaurant chooses, either a custom tool or an established cloud system, to extract the data (input). Then, it will move the data to a, possibly for the size of the business, an access system or even to an excel file, proper transformation will be carried if necessary by a python script or even the same excel tool. As the amount of data increases and more systems integrate (kitchen, front and back of the house and even office clerical tasks data), we are going to use a tool like Bigquery for storage and quick query of data. From there the data will be loaded to a visualization tool to show relevant information.



##### Initial Workflow And Milestones Of The Process:

###### Phase One
Gather data from the different present sources of data.
Transforme in the appropriate way for analysis.
Make observations of the critical points to resolve the problem.
Create a proper visualization tool to make the representation of the issues.



###### Phase Two
Create a PWA app, minimalistic and efficient, that serves as an input tool of the number of stocks and consumption.
Establish a proper storage platform for loading the data (Excel, Access, Database in Place, Cloud).
Implement a proper Transformation and Analysis platform (if necessary) for the data to subsequently load it to a visualization tool.
Build and establish a visualization tool that will allow a clear observation of the key values. This platform will have easy integration with third party tools to connect other important business processes to initiate the next phase.


###### Phase Three
Proper integration of requesting orders, vendor connection, notification of crossing targets levels. Create a structure that will automate and keep track of the number of items and consumption, reducing the need for inventory work.


Phase Four
AI integration, create an AI agent that will assist in the bar inventory process and possibly integrate with other areas of the restaurant.



###  Development phase

#### Phase One
Gather data from the different present sources of data.
Data is coming from paper, some from excel files and some other will be scraped from the web to complement a more accurate and detailed data to work with.
The inventory is done, every two weeks, by the Bar Manager, who commonly writes down one by one the quantity of each product, then this data is passed to an excel file where it is stored for later review in order to make orders to re-stock.
In the same way, the Banquet’s department fills up consumption reports of everything that was consumed at each event. This data is manually filled on paper then it is stored in a folder to be reviewed when necessary. It is important to notice that this data is never put together or analyzed in any way.
In order to increase the data culture and collaboration between the Banquet’s department, the main bar, and the storage inventory numbers, i build a business intelligence tool, which is a Progressive Web App, that would facilitate bartenders to input the consumption data faster, easier, and in a immediate digital form that will find its way through a pipeline into a repository of data from the main bar and the storage, to made easier a subsequent analysis and use of a reliable source of data.
The tool will be built using Flask which it is a python library to build web application tools, it will be minimalistic design, but efficient functionality that will use a form to take the data properly validate and transform for it to be send, ether to a excel file, and access database , a postgresql database, or a cloud platform, also it will be structured and emailed to the departments manager so he can start working on the event’s bill to be paid.


Transforme in the appropriate way for analysis.
Data is gathered in excel and cleaned specially the scraped data needs some duplicates to be removed, trimmed, correct data syntax, and normalize the data.
In this initial phase, the data then will be structured in a proper dataset schema, either in a database or in the proper visualization tool.

Excel data sheets modeling:
=RIGHT(D2,LEN(D2)-SEARCH(" ",D2)). Clean name

Make observations of the critical points to resolve the problem.
Some important problems will be resolved just by properly integrating the banquet department data consumption.

List of the most important procedures to improve the inventory system:
Organize the inventory stock by removing any unused items or excess on items, or at the contrary make sure there are existent sufficient items when they are requested. This requires having just enough inventory according to sales over time, and implementation of target restock levels to always have items available.

To know what is in existence almost in real time or at least day by day is an important metric to have more in a fast paced business like this. This mechanism will be improved over time as software and hardware is designed and upgraded. As for now we are going to use the input of the staff which will set the metric daily then it will be compared by the observations of the bar manager.
