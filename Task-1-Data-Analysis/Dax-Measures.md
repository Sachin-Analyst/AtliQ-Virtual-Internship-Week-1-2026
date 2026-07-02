## April

WFH_Status_April = 
CALCULATE(
    COUNT(attendance_data[Date]),
    attendance_data[Month Name]="April",
    attendance_data[Status]="WFH")
    

WFO_Status_April = 
CALCULATE(
    COUNT(attendance_data[Date]),
    attendance_data[Month Name]="April",
    attendance_data[Status]="WFO")

Total_status_April = 
CALCULATE(
    COUNT(attendance_data[Status]),
    attendance_data[Month Name]="April")

Total_present_days_April = [WFH_Status_April]+[WFO_Status_April]
    

WFH_April_% = 
DIVIDE([WFH_Status_April],[Total_present_days_April],0)

---------------

## May

WFO_Status_May = 
CALCULATE(
    COUNT(attendance_data[Date]),
    attendance_data[Month Name]="May",
    attendance_data[Status]="WFO")
    

WFH_Status_May = 
CALCULATE(
    COUNT(attendance_data[Date]),
    attendance_data[Month Name]="May",
    attendance_data[Status]="WFH")
    

Total_status_May = 
CALCULATE(
    COUNT(attendance_data[Status]),
    attendance_data[Month Name]="May")

Total_present_days_May = [WFH_Status_May]+[WFO_Status_May]


WFH_May_% = 
DIVIDE([WFH_Status_May],[Total_present_days_May],0)

---------------

## June

WFO_Status_June = 
CALCULATE(
    COUNT(attendance_data[Date]),
    attendance_data[Month Name]="June",
    attendance_data[Status]="WFO")
    

WFH_Status_June = 
CALCULATE(
    COUNT(attendance_data[Date]),
    attendance_data[Month Name]="June",
    attendance_data[Status]="WFH")
    

Total_status_June = 
CALCULATE(
    COUNT(attendance_data[Status]),
    attendance_data[Month Name]="June")

Total_present_days_June = [WFH_Status_June]+[WFO_Status_June]

Attendance_%_June = 
DIVIDE([Total_present_days_June],[Total_status_June],0)

---------------

## Other Dax measures

Distinct_Employees = 
    COUNTROWS(
             DISTINCT(attendance_data[name])
                )

Distinct_Employees_id = 
    COUNTROWS(
             DISTINCT(attendance_data[employee_id])
                )

Total_Rows = COUNTROWS(attendance_data)

WFH_Employee_count = 
CALCULATE(
    DISTINCTCOUNT(attendance_data[name]),
    FILTER(
        VALUES(attendance_data[name]),
        [WFH_April_%] > 0.10
    )
)
