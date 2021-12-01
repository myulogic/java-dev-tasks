# Java Developer Tasks
Please create the following two Spring Boot Applications –
## Task 1
Create Spring Boot Application to take local file path of the provided sample Excel file (like "C:\Users\GKalyan\Documents\sample.xlsx") as argument and do the following -

1. Parse/extract data from the two worksheets in the Excel file

2. Load parsed/extracted data (like Sheet name, Column header, the number values, etc.,) into any NoSQL DB (preferable MongoDB) such that the result needed in the second task is possible

3. Handle error scenarios like file missing in the path, Parser exceptions (non-numeric characters in number columns), etc., with an appropriate error response with proper logging in a log file

## Task 2
Create a Spring Boot Application that takes the Excel workbook filename ("sample.xlsx") as an argument and does the following -

1. Group by Sheet name and Column header

2. Calculate the SUM and AVG of the numbers under each column

3. Write result in a text file as per the output example given below

4. Handle error scenarios like Excel workbook data not found, MongoDB exceptions, etc., with an appropriate error response with proper logging in a log file

### Text file output

    [
       {
          "sheet":"Sheet1",
          "data":[
             {
                "column":"ABC",
                "sum":8584,
                "avg":232
             },
             {
                "column":"DEF",
                "sum":67779556,
                "avg":651726.5
             }
          ]
       },
       {
          "sheet":"Sheet2",
          "data":[
             {
                "column":"GHI",
                "sum":92361994,
                "avg":205706
             },
             {
                "column":"JKL",
                "sum":11907929,
                "avg":26521
             }
          ]
       }
    ]

## Bonus Points

 - Perform Excel data parsing/extraction using [SAX](https://docs.oracle.com/javase/tutorial/jaxp/sax/parsing.html) technique
 - Use Apache Spark to generate the result
 - Deploy the two Spring Boot Applications as microservices in a local Docker Swarm