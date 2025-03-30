
# AWS RDS Testing - Employee Data Viewer

This is a Java-based desktop application that connects to an **AWS RDS MySQL database** to retrieve and display employee data in a **Swing JTable** interface. The application allows users to view employee information and provides details like ID, last name, first name, and city when selecting a row in the table.

## Features

- **Connects to AWS RDS MySQL Database** to retrieve employee data.
- **Displays employee data** in a table with columns for ID, Last Name, First Name, and City.
- **Row Selection** functionality that displays detailed information about the selected employee.
- **Efficient data handling** with real-time updates when selecting rows.

## Technologies Used

- **Java** (Swing for GUI)
- **JDBC** (MySQL Connector)
- **AWS RDS** (MySQL Database)
- **SQL** (Queries to fetch employee data)

## Prerequisites

Before running the application, ensure that you have the following installed:

- **Java JDK** (Version 8 or later)
- **MySQL JDBC Driver** (for connecting to MySQL)
- **MySQL Database** hosted on **AWS RDS**

## Setting Up

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Hamzapatel01/AWS_Homework.git
   cd AWS_Homework
   ```

2. **Configure Database Connection:**

   Open the `HomeWork2.java` file and update the following lines with your database credentials:

   ```java
   Connection con=DriverManager.getConnection("jdbc:mysql://itclub.cgofsekjc56k.us-east-1.rds.amazonaws.com:3306/WrightDB", "HamzaPatel01", "PASSWORD");
   ```

   - Replace `PASSWORD` with your actual database password.
   - You can also change the `WrightDB` database name if needed.

3. **Build and Run the Application:**

   If using **IDE** (like IntelliJ or Eclipse):
   - Import the project and run the `HomeWork2.java` file.

   If running from the command line:
   - Compile the Java file:

     ```bash
     javac HomeWork2.java
     ```

   - Run the application:

     ```bash
     java HomeWork2
     ```

## Usage

- Upon running the application, a window will appear with a table displaying employee data from the AWS RDS MySQL database.
- You can **select a row** to view detailed information about that specific employee (ID, Last Name, First Name, City).
- A dialog box will pop up with the selected employee's data when you click on any row.

## Screenshots

![image](https://github.com/user-attachments/assets/e894e8d3-114e-48c3-80fc-8008907e251c)


## Troubleshooting

- **Error: Connection failure to AWS RDS**  
  - Ensure that your AWS RDS instance is accessible and that your security groups allow connections from your IP address.

- **Error: JDBC Driver not found**  
  - Make sure that the **MySQL JDBC driver** (`mysql-connector-java`) is added to the project's classpath.

## Future goals

- Add the ability to edit or delete employee records directly from the application.
- Improve the user interface by adding search functionality to filter employee data.
- Implement pagination for handling large datasets more efficiently.

## License

This project is licensed under the MIT License.
