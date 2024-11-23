\-- Setup FitPro Database Schemas

\-- Create members table  
CREATE TABLE members (  
    member\_id INT PRIMARY KEY,  
    name VARCHAR(100)  
);

\-- Create memberships table  
CREATE TABLE memberships (  
    member\_id INT PRIMARY KEY,  
    age INT,  
    gender CHAR(1),  
    membership\_type VARCHAR(20),  
    join\_date DATE,  
    status VARCHAR(20),  
    FOREIGN KEY (member\_id) REFERENCES members(member\_id)  
);

\-- Create visits table  
CREATE TABLE visits (  
    visit\_id INT PRIMARY KEY,  
    member\_id INT,  
    visit\_date DATE,  
    check\_in\_time TIME,  
    check\_out\_time TIME,  
    FOREIGN KEY (member\_id) REFERENCES members(member\_id)  
);

SELECT 'All table created successful\!';  
\-- Schemas Creation END  
