# Task-1

create the database
create database LibraryDB;
use LibraryDB;



-- Create Authors table
CREATE TABLE Authors (
    AuthorID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(100) NOT NULL,
    Nationality VARCHAR(50)
);

-- create books table
create table books(
bookID int auto_increment primary key,
Title varchar (150) not null,
Genre varchar(50),
publishedYear year,
AuthorID int,

foreign key (AuthorID) references Authors(AuthorID)
);


-- Create Members table
CREATE TABLE Members (
    MemberID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(100),
    Email VARCHAR(100) UNIQUE,
    MembershipDate DATE
);

-- Create Loans table
CREATE TABLE Loans (
    LoanID INT AUTO_INCREMENT PRIMARY KEY,
    BookID INT,
    MemberID INT,
    LoanDate DATE,
    ReturnDate DATE,
    FOREIGN KEY (BookID) REFERENCES Books(BookID),
    FOREIGN KEY (MemberID) REFERENCES Members(MemberID)
);

![IMG-20250623-WA0012](https://github.com/user-attachments/assets/6b1d1588-8e80-43d2-96ca-78b94fda2596)
