# FileMaker-Portal-Sort-Headers
Portal Sort Header Object for FileMaker

The intent of this module is to provide a set of button bars that can be placed on any layout and controlled via global variables ( or global fields ). They display sort ascending, sort descending, and unsorted icons. The names that appear and the fields they sort on are controlled via global variables. 

Due to some constraints in FileMaker, they are preloaded with reference numbers. Those reference numbers link to the array index of the global values that are loaded. There are 20 buttons and they can reference 20 sort headers. The same 20 buttons can be applied to any layout, and you need only change the global values for the layout to change the header name and sort field. If you need more than 20, you can duplicate one and then follow the pattern for changing the button bar settings to be reference number 21 and so on.

# To Install
To implement these headers into a solution you will need these items in the below order:

1. Import Custom functions to the interface file:
	"#"
	"#Get"

2. Copy these two fields in to each data table that is the related table for the portal you will be sorting
	sorter_asc
	sorter_desc

3. Set the portal sort values *
	sorter_asc (as ascending)
	sorter_desc (as descending)

4. Copy/Import Script:
	Set Globals Sort Field

5. Copy the 20 Button Bars into your solution

6. Copy the "global text calculation" object (in layout mode it is the red text box) onto the layout where you will be placing the button bars.

7. Set the GLOBAL FILE SETTINGS hide calculation (in layout mode, it is on the page and is a let statement in the hide ) with the desired values **:
	$$FIELD.NAME
	$$FIELD.TOSORT
	$$PORTALS.NAME

*  Optional: For sorting a list view (instead of a portal) look at the commented out text in the "Set Global Sort Field" script
** Optional: you could also set the globals in a script instead of referencing them from the object, but the script will need to be run before the layout displays.
    
    
# Credits
The example provided uses a great a technique by Kevin Frank for sorting, you can read about it more on FileMaker Hacks.
http://filemakerhacks.com/2011/04/07/portal-sorting-part-2/

For the multifile or data separated example:
https://github.com/Xandon/FileMaker-Portal-Sort-Headers-Multifile
