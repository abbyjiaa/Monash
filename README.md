# Monash MADA Project

The code document purposes for analysing the data of MADA. The codes mainly used for step-by-step data cleaning.

## Description
 For data cleaning, it contains several steps:
   *  Auto fill the NA(blank) cell by extracting the last row value - used for the contents of columns are text 
   eg: University Name，Course name, type of applicants
 
 
 -----------------------------------  
 (Original table)
 University         |  Couse Name                             
 ------------------ | -------------                        
 Monash University  | Art                                            
 (blank)            | Design                                    
 (blank)            | Architecture                 
 (blank)            | Marketing                                    
Deakin University   | Business   
-----------------------------------  
                
                  

-----------------------------------
(New table)
University         |  Couse Name  
------------------ | -------------
Monash University  | Art
Monash University  | Design
Monash University  | Architecture  
Monash University  | Marketing  
Deakin University  | Business  
-----------------------------------  
 
  
  
   *  Replace the NA value into 0  - used for the contents of columns are number 
   eg: Number of applicants, number of offer, number of enrollment
   
   *  Insert the perference as an order from 1 to 8

   ----------------------------------------- 
   (Original table)
   Applicants type    |  Preference order                             
   ------------------ | -------------------                          
   Current Y12        | 1st pref                                         
   Current Y12        | 2nd pref                                        
   Current Y12        | 4th pref                                    
   Current Y12        | 6th pref                                           
   Current Y12        | 7th pref                                                                                                                                                 
  ----------------------------------- ------                        
  Lack of preference order in 3th，5th，8th
  

 --------------------------------------
 (New table)
  Applicants type   |  Preference order
 ------------------ | ----------------- 
  Current Y12       | 1st pref  
  Current Y12       | 2nd pref
  Current Y12       | 3rd pref
  Current Y12       | 4th pref
  Current Y12       | 5th pref
  Current Y12       | 6th pref
  Current Y12       | 7th pref 
  Current Y12       | 8th pref
 -----------------------------------
 
 
 
   * select first three preference order


   * Calculate the sum of applicant from 1-3 preference order
