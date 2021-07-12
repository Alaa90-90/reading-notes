# Creating tables with HTML
## Introduction
sometimes we want to consider using HTML tables in our website. In addition to creating HTML tables to present data in rows and columns, i can also create HTML tables to organize information on your web page.

The process of creating an HTML table is similar to the process that you used to create your web page and any elements that you may have already included in your page, such as links or frames. Coding HTML tables into your web page is fairly easy since you need only understand a few basic table codes.

## Creating a basic table
The basic structure of an HTML table consists of the following tags:

- Table tags:  <TABLE> </TABLE>
- Row tags:   <TR> </TR>
- Cell tags:    <TD> </TD>

Constructing an HTML table consists of describing the table between the beginning table tag, <TABLE>, and the ending table table tag, </TABLE>. Between these tags, i then construct each row and each cell in the row. To do this, i would first start the row with the beginning row tag, <TR>, and then build the row by creating each cell with the beginning cell tag, <TD>, adding the data for that cell, and then closing the cell with the ending cell tag, </TD>. When you finish all of the cells for a row, you would then close the row with the ending row tag, </TR>.Then, for each new row, you would repeat the process of beginning the row, building each cell in the row, and closing the row.

The following table is an example of a basic table with three rows and two columns of data.

Data 1	Data 2
Data 3	Data 4
Data 5	Data 6
The codes that generated this table look like this:

<TABLE>
   <TR>
      <TD>Data 1</TD>
      <TD>Data 2</TD>
   </TR>
   <TR>
      <TD>Data 3</TD>
      <TD>Data 4</TD>
   </TR>
   <TR>
      <TD>Data 5</TD>
      <TD>Data 6</TD>
   </TR>
</TABLE>

This table contains no border, title, or headings.  If i wish to add any of these elements to your table, i need to include additional HTML codes. 

## Adding a border, title, and headings
In addition to the basic table tags, several options are available for adding additional elements to my table. For example, if i want add a border, title, and column headings to the table in the previous section, the table would then resemble the following:

TABLE TITLE     |
|Column A	|Column B| 
|--------|---------|
|data 1 | data 2|
|data 3| data 4 |
|data 5|data 6|


  


The following codes generated the border, TABLE TITLE, and Column A and Column B headings for this table: 
<TABLE  BORDER="5">
   <TR>
      <TH COLSPAN="2">
         <H3><BR>TABLE TITLE</H3>
      </TH>
   </TR>
      <TH>Column A</TH>
      <TH>Column B</TH>

Note:  If you wish to view the codes that generated the Data 1 through Data 6 cells, refer to the previous section.

Notice that the beginning table tag, <TABLE>, now includes the border tag, BORDER="5", which places a border around the table and frames each cell. The number that you ascribe to the border tag, BORDER=n, sets the width of the table border. Depending on how you design your table, you can then determine the border size that best suits your table and the overall design of your web page.

To add a title to your table, you would place the title and the attributes of that title between the row commands, <TR> and </TR>. The heading codes, <TH> and </TH>, define a heading cell and, by default, these codes center the heading and set it in bold type.  However, if you want the title to span across the columns below it, you need to include the COLSPAN=n code. Since this table has two columns, the COLSPAN="2" code was necessary. To add emphasis to the header, you can use the header commands to make the text larger. In this table, notice that the <H3> and </H3> commands made the title larger. Finally, the <BR> tag created a space above the title.

The individual column headings are also described by the heading codes, <TH> and </TH>. Since these codes, by default, center the heading and set it in bold type, no additional commands or attributes were included in the heading commands.

## Polishing your table
To give your table a more polished look, you can include commands that will adjust the size of your table, add space in the cell, add space between rows, and align the data in a cell. Working with these commands is basically a process of trial and error to create the most appealing presentation of your information. The type of table that you create and the overall design of your web site will help you determine what works best for your table.

Some of the commands that enable you to customize your table include:

- The WIDTH=n% command sets the width of your table as a percentage of the screen.  The letter n designates the percentage that you assign to this command.  For example, if you want the width of your table to be one half the width of the screen, you would include the WIDTH="50%" command in the beginning table command.
- The CELLPADDING=n command adjusts the vertical dimension of the cells.  The letter n designates the numerical value that you assign to this command.
- The CELLSPACING=n command sets the space or border around the cells.  The letter n designates the numerical value that you assign to this command.
- The ALIGN=(LEFT, RIGHT, or CENTER) command will horizontally align the data in a cell.  For example, if you wish to place the data in the center of each cell in a row, you would include the ALIGN=CENTER command within the row command.
- The VALIGN=(TOP, MIDDLE, or BOTTOM) command will vertically align the data in a cell.  For example, if you wish to place the data in the center of each cell in a row, you would include the ALIGN=MIDDLE command within the row command.
In addition to the codes that were explained in the previous sections, the table below now includes some of these commands.

TABLE TITLE
Column A	Column B
Data 1	Data 2
The following codes, along with codes previously discussed, created this table:

<TABLE BORDER="5"    WIDTH="50%"   CELLPADDING="4" CELLSPACING="3">
   <TR>
      <TH COLSPAN="2"><BR><H3>TABLE TITLE</H3>
      </TH>
   </TR>
   <TR>
      <TH>Column A</TH>
      <TH>Column B</TH>
   </TR>
   <TR ALIGN="CENTER">
      <TD>Data 1</TD>
      <TD>Data 2</TD>
   </TR>
</TABLE>

Notice that the TABLE command now includes the WIDTH="50%" command. This command extends the table across one half of the width of the text. Also, the CELLPADDING="4" command increases the vertical dimension of the cells, and the CELLSPACING="3" command increases the border around the cells. Finally, the ALIGN="CENTER" command places Data 1 and Data 2 in the center of the cell.

## Creating links
After you create your table, you can also create a link to another web page in one or more cells.  To do this, you need only include the link commands between the <TD> and </TD> commands. 