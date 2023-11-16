#include <iostream>
#include <string>

Using namespace std;

Class Course {
Private:
    String course Name;
    String* students;
    Int numStudents;
    Int maxStudents;

Public:
    // Constructor
    Course(const string& name, int max) : courseName(name), numStudents(0), maxStudents(max) {
        Students = new string[maxStudents];
    }

    // Deep copy constructor
    Course(const Course& other) : courseName(other.courseName), numStudents(other.numStudents), maxStudents(other.maxStudents) {
        Students = new string[maxStudents];
        For (int I = 0; I < numStudents; ++i) {
            Students[i] = other.students[i];
        }
    }
// https://github.com/Laibasatti55/drop-student.git

    // Destructor
    ~Course() {
        Delete[] students;
    }

    // Function to get the course name
    String getCourseName() const {
        Return courseName;
    }

    // Function to add a new student
    Void addStudent(const string& studentName) {
        If (numStudents < maxStudents) {
            Students[numStudents] = studentName;
            ++numStudents;
        } else {
            Cout << “Course is full. Cannot add more students.” << endl;
        }
    }

    // Function to drop a student
    Void dropStudent(const string& studentName) {
        For (int I = 0; I < numStudents; ++i) {
            If (students[i] == studentName) {
                // Shift remaining elements to fill the gap
                For (int j = I; j < numStudents – 1; ++j) {
                    Students[j] = students[j + 1];
                }
                --numStudents;
                Return; // Student found and dropped
            }
        }
        Cout << “Student not found in the course.” << endl;
    }

    // Function to get the array of students
    Const string* getStudents() const {
        Return students;
    }

    // Function to get the number of students
    Int getNumStudents() const {
        Return numStudents;
    }
};

Int main() {
    // Example usage in the main function
    Course course1(“Math”, 3);
    Course1.addStudent(“Alice”);
    Course1.addStudent(“Bob”);

    // Deep copy using copy constructor
    Course course2 = course1;

    // Drop a student from course2
    Course2.dropStudent(“Alice”);

    // Output course names and students
    Cout << “Course 1: “ << course1.getCourseName() << endl;
    Cout << “Students in Course 1: “;
    For (int I = 0; I < course1.getNumStudents(); ++i) {
        Cout << course1.getStudents()[i] << “ “;
    }
    Cout << endl;

    Cout << “Course 2: “ << course2.getCourseName() << endl;
    Cout << “Students in Course 2: “;
    For (int I = 0; I < course2.getNumStudents(); ++i) {
        Cout << course2.getStudents()[i] << “ “;
    }
    Cout << endl;

    Return 0;
}

