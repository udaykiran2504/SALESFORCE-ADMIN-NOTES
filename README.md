
what is salesforce CRM?

sales force is a cloud based CRM platform which has a the  tools, technologies, and procedures to manage , improve or facilitate sales 
support and related interactions with customer and business partners 
CRM= customer Relationship management 
types of crm 
1. on premises crm
2.cloud based crm 
role of an administrator 

user support
user management ( access control, managing the user in the org, permissions, license )
data management
creating reports
building dashboards
business process autonation-decletative ( drag and drop)

salesforce editions
1.essential ( basic for small business)
2.professional
3.enterprise(full fledge version with no limitation )
4.unlimited( extension of some features)
5.developer( to learn has all the features )

WORKING WITH APPS

there are different types of apps in salesforce 
1.standard apps (sales , service, marketing )
2.app exchange apps ( app installed from market place which can be free or paid)
3. force.com platform( developers develop the app using apex language or declarative tools, visual force)
force.com is a PaaS which allow developers to develop the apps, they are hosted on sales force platform which are ready to integrate
sales force platform or applications


Force.com platform components= MVC FRAMEwork
 mvc= model view controller 
model layers where the database components exits like backend database
view layer where the UI of the app like ( HTML, CSS Components exist)
controller layer where the logic exist (js)

database components : objects, fields, records)
view layer components: pages(acc pages,opp page), tabs(acc tab,contact tab), apps(sales app, service app)
controll conponents: logic, functions like save, convert, autoresponse , datavalidation etc

to create a lignting  app
1.go to setup> app manager> create new app > create the app name , logo etc 
2.import the required objects > assign access> save and finish









objects = tables 
columns are fields 
rows are records 
lable = name 
data types are to define the which type if data to be stored


DATA TYPES IN salesforce CRM 


Salesforce Custom Field Data Types Reference Table


Data Type	Description / Behavior
Auto Number :	    A system-generated sequential number using a defined display format, automatically incremented for each new record.
Formula  :	    A read-only field whose value is derived from a custom expression and updates automatically when source fields change.
Roll-Up Summary	 :   A read-only field displaying aggregate values (sum, min, max) or record counts from a related list.
Lookup Relationship:	Links the object to another source object via a popup selection icon.
Master-Detail Relationship:	Establishes a parent-child bond where detail records require the relationship field, inherit sharing/ownership from the master, cascade delete with the master, and support roll-up summaries.
External Lookup Relationship:	Links the object to external data stored outside the Salesforce organization.
Checkbox:	Toggles a True (checked) or False (unchecked) value.
Currency:	Accepts and formats monetary values, optimizing spreadsheet exports.
Date / Date/Time:	Captures calendar dates or combined date and time inputs.
Email:	Validates email address formatting and integrates with contact/lead emailing features.
Geolocation:	Captures latitude and longitude coordinates for location tracking and distance calculations.
Number / Percent / Phone:	Handles numeric input, automatic percentage formatting, and standard phone number formatting.
Picklist / Picklist (Multi-Select):	Restricts input to predefined single or multiple selection lists.
Text / Text Area variants:	Supports standard text strings, basic multi-line text up to 255 characters, long/rich text up to 131,072 characters, and encrypted storage.
Time / URL:	Captures local time values and valid website links that open in separate windows.



creating a first objects and records 

CREATING AN OBJECT

1.click on the settings icon on the dev org
2.click setup
3.click on object manager
4.create a custom object ( label name , plural name)
5.Prior to saving the custom object, scroll to the bottom of the page and select the checkbox Launch New Custom Tab Wizard after saving this custom object.
6.Leave the rest of the values as default and click Save.
7.On the New Custom Object Tab page, click the Tab Style field and select a style you like. The style sets the icon to display in the UI for the object.
8.Click Next, Next, and Save.

CREATING FIELDS
1.go to object manager > select the object
2.In the sidebar, click Fields & Relationships. Notice that there are already some fields there. There’s a name field and some of the system fields you learned about earlier.
3.Click New in the top right.
4.select data type 
5.fill the label name , description
6.Check the Required box.
7.Click Next, Next again, and then Save.

after creating the objects we need to create tabs for it 
go to home >go to nav bar> select tabs > new > select the object> symbol > save

CREATING A RECORD
1.go to the app launcher > select the required app ( ex : sales)
2.serach the object in the NAV bar 
3.click new in the top corner
4.enter the details and save 

DATA MODELING RELATIONSHIP BUILDING

there are two types of relationships in sales force CRM 
1. lookup relation ship : Creates a relationship that links this object to another object. The relationship field allows users to click on a lookup icon to select a value from a popup list. The other object is the source of the values in the list.

2. master detailed relationship :Creates a special type of parent-child relationship between this object (the child, or "detail") and another object (the parent, or "master") where:
The relationship field is required on all detail records.
The ownership and sharing of a detail record are determined by the master record.
When a user deletes the master record, all detail records are deleted.
You can create rollup summary fields on the master record to summarize the detail records.
The relationship field allows users to click on a lookup icon to select a value from a popup list. The master object is the source of the values in the list.

3. external lookup relationship : Creates a relationship that links this object to an external object whose data is stored outside the Salesforce org.

CREATING A RELATIONSHIP 

How to Create a Lookup Relationship

Use this if the two objects are independent (e.g., if you delete the parent, the child should not be deleted).
1. Go to Setup (click the Gear Icon in the top right corner).
2. Click on the Object Manager tab at the top.
3. Find and click on the Child Object (the object where you want to fill in the field).
4. On the left sidebar, click Fields & Relationships, then click the New button in the top right.
5. Select Lookup Relationship from the list of data types and click Next.
6. In the Related To dropdown menu, choose the Parent Object you want to connect it to, then click Next.
7. Enter a Field Label (e.g., "Parent Company") and click Next.
8. Click Next through the security screens (Profile Visibility and Page Layouts).
9. Click Save.


How to Create a Master-Detail Relationship

Use this if the child cannot exist without the parent (e.g., if you delete the parent, all its child records are automatically deleted).
1. Go to Setup ➔ Object Manager.
2. Click on your Child Object (the "Detail" side).
3. Click Fields & Relationships on the left, then click New.
4. Select Master-Detail Relationship and click Next.
5. In the Related To dropdown, select your Parent Object (the "Master" side) and click Next.
6. Give your field a name. You can also check the Allow Reparenting box if you want users to be able to switch parents later. Click Next.
7. Click Next to confirm security and page layout choices.
8. Click Save.


IMPORTING THE DATA 
there are two types of methods to inmport the data in salesforce 
1.data import wizard
2.data loader
3.data loader.io( built in )

1. The Data Import Wizard

• What it is: A simple, built-in tool that runs directly inside your web browser under the Salesforce Setup menu.
• Best used for: Minor, everyday data cleanups and simple uploads managed by business users or administrators.
• Supported objects: Core standard objects (Accounts, Contacts, Leads, Solutions) and all Custom Objects.
• Key limits: It can only handle up to 50,000 records at a time. It cannot be used for certain major standard objects like Opportunities, Cases, or Products.

2. The Data Loader

• What it is: A powerful, standalone desktop application that you download and install locally on your Windows or Mac computer.
• Best used for: Large-scale data migrations, automated nightly backups, complex database operations, and massive record updates.
• Capabilities: It supports advanced actions like Delete, Hard Delete, and Export, and it can interact with every single data object in your entire Salesforce system.
• Key limits: It can process up to 5 million records per file upload by utilizing the Salesforce Bulk API.

3. Dataloader.io

• What it is: A popular, cloud-based web application built by MuleSoft (a Salesforce company) that you log into using your Salesforce credentials.
• Best used for: Users who need a middle ground—more power than the Wizard, but without installing a desktop app. It easily schedules automated imports and lookups related record IDs automatically.
• Key limits: The free tier restricts you to 10,000 records per month.

4. Salesforce Workbench

• What it is: A secure, web-based developer console tool designed for administrators and developers to interact directly with Salesforce APIs.
• Best used for: Advanced data tasks, testing quick data updates, or executing data operations using raw CSV or JSON files.


DATA EXPORT METHODS


1. Data Export Service (Weekly/Monthly Export)

• What it is: A built-in web tool inside Salesforce Setup that prepares an automated backup of your entire organization's data.
• Best used for: Complete system backups and archiving. You can set it to run automatically every week or every month.
• How it works: Salesforce packages all your records into downloadable CSV files compressed inside a ZIP file. Once ready, Salesforce sends you an email link to download the files.

2. Salesforce Reports (Export to Excel/CSV)

• What it is: The standard reporting engine that everyday business users use to read data on screen.
• Best used for: Quick, targeted lookups of specific files, lists, or clean spreadsheets (like a list of active open opportunities).
• How it works: You build a report, filter it to show exactly what you want, click the "Export" button, and download the results as a formatted Excel sheet (.xlsx) or a raw data file (.csv).
• Key limits: Standard report exports are capped at 256,000 rows or 100 columns for a single report run.

3. The Data Loader (Desktop Application)

• What it is: The same downloadable desktop program used for heavy imports can also extract data.
• Best used for: Large-scale data extraction, system-wide migrations, or setting up scheduled command-line exports to an external server.
• Capabilities: It bypasses standard report limits entirely and can export up to 5 million records across any object in your database using the Salesforce Bulk API.

4. Dataloader.io (Cloud App)

• What it is: The web-based MuleSoft application accessible through your browser.
• Best used for: Scheduling automatic, recurring data extractions directly into cloud storage locations like Dropbox, Box, or secure FTP servers.
• Capabilities: It allows you to build custom export queries visually without needing to write code or install software.

5. Salesforce Workbench

• What it is: The web-based developer console used for quick system management.
• Best used for: Admins and developers who need to run a quick SOQL (Salesforce Object Query Language) text query to extract targeted technical data directly into a downloadable CSV file.


CREATING LIST,FILTER, CHARTS 


1. Creating a List View

• Navigate to the Object: Open the app launcher (9-dot grid) to choose your app (like Sales), then click on the object's tab (such as Opportunities or Accounts) in the top navigation bar.
• Open List Controls: Click the List View Controls icon (the gear/cog icon in the top right corner of the record list view).
• Create New List: Select New from the dropdown menu.
• Name and Access: Enter your List Name (the API name will auto-populate) and choose who can see this list (Only me, All users, or a Group of users). Click Save.

2. Applying Filters to a List View

• Open the Filter Panel: Click the Filter icon (it looks like a funnel) in the top-right corner if the side panel isn't already open.
• Set Global Scope: Always check the default Filter by Owner setting. Change it from "My records" to All records if you want to search the entire database, then click Done.
• Add Custom Criteria: Click Add Filter for each rule you need to create:
	• Select your target Field (e.g., Stage or Amount).
	• Choose the correct Operator (e.g., equals, greater than, or contains).
	• Select or type the matching Value.
	• Click Done to lock in that specific rule.
• Save Changes: Click the blue Save button at the top of the filter panel to apply your rules and refresh the records list.

3. Adding a Chart to a List View

• Open Chart Settings: Click the Display As Chart icon (it looks like a small three-bar vertical chart) located in the upper-right corner next to the filter funnel.
• Access Chart Layouts: Click the Chart Settings icon (the gear/cog icon that appears inside the newly opened chart panel on the right).
• Configure Visuals: Select New Chart (or Edit Chart to change the current one) and configure three things:
	• Chart Type: Choose your visual layout (Pipeline / Donut Chart, Bar Chart, or Column Chart).
	• Aggregate Type: Choose how to measure the data (Sum, Average, or Count).
	• Grouping Field: Choose the field you want to group your segments by (such as grouping opportunity values by Stage or Fiscal Quarter).
• Save and Render: Click Save. The chart will instantly appear alongside your filtered list view rows.


CREATING A COMPACT LAYOUT

1.First, find and open the compact layouts node in Setup for Energy Audit.
2.From Setup, click Object Manager.
3.Click Energy Audit to open the object and then click Compact Layouts.
You can see that the System Default compact layout is assigned as the primary compact layout right now. We’re going to change that.
4.Click New.
5.Give the compact layout a label: Energy Audit Compact LayoutCopy.
6.Add  fields to the compact layout, in this order:
Click Save.
Now let’s set the compact layout that you created as the primary compact layout for the object. This step makes the compact layout the new default for the Energy Audit custom object.
1.Click Compact Layout Assignment and then Edit Assignment.
2.select Energy Audit Compact Layout and click Save.


Customize Record Page Components and Fields


1. Create a New Lightning Page

• Open the Builder: Go to Setup ➔ Type App Builder in the left Quick Find box ➔ Click Lightning App Builder.
• Start New Template: Click the New button at the top of the page.
• Choose Page Type: Select Record Page (or App Page / Home Page depending on your goal) and click Next.
• Name & Object: Type a Label for your page, select the target Object (e.g., Account or Opportunity), and click Next.
• Choose Layout: Select a structural layout template (like Header and Three Regions) and click Finish.

2. Customize & Manage the Page

• Add Components: Drag functional blocks (like Highlights Panel, Record Detail, or Chatter) from the left-hand Components pane and drop them onto the center canvas workspace.
• Adjust Component Properties: Click directly on any component you just placed on the canvas to update its specific settings in the right-hand properties pane.
• Rearrange or Delete: Click and drag components to move them to different sections of the canvas, or click the X icon in the corner of a component box to delete it.
• Save Work: Click the blue Save button in the top-right corner of the page header.

3. Assign the Page to a Profile

• Open Activation settings: Click the Activation button in the top-right header (if you just saved for the first time, this popup opens automatically).
• Select Assignment Depth: Click the App, Record Type, and Profile tab, then click Assign to Apps, Record Types, and Profiles.
• Step Through the Wizard:
	• Select the specific Lightning App where this page should appear and click Next.
	• Select your Form Factor (Desktop, Phone, or both) and click Next.
	• Choose the Record Type (usually Master) and click Next.
	• Check the boxes next to the specific User Profiles (like Custom: Sales Profile or System Administrator) that should see this layout.
• Review & Save: Review the final assignment summary matrix and click Save to push the page live for those users.



CREATING THE CUSTOM BUTTONS, ACTIONS


1. Creating Custom Buttons & Links

Use these to open external web links, launch internal Salesforce URLs, or run specific actions directly from a record.
• Navigate to the Object: Go to Setup ➔ Object Manager ➔ Select the object where you want the button or link to live (e.g., Account or Energy Audit).
• Start a New Element: Click Buttons, Links, and Actions on the left menu sidebar, then click the New Button or Link button in the top right.
• Define the Properties:
	• Enter a Label (e.g., Google Search). The Name (API name) will auto-populate.
• Choose the Type: Select one of the three visual display options:
	• Detail Page Link: Adds a clickable link at the top or bottom of the record page.
	• Detail Page Button: Adds a standard button to the action bar at the top of the record.
	• List Button: Adds a button to the top of an entire list view grid.
• Set the Target Behavior: Choose how it opens (e.g., Display in new window or Display in existing window with sidebar).
• Enter the Content/URL: In the large formula box at the bottom, type the destination. You can use the Insert Field tool to dynamically pass data (e.g., typing https://google.com and inserting the Account Name field).
• Save: Click Save, then click OK on the system confirmation popup.

2. Creating Custom Actions (Quick Actions)

Use these to let users quickly create new records, update specific fields, or log a call directly without navigating away from the page.
• Open the Tool: Inside the object's Buttons, Links, and Actions menu, click the New Action button.
• Choose the Action Type: Select what you want this button to do from the dropdown:
	• Create a Record: Opens a fast popup form to create a new related record.
	• Update a Record: Modifies specific fields on the current record instantly.
	• Log a Call: Lets users record a phone call interaction quickly.
• Select the Target: Choose which object or specific field is being impacted, enter a Label for the button (e.g., Quick Close), and click Save.
• Design the Popup Layout: A mini layout editor will open. Drag and drop only the fields you want the user to see inside the quick popup window, then click Save.
• Set Predefined Values (Optional): You can set fields to automatically fill in (e.g., automatically setting the Stage to "Closed Won" when this action is clicked).

3. Making Buttons & Actions Visible to Users

Just like Dynamic Forms, creating a button or action does not make it appear automatically. You must add it to the user interface.
• If using Standard Page Layouts:
	• Go to Page Layouts in the left sidebar of your object and open your active layout.
	• In the top selection palette, click Buttons (for custom links/buttons) or Mobile & Lightning Actions (for Quick Actions).
	• Drag your new button or action down into the Salesforce Mobile and Lightning Experience Actions panel on the canvas layout.
	• Click Save.
• If using Dynamic Forms / Lightning App Builder:
	• Open your record page in the Lightning App Builder (via Gear Icon ➔ Edit Page).
	• Click directly on the Highlights Panel component at the very top of the canvas layout.
	• In the right-hand properties panel, click Add Action.
	• Search for your custom button or action name, select it, and click Done.
	• Click Save at the top right of the screen.

1. Create an Object-Specific Action

Use this when the action belongs to a single object and needs to pull data from the record you are looking at.
• Find the Object: Go to Setup ➔ Object Manager ➔ Click the specific object you want (e.g., Account).
• Start the Action: Click Buttons, Links, and Actions on the left menu, then click New Action.
• Fill in Settings: Select your Action Type (like Create a Record or Update a Record), choose the target object, and enter a Label (the button name). Click Save.
• Design the Layout: Drag the fields you want users to fill out onto the mini-popup window layout, then click Save.
• Make it Visible: Open your object's Page Layout, drag your new action into the Salesforce Mobile and Lightning Experience Actions box, and click Save.

2. Create a Global Action

Use this when you want a button that can be clicked from anywhere in Salesforce (like the global "+" sign in the top-right header).
• Open Global Actions: Go to Setup ➔ Type Global Actions in the left Quick Find box ➔ Click Global Actions.
• Start the Action: Click the New Action button at the top.
• Fill in Settings: Select the Action Type (usually Create a Record), pick the target object, and give it a Label. Click Save.
• Design the Layout: Drag and drop the fields you want to show up in the quick-creation popup window, then click Save.
• Make it Visible: In the left Quick Find box, type Publisher Layouts ➔ Click Publisher Layouts ➔ Click Edit next to your global layout ➔ Drag your action into the Global Actions panel, and click Save.


Add a Global Action to the Global Actions Menu

• From Setup, click the Home tab.
• Enter PublisherCopy in the Quick Find box and click Publisher Layouts.
• Click Edit next to Global Layout.
• If the “Salesforce Mobile and Lightning Experience Actions” section isn’t customized, click override global publisher layout to override it.
• Click the Mobile & Lightning Actions category in the palette.
• Drag New Campaign from the palette into the Salesforce Mobile and Lightning Experience Actions section
• Save the layout.
