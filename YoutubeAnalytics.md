# Lesson 1 – Data Cleaning and Visualization: YouTube Analytics Dashboard

<br>

## Dataset <br>

Name: YouTube_Analytics.csv <br>
This dataset contains weekly performance metrics from a YouTube channel, including total views, subscribers gained and lost, likes, comments, shares, and watch time. <br>
It will be used to build a complete interactive dashboard in Power BI. <br><br>

## Learning Objectives <br>

By the end of this lesson, you will be able to:
• Import and clean raw data using Power Query. <br>
• Adjust data types, remove errors and null values. <br>
• Design and format a professional report canvas. <br>
• Create KPI cards for key performance metrics. <br>
• Build analytical visuals (Table, Column Chart, Line Chart). <br>
• Add interactive slicers for filtering data. <br>
• Apply consistent formatting and export a professional dashboard. <br> <br><br>

## Lesson Overview <br>

In this first lesson, you will follow the full data-to-dashboard workflow: <br>
Data import and cleaning in Power Query. <br>
Report layout setup in Power BI Desktop. <br>
Building and formatting visuals. <br>
Adding interactivity and visual consistency. <br> <br><br>

## Expected Dashboard <br>
<img width="1299" height="733" alt="Screenshot 2025-11-01 174542" src="https://github.com/user-attachments/assets/df32d554-3405-4f8c-9f26-8ff0de42b53e" />


## Step 0 – Data Cleaning and Preparation (Power Query) <br>

Open Power BI Desktop and go to Home → Get Data → Text/CSV. <br>
Select the file YouTube_Analytics.csv and check the preview. <br>
Make sure the delimiter is Comma (,) and load the first 200 rows for preview. <br>
Click Transform Data to open Power Query Editor. <br>

If your dataset contains a first row labeled Total or another summary row, remove it using Home → Remove Rows → Remove Top Rows → 1. <br>
If the first row contains column names, select Home → Use First Row as Headers. <br>

Replace null values by selecting columns such as Videos Added, Likes, or Comments and going to Transform → Replace Values. <br>
Find null and replace it with 0 so that missing values become zeros instead of blanks. <br>

Remove any data errors with Home → Remove Rows → Remove Errors, which deletes invalid or corrupted rows (for example, row 501). <br>

Assign proper data types to each column. <br>
Change Date to Date, Subscribers, Videos Added, Views, Likes, Comments to Whole Number, Watch Time (hours) to Decimal Number, Average View Duration to Duration, and Stayed to Watch (%) to Decimal Number. <br>
If Power BI does not recognize a column type, right-click the column → Change Type → [correct type]. <br>

Rename columns for clarity by right-clicking and selecting Rename. <br>
For example: Subscribers gained → New Subscribers, Subscribers lost → Lost Subscribers, Videos added → Videos Published, Stayed to watch (%) → Watch Retention (%), and Average views per viewer → Avg Views per Viewer. <br>

When you finish, your applied steps should read: <br>
Source → Removed Rows → Promoted Headers → Replaced Values → Removed Errors → Changed Type → Renamed Columns. <br>

Click Close & Apply to load the cleaned dataset into the report model. <br> <br><br>

## Step 1 – Canvas Setup (Background and Title) <br>

Go to the Report View and click on a blank area of the canvas. <br>
In the Visualizations pane, open the Format Page (paint roller icon) and expand Canvas settings. <br>
Set the page size to 16:9, background color to White (#FFFFFF) or Light Grey (#F5F5F5), and transparency to 0%. <br>
Go to Insert → Text Box and type the title **YouTube Channel Performance Dashboard**. <br>
Format the title using font Segoe UI Semibold, size 28 pt, color #E50914, and center alignment. <br> <br><br>

## Step 2 – KPI Cards (Key Metrics) <br>

Create three KPI cards for Total Subscribers, Total Views, and Watch Time (hours). <br>
Click on the Card visual in the Visualizations pane. <br>
In Build visual, drag the corresponding field into Values. <br>

In Format visual → Callout value, set font Segoe UI Semibold, size 30 pt, color #FF0000, and center alignment. <br>
Turn on the Category label and set text to Total Subscribers / Total Views / Watch Time, font size 14 pt, color #333333, alignment center, and position bottom. <br>
Set the background to white with border on (#D9D9D9), corner radius 8, and shadow on. <br>

Duplicate the first card (Ctrl + C → Ctrl + V), change the field to Total Views or Watch Time, and align all cards with Format → Align Top → Distribute Horizontally. <br> <br><br>

## Step 3 – Table (Performance Summary) <br>

Add a Table visual to display detailed metrics. <br>
Include the following fields: Date, Videos Published, Total Views, Likes, Comments, Watch Time (hours), and Avg View Duration (min:sec). <br>

Format the table by setting the column headers’ background to #1C1C1C, font color white, and size 12 pt. <br>
Set the values to font Segoe UI, size 12 pt, color #333333. <br>
Add gridlines in #E0E0E0, enable alternating rows with color #FAFAFA, align text left for Date and right for numbers. <br>
Add a title *Video Performance Summary* in color #E50914, font Segoe UI Semibold, size 15 pt. <br>
Set the date format in Column tools → Format → dd/mm/yyyy. <br> <br><br>

## Step 4 – Column Chart (Engagement Metrics) <br>

Create a Clustered Column Chart to display engagement trends. <br>
Set Date as the Axis and Likes, Comments, and Shares as the Values. <br>

Format the chart with the legend on (top center, font 11 pt). <br>
Set the color for Likes to #FF0000, Comments to #2E86DE, and Shares to #A6ACAF. <br>
Use font color #444444 for axes, with size 11 pt, and set the title *Engagement Metrics Over Time* using font Segoe UI Semibold, size 14–16 pt, color #E50914. <br> <br><br>

## Step 5 – Line Chart (Views Over Time) <br>

Insert a Line Chart to show view trends. <br>
Set Date as the X-axis and Total Views as the Y-axis. <br>

Format the line with color #FF0000, width 3 pt, and markers on. <br>
Set both axes to categorical, font color #444444, and add a title *Views Over Time* using font Segoe UI Semibold, size 14–16 pt, color #E50914. <br>

Open the Analytics pane, add an Average line, set its color to #A6ACAF, data label to “Average Views”, font size 11 pt, and alignment center. <br> <br><br>

## Step 6 – Filter (Slicer) <br>

Add a Slicer visual using the Date field. <br>
Change its type to Between to create a date range filter. <br>

In Format visual → Title, set text *Select Date Range*, font Segoe UI Semibold, size 16 pt, color #E50914, and alignment center. <br>
Set background to white, border on, corner radius 8. <br>

Under Values, use font size 12 pt, color #333333. <br>
In the Slider section, set handle size 22 px and color #A6ACAF. <br>

If visuals do not react to the filter, go to Format → Edit interactions and activate the Filter icon on each visual. <br> <br><br>

## Step 7 – Modifying and Polishing <br>

Refine the final layout for visual balance and clarity. <br>
Ensure spacing and alignment are consistent across all elements. <br>
Check color contrast and readability, keeping the dashboard clean and minimal. <br>
Confirm that all visuals respond correctly to the date slicer. <br>
Review labels, units, and titles for accuracy and coherence. <br>
Save the file as **YouTube_Analytics_Dashboard_Final.pbix**. <br>
Optionally, export as PDF via File → Export → PDF. <br> <br><br>
