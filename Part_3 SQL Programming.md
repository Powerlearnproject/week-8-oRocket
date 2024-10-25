# Part 3: SQL Programming
## Data Retrieval:
1. **Retrieve all students and their enrollment status:**
    ```
    SELECT * FROM Students;
    ```

2. **Get dropout rates by gender:**
    ```
    SELECT Gender, COUNT(*) AS Dropout_Count 
    FROM Students 
    WHERE Enrollment_Status = 'Dropped Out' 
    GROUP BY Gender;
    ```
## Data Analysis:

1. **Analyze reasons for dropout:**
    ```
    SELECT Dropout_Reason, COUNT(*) AS Reason_Count 
    FROM Dropout_Records 
    GROUP BY Dropout_Reason;
    ```