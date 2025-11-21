[README.txt](https://github.com/user-attachments/files/23683034/README.txt)
#Project Description

ZMM_TABSTRIP_ALV is an SAP ABAP application that provides a two-tab interface for displaying material master data and related purchasing documents. It uses ALV grids within a TabStrip to present data retrieved from MARA, MAKT, MARC, EKKO, and EKPO. The program supports quick navigation to standard SAP transactions (MM03 and ME23N) through double-click actions.

#Features

Search materials by material number with an optional plant filter.

Display material master attributes in an ALV grid.

Display related purchase order items (up to 100 recent entries).

Filter purchasing data to document type NB and exclude deleted items.

Double-click on:

Material number → opens MM03

PO number → opens ME23N

Automatic refresh of both ALVs after a search.



#Technologies

The project is built using standard SAP ABAP and Dynpro technologies. Key components include:

-ABAP Objects (OO)
Used for structuring logic into local classes (lcl_get_mat_data, lcl_event_handler).

-SAP Dynpro (Screens 0100–0102)
Provides the user interface with input fields and a two-tab TabStrip layout.

-TabStrip Control
Used to display Material Data and Purchasing Data on separate subscreens.

-ALV Grid Control (CL_GUI_ALV_GRID)
Used to render interactive tables for material and purchasing data.

-Custom Containers (CL_GUI_CUSTOM_CONTAINER)
Hosts ALV grids inside dynpro screens.

-SQL Select Statements with JOIN
Reads data from MARA, MAKT, MARC, EKKO, and EKPO using SELECT ... INTO CORRESPONDING FIELDS.

-Event Handling
ALV double-click event for navigation to MM03 and ME23N.

-Classic SAP Navigation
CALL TRANSACTION and SET/GET parameters for fast document access.
