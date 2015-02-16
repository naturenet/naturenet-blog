---
title: Excel Methods for Data
author: Jackie Cameron
date: 2015-02-09
template: article.jade
---

##  eBird Questions Pt.2: Answered with a subsection of data in Excel

To prepare for using the whole dataset and testing if my code works, I answered the 20 questions for a subset of the eBird data using Excel for Mac 2011.  To do this, I used the following methods (sometimes in combination):

1. **Sort:**
Go to Data > Sort.  Then select the column and order you would like.  This allowed me to quickly find largest and smallest numbers.

1. **Remove Duplicates:**
Under the data tab, there is an icon called remove duplicates.  Select a column and then click the "remove duplicates" icons to get a simple list of features.

1. **Counting:**
There are multiple ways to count cells in excel based on different factors:
	- Count cells w/numbers: COUNT(valueX:valueY)
	- Count cells w/data: COUNTA(valueX:valueY)
	- Count blank cells: COUNTBLANK(valueX:valueY)
	- Count with exact phrase: COUNTIF(valueX:valueY, “condition”) 
	- Count with string (phrase segment): COUNTIF(valueX:valueY, “*condition *”)

1. **Dragging to Apply Same Equation:**
	- Once you write a question, click on the bottom right corner of the cell and drag down.  This will copy that equation into all following cells.
	- Excel will automatically increment cell numbers in an equation.  If you do not want to increment all cell numbers, you can put money symbols in the cell and number (e.g. D2 --> $D$2).
	- To cite a cell on a different sheet, but the sheet name in single quotes followed by an exclamation before the cell number (e.g. '5000.txt'!D2).
	- For using a cell's content as a condition in the count formula, you need to put the quotes and concatenate the cell number with an & symbol (e.g. COUNTIF(D2:D5000,"" & A2)).  Otherwise, it will search for the string "A2" in the cells.

1. **Length:**
To get a character count, I used the function LEN(valueX).

1. **Delete Blanks:**
To highlight/select all blank space in a column, select that column and go to Edit>Go to...  Click Special, then Blanks, then OK.  If you would like to delete these, right click on a selected space and click Delete.  You can then choose to delete the blank in that column or the whole row.

1. **Merge Columns:**
Make a new row that adds each cell and symbol/space using the concatenate symbol, & (e.g. =A2&"/"&B2).

1. **Split Columns:**
Go to data tab and select "Text to Columns".  Choose "delimited" file type and what character separates the different parts to be split.  

1.  **Combo #1:**
Copy and paste a column of data into a new row, remove the duplicates to get a simplified list, then use a COUNTIF function on the original column with a cell from the simplified chart as the condition, and finally drag the equation down and sort to get the largest or highest count of a feature.

Answers and Methods for Ebird questions:

1. How many total observations?
	- Method: COUNTA for first column
	- Answer: 4999

1. What are the 3 most common birds?
	- Method: Combo#1 for common bird names
	- Answer: Mourning Dove (48), American Robin (38), and European Starling (38)

1. What state has the most observations?
	- Method: Combo #1 for states
	- Answer: Oregon with 523

1. What is the most number of count made by a person in a single observation?
	- Method: Sort data by observation count
	- Answer: 100000

1. How many unique taxonomy ids?
	- Method: Combo #1 for taxonomic order
	- Answer: 913

1. What is the longest common name?
	- Method: Length on simplified common name list
	- Answer: Short-billed/Long-billed Dowitcher (34 characters)

1. Who observed the most birds?  List their first and last name. 
	- Method: Concatenate first and last name then combo #1 on that list
	- Answer: Rich Hoyer - 2799 separate observations

1. How many kinds of hybrid species are there? 
	- Method: COUNTIF with condition "hybrid" on simplified common bird list 
	- Answer: 0

1. What time of year has the most observations?
	- Method: Split Observation Date cell with delimiting factor as "/".  Then COUNTIF to find the most common month.
	- Answer: November & October

1. Which bird was observed in the most number of states/countries?
	- Method: Concatenate bird and state tag, remove duplicates, split cells, and then COUNTIF using simplified bird list.
	- Answer: European Starling and Mourning Dove (13 states)

1. What is the average duration of an observation?
	- Method: =AVERAGE(valueX:valueY)
	- Answer: 596.06766

1. How many bird species have American in their common name?
	- Method: Use simplified bird list and =COUNTIF(valueX:valueY, “*Value *”)
	- Answer: 15

1. What percentage of time do the observers identify a bird's sex?
	- Method: Remove blanks, count times with male or female, and divide that number by total observations.
	- Answer: 10/4999 = .002 = .2%

1. How many different countries?
	- Method: Remove duplicates and COUNTA().
	- Answer: 7

1. Which country has the most number of observers?
	- Method: Combo #1
	- Answer: Brazil

1. Which column has the most number of missing data?
	- Method: COUNTA() for each column
	- Answer: Breeding Bird Atlas Code

1. Which locality type is the most frequent?
	- Method: Combo #1
	- Answer: H (3839)

1. What is the longest trip comment?
	- Method: Length function
	- Answer: 853 characters (comment left out for privacy)

1. What is the highest latitude an observation was taken?
	- Method: Sort on latitude column
	- Answer: 52.86 degrees N in England

1. When was the earliest date and the most recent date?
	- Method: Sort on date column
	- Answer: Earliest (3/2/53) and Most Recent (12/28/04)



