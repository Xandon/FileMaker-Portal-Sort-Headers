# FileMaker-Portal-Sort-Headers
Portal Sort Header Object for FileMaker

The intent of this module is to provide a set of button bars that can be placed on any layout and controlled via global fields. They display sort ascending, sort descending, and unsorted. The names that appear are controlled via global variables. The fields they sort on are controlled via global variables. Due to some of Filemakers constraints, they are preloaded with reference to the array index of the global values that are loaded. There are 12 buttons and they can reference 12 sort headers. If you need more, you can duplicate one and then follow the pattern for changing the button bar settings.

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
