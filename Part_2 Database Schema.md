```
CREATE TABLE Students (
    Student_ID INT PRIMARY KEY,
    Name VARCHAR(100),
    Gender VARCHAR(10),
    Age INT,
    Socioeconomic_Status VARCHAR(50),
    Enrollment_Status VARCHAR(20)
);

CREATE TABLE Schools (
    School_ID INT PRIMARY KEY,
    School_Name VARCHAR(100),
    Location VARCHAR(100),
    Type VARCHAR(50)
);

CREATE TABLE Dropout_Records (
    Record_ID INT PRIMARY KEY,
    Student_ID INT,
    School_ID INT,
    Dropout_Reason VARCHAR(255),
    Dropout_Date DATE,
    FOREIGN KEY (Student_ID) REFERENCES Students(Student_ID),
    FOREIGN KEY (School_ID) REFERENCES Schools(School_ID)
);

CREATE TABLE Demographics (
    Demographic_ID INT PRIMARY KEY,
    Gender VARCHAR(10),
    Socioeconomic_Status VARCHAR(50),
    Region VARCHAR(100)
);

```