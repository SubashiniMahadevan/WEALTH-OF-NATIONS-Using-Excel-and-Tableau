# WEALTH-OF-NATIONS


## Overview
This project focuses on analyzing the Wealth of Nations dataset to gain insights into global economic indicators. The dataset includes data on Life Expectancy, GDP, and Smartphone Ownership for countries around the world. The dataset was cleaned, filtered, and sorted using Excel, and then visualized on Tableau. The analysis is centered around the top 20 highest ranking countries in terms of economic indicators.

## Dataset
The Wealth of Nations dataset contains various economic indicators for countries around the world, including Life Expectancy, GDP, and Smartphone Ownership.



## Data Cleaning and Preparation
The dataset was cleaned, filtered, and sorted using Excel to ensure data consistency and quality. Missing values were handled, duplicates were removed, and the data was sorted according to the client's requirements.

## Visualization
Various visualizations were created using Tableau to represent the economic indicators for the top 20 highest ranking countries.

### Dashboards
Two dashboards were created to provide interactive visualizations of the economic indicators:

1. **Global Economic Overview Dashboard**: This dashboard provides an overview of key economic indicators, including GDP, Life Expectancy, and Smartphone Ownership, for the top 20 highest ranking countries.
2. **Country Comparison Dashboard**: This dashboard allows users to compare economic indicators between different countries using line charts, bubble charts, tree maps, pie charts, and maps.

### Visuals
Several types of visualizations were created to represent the economic indicators:

1. **Line Chart**: Visualizing trends in GDP over time and Smartphone users for the top 20 countries.
2. **Bubble Chart**: Comparing Life Expectancy, GDP for the top 20 countries.
3. **Tree Map**: Displaying Life Expectancy by country for the top 20 countries.
4. **Pie Chart**: Showing the distribution of GDP for the top 20 countries.
5. **Map**: Geospatial representation of GDP distribution across countries for the top 20 countries.

## Accessibility
All visualizations and dashboards were designed with accessibility in mind, taking into account the client's color blindness.

## Conclusion
Through data cleaning, preparation, and visualization, this project provides valuable insights into the economic performance of the top 20 highest ranking countries. The interactive dashboards and visualizations offer intuitive representations of key economic indicators, enabling stakeholders to explore and analyze the data effectively.

##TASK -1 


**EXCEL**

1.Set a password to protect the workbook

2.Highlight column C and change the data to display in British Pound symbol

3.Turn the GDP sheet into a table.

4.Filter the table to display only the information for 2019

5.Next create a chart that will only display the following data ‘Rank, Country and GDP - per capita (PPP). The chart can be anything as long as it is suitable.

6.Using your creative skills edit the chart

a.Add a title

b.Add X and Y axis labels

c.Make the chart visually pleasing

7.Move the chart to a new sheet tab and label with a suitable name

8.Create a sort for the top 20 highest ranking counties

9.Next create a new Bar chart to display the 20 highest ranking countries from your sort and then move the chart to be underneath the table, as shown below.

10.Colour the background by highlighting the area underneath the table as shown below. Find the add a fill colour icon and sellect a colour.

Password Protection 

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/6b802ed7-e96e-49a0-b29c-1d38eb0813bb)

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/1a5d8893-582c-45cc-8475-3882da894234)

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/bc967bcc-f82b-4231-b035-2f2724135b25)

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/c2115e97-babc-4fd9-a512-4b612fa48bcb)

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/c7eb75c1-7ca0-4c32-968b-9385b718c74a)








![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/a0882de0-1571-4a11-899d-afd046ff2373)

**Macro creation for copy, save and Print**

1.The next task is to create 3 macro buttons, print the sheet, Save the file and Copy the sheet.

2.To copy the sheet in a macro you hightlight the area to be copyed then right click copy then stop the macro. Next asign the macro to the copy button. 

2.Using the copy macro, copy the sheet and then paste it into a new word document keeping the formating. 

Give the page a title ‘GDP (Gross domestic product)’.

3.Save your document as ‘Word Gross domestic product report 1'

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/b9d2ccc8-854d-4891-8d89-e718e11de985)

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/689e3014-8ddd-41fb-8e12-e775ee5cdaf5)


![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/1c380af6-995e-403b-8994-8fd70d82ea27)

**VBA Code For Macros:**

**Copy Macros:**

Sub copy_2()
'
' copy_2 Macro
'
Dim wb As Excel.Workbook

Dim ws As Excel.Worksheet

Dim wdapp As Object

Dim wddoc As Object

Set wb = ActiveWorkbook

Set ws = wb.Sheets("GDP")

 If ws Is Nothing Then
 
        MsgBox "Worksheet 'GDP' not found in the workbook."
        
        Exit Sub
        
    End If
    
ws.Range("A1:D21").Copy

End Sub

**Save macros:**

Sub Macro3()

Dim wdapp As Object

Dim wddoc As Object

On Error Resume Next

Set wdapp = GetObject(, "Word.Application")

If Err.Number <> 0 Then

    MsgBox "Error: " & Err.Description
    
    ' Handle the error as needed
    
End If

On Error GoTo 0

wdapp.Visible = True

Set wddoc = wdapp.Documents.Open("C:\Users\subab\OneDrive\justIT\Assignments\Assignment 1\Excel Gross domestic product report 1.docx", ReadOnly:=False)
   
wdapp.Selection.TypeText "GDP (Gross domestic product)" & vbCrLf & vbCrLf ' Adjust the title as needed

'wddoc.Range.PasteExcelTable LinkedToExcel:=False, WordFormatting:=False, RTF:=False

wdapp.Selection.PasteSpecial DataType:=wdPasteText

wddoc.Save

wddoc.Close

' Clean up

Set wdapp = Nothing

Set wddoc = Nothing

Set ws = Nothing

Set wb = Nothing

End Sub


**TABLEAU**

1)Import data

2)Set relationships:

You have three sheets and the common column for all of them is country, so the visual arrangement  of the sheets does not matter Only the columns that you use to create the relationship matters. You can arrange the sheets in a straight line as seen below: 

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/bec882e1-539f-40db-9afb-ad1f702caa1d)

3)Check data types.

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/59ac7b88-2d69-4b68-ab1f-c9774a009725)


4)Build charts

5)As you create your charts, if you see a little gray box containing a count of null values, select the filter option.


![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/04c8d35b-2e00-4ae2-9645-3cf04e801382)

Sorting:

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/cb121a8b-9414-43b0-8da2-7f9ed2c853ab)

Editing Axis 

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/b57761a0-2ed3-4b8a-a59f-08a8171c2398)


6)Build your dashboard.


[Link For Dashboard1](https://public.tableau.com/app/profile/subashini.mahadevan/viz/Assignment_17096639275850/Dashboard1?publish=yes)

**Dashboard1:**

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/da3b71e5-ffc3-4b16-8293-aaf50354e77d)


[Link for Dashboard2](https://public.tableau.com/app/profile/subashini.mahadevan/viz/Assignment_17096639275850/Dashboard2)

**Dashboard 2:**

![image](https://github.com/SubashiniMahadevan/WEALTH-OF-NATIONS-Using-Excel-and-Tableau/assets/168095179/7a499418-a34e-4cfb-83b3-15805730c80b)



📊🌍💼📱
