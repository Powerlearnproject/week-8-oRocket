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


## Sample Data

```
INSERT INTO Students (Student_ID, Name, Gender, Age, Socioeconomic_Status, Enrollment_Status) VALUES
(1, 'John Doe', 'Male', 16, 'Low', 'Dropped Out'),
(2, 'Jane Smith', 'Female', 15, 'Medium', 'Enrolled'),
(3, 'Alice Johnson', 'Female', 17, 'High', 'Dropped Out');

INSERT INTO Schools (School_ID, School_Name, Location, Type) VALUES
(1, 'Central High', 'City Center', 'Public'),
(2, 'Eastside Academy', 'East End', 'Private');

INSERT INTO Dropout_Records (Record_ID, Student_ID, School_ID, Dropout_Reason, Dropout_Date) VALUES
(1, 1, 1, 'Family Issues', '2023-06-15'),
(2, 3, 2, 'Financial Constraints', '2023-07-01');

INSERT INTO Demographics (Demographic_ID, Gender, Socioeconomic_Status, Region) VALUES
(1, 'Male', 'Low', 'Urban'),
(2, 'Female', 'Medium', 'Suburban');

```