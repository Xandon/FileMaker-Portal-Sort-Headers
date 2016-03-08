# FileMaker-Portal-Sort-Headers
Portal Sort Header Object for FileMaker

The intent of this module is to provide a set of button bars that can be placed on any layout and controlled via global variables ( or global fields ). They display sort ascending, sort descending, and unsorted icons. The names that appear and the fields they sort on are controlled via global variables. 

Due to some constraints in FileMaker, they are preloaded with reference numbers. Those reference numbers link to the array index of the global values that are loaded. There are 12 buttons and they can reference 12 sort headers. The same 12 buttons can be applied to any layout, and you need only change the global values for the layout to change the header name and sort field. If you need more than 12, you can duplicate one and then follow the pattern for changing the button bar settings to be reference number 13 and so on.

# To Install
To implement these headers into a solution you will need these items in the below order:

1. Import Custom functions:
	"#"
	"#Get"

2. Copy these two fields in to each table that is the related table for the portal you will be sorting 
( be sure to set the portal to sort by them ):
	sorter_asc
	sorter_desc

3. Copy/Import Script:
	Set Globals Sort Field

4. Copy the 12 Button Bars into your solution

5. Copy the Global File Settings text objects (in layout mode it is to the right) onto the layout you will be placing the button bars onto.

6. Set the GLOBAL FILE SETTINGS text (in layout mode it is to the right) with the desired values:
	$$FIELD.NAME
	$$FIELD.TOSORT
	$$PORTALS.NAME
    
    
# Credits
The example provided uses a great a technique by Kevin Frank for sorting, you can read about it more on FileMaker Hacks.
http://filemakerhacks.com/2011/04/07/portal-sorting-part-2/
