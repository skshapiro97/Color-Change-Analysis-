# Color-Analysis
Protocol for collecting average color (RGB) for a region of interest and R code for how to analyze color data

**Uses:** ImageJ software and R programming language

**Purpose:** This protocol and code were developed to track color changes over time for regions of interest (ROIs) by collecting the average RGB values within the ROIs and subsequently visualizing how the RGB values change with time.

**Need/Requirements:** 
- ImageJ (or Fiji) and R coding language
- Images that all contain the same "true white" reference to use for white-balancing (need to be able to white-balance all images to the same thing to not bias color data)
- Images should be taken all using the same device under as similar conditions as possible to avoid any bias

Note: The project this code was created for and is being used for is analyzing color change over time in post-larval lobsters when subjected to different temperatures and UV exposure. Because of this, there is reference to lobsters and lobster anatomy in the protocol.

**PROTOCOL:**
- Step 1: Follow the Lobster Photo ImageJ Protocol for all images to collect color data; when pasting the color data into a spreadsheet, I like to pre-label my columns and rows and separate each ImageJ table by a blank spreadsheet row to keep my data separated and properly labeled, as it can get confusing when collecting data for multiple ROIs on multiple subjects.
- Step 2: Format ImageJ results table data into the correct format
	- When the data is collected for each ROI, it is formatted with the columns being each ROI and rows being the Red average, Green average, and Blue average. In order to make the data more user-friendly for R, it needs to be flipped.
 	- The best way I found to do this is to create a new spreadsheet tab, copy one set of ImageJ result table data (aka only one set of Red average, Green average, and Blue average rows), go into the new spreadsheet tab, right-click, go to Paste Special -> Transposed (this will paste the data in the correct orientation). Repeat for all data.
  - Once the data is in the correct orientation and has the appropriate columns for your data (in this case it's: Date, Lobster, Temp, UV_Treatment, Region, Red, Green, Blue), save it as a .csv file
- Step 3: Follow the R code (developed by Arianna Krinos, 31 July 2024) for formatting the ImageJ data
