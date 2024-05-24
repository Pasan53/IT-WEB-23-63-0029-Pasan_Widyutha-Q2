Creating a simple  system to manage students' information using ASP.NET and MS SQL Database.


Answers for - 
iv) 
A. Get all the information of all Students.

Query - 

SELECT * FROM Student;

Output - 

StudentId	Name			    City		  courseId
1		Kasun Gamage		    Kandy		      2
2		Daniel Sam 		      Jaffna		    3
3		Hansi Silva		      Colombo		    1
4		Ranidu Heath		    Matara		    3
5		Praneeth Wijesinghe	Kandy		      4
6		Nuwani Herath		    Rathnapura	  1

B. Select student id, name and city from students who are from the ‘Kandy’.

Query -

SELECT StudentId, Name, City FROM Student WHERE City = 'Kandy';

Output - 

StudentId	Name			City
1		Kasun Gamage		Kandy
5		Praneeth Wijesinghe	Kandy


C. Update the City as 'Galle' of the student whose id equals to 4 .

Query -

UPDATE Student SET City = 'Galle' WHERE StudentId = 4;

Output - 

StudentId	Name			City		courseId
4		Ranidu Heath		Matara		3

D. Get all the information of all students with their course names.

Query -

SELECT Student.*, Course.Name AS CourseName
FROM Student
INNER JOIN Course ON Student.CourseId = Course.CourseId;

Output - 


StudentId	Name			    City		    courseId	CourseName
1		Kasun Gamage		    Kandy		      2		    Graphic Design
2		Daniel Sam 		      Jaffna		    3		    Mobile App Development
3		Hansi Silva		      Colombo		    1		    Web Development
4		Ranidu Heath		    Matara		    3		    Mobile App Development
5		Praneeth Wijesinghe	Kandy		      4		    Java
6		Nuwani Herath		    Rathnapura	  1		    Web Development
