---
title:  "Excel Utilization"
weigt:  1
header:
  teaser: /assets/images/teasers/func.jpg
categories: 
  - functional
tags:
  - testing
---

_Useful Excel Build-in Function_  

**Scenario 1 :**   
![scenario1_1](/assets/images/excel/scenario1_1.png)
![scenario1_2](/assets/images/excel/scenario1_2.png)
**Formula 1 - SUBTOTAL(function_num, ref1)**  
For SUBTOTAL Function, forever use ***101-111*** as function_num

Q1: How many pdf type transactions?  
A1: Two Steps: 1. Filter Type PDF 2. =SUBTOTAL(103，C4:C8)
![scenario1_A1](/assets/images/excel/scenario1_A1.png)
Q2: What is average total process time of word type transactions?  
A2: Two Steps: 1. Filter Type Word 2. =SUBTOTAL(101，D5:D12)
![scenario1_A2](/assets/images/excel/scenario1_A2.png)

**Formula 2 - PERCENTILE.INC(array, k)**  
For PERCENTILE.INC Function, it is used to calculate percentage number

Q3: What is 90% total process time of PDF type transactions?  
A3: Two Steps: 1. Filter Type PDF 2. =PERCENTILE.INC(D4:D8，**0.9**)
![scenario1_A3](/assets/images/excel/scenario1_A3.png)

**Formula 3 - IF(logic_test, value_if_true, value_if_false)**  
For IF Function, logic often includes >,=,>=,<>,<=, and not recommoned complex IF

Q4: If type is PDF & time > 155; Word & time > 165,show fail.  
A4: =IF(C4="PDF",IF(D4>155,"fail","pass"),IF(D4>165,"fail","pass"))
![scenario1_A4](/assets/images/excel/scenario1_A4.png)

**Formula 4 - VLOOKUP(lookup_value, table_array, col_index_num,true/false)**  
For VLOOKUP Function, it is used to find value in one table  
Explanation:
* lookup_value: Find value according to what
* table_arrary: must include loopup_value as the first seclection, and use absolute path
* col_index_num: the value you select exists in which column
* false means accurate, true means approximate

Q5: If I would like to add Type colunm in the second table, but the transactions is not same sequence as table 1,how?    
A5: =VLOOKUP(B19,$B$3:$C$12,2,FALSE)
![scenario1_A5](/assets/images/excel/scenario1_A5.png)

_Pivot Chart_  

**Scenario 2 :**   
![scenario2_1](/assets/images/excel/scenario2_1.png)

Q6: My boss would like to know the current execution status  
A6: Three Steps: 1. Insert Pivot Chart 2. Select table(table no merge,no blank) 3.drag date, planned and actual into section
![scenario2_A6](/assets/images/excel/scenario2_A6.png)

_Power Query_  

Are you tired of copying and pasting? Are you tired of mering sheets manually? If so, Power Query can help  
**Scenario 3 :**   
![scenario3_1](/assets/images/excel/scenario3_1.png)
![scenario3_2](/assets/images/excel/scenario3_2.png)
![scenario3_3](/assets/images/excel/scenario3_3.png)

Q7: How to merge into one table?  
A7: Three Steps: 
1. New Excel->Data->Get data->From File->From Excel Workbook->Staff.xlsx->click sheet->Transform data
![scenario3_3](/assets/images/excel/scenario3_A7_1.png)
2. In Power Query Editor->New Source->File->Excel Workbook->Salry.xlsx
![scenario3_3](/assets/images/excel/scenario3_A7_2.png)
3. Choose Staff.xlsx sheet1->Home->Merge Queries->Merge Queries as new->choose same column(Ctrl+Right Click)->Remove Prefix->Close & Load To
![scenario3_3](/assets/images/excel/scenario3_A7_3.png)
![scenario3_3](/assets/images/excel/scenario3_A7_4.png)
![scenario3_3](/assets/images/excel/scenario3_A7_5.png)

Q8: If LAN ID begins with E, we regard this staff as External Consult, Add a new column to reflect this  
A8: Follow one step
1. ...Merge Queries as new->Add Column->Conditional Column
![scenario3_3](/assets/images/excel/scenario3_A8_1.png)
![scenario3_3](/assets/images/excel/scenario3_A8_2.png)

Q9: Extract first 3 character as test account  
A9: One Step
1. ...Merge Queries as new->Add Column->Choose LAN ID->Duplicate Column->Choose the duplicated one->Home->Extract first 3 char
![scenario3_3](/assets/images/excel/scenario3_A9_1.png)