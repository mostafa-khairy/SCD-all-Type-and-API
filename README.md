# SCD-all-Type-and-API
# using Informatica Intelligent Cloud Services (IICS) to apply SCD Type 1, 2, 3, and request data from an API

## SCD Type 1 using MD5 Function 

* MD5 Function: Calculates the checksum of the input value.
![image](https://github.com/mostafa-khairy/SCD-all-Type-and-API/assets/87584678/7d19fc67-fb36-414e-9fff-8aaed2b1d140)

## SCD Type 2
* SCD Type 2 SCD Type 2 and there is an additional flag indicating if the row was deleted from the source DB or not, using post-SQL (Update Statment)
![image](https://github.com/mostafa-khairy/SCD-all-Type-and-API/assets/87584678/10b7a539-f5cc-4c49-84d9-2376c141309c)

* another way to apply SCD Type 2 is by using a full outer join and creating an indicator to mark the row as ( insert or upsert ) and if the row in the target was deleted from the source or not

  ![image](https://github.com/mostafa-khairy/SCD-all-Type-and-API/assets/87584678/ea81deac-a9a7-4d76-9860-37623d8df600)

** upsert Flag and handling NULLS in comparison 

  ![image](https://github.com/mostafa-khairy/SCD-all-Type-and-API/assets/87584678/c075d306-e81f-4839-95af-013086a56b96)



## SCD Type 3 
![image](https://github.com/mostafa-khairy/SCD-all-Type-and-API/assets/87584678/d56527dd-ba22-485e-bbe6-7ac5e419cb87)


## Getting data from an open API using Data integration 
using Postman as a test for API 

SITE: "https://aladhan.com/islamic-calendar-api#GetGToHCalendar"

API: http://api.aladhan.com/v1/gToHCalendar/:month/:year

this API takes two parameters as an input month and year and returns the Hijri Calendar for this month
using Java transformation to create nested loop-to-loop for years and months to request data for different months
![image](https://github.com/mostafa-khairy/SCD-all-Type-and-API/assets/87584678/3d83aee0-b448-4d95-b6a1-7bedf9daba42)

Steps :
* create a swagger file then create a connection 
* create a Business Service then create a web Service 
* create a dummy source as an input for mapping




