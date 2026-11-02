<!DOCTYPE html>

<html lang="en">

<head>

&#x20;   <meta charset="UTF-8">

&#x20;   <meta name="viewport" content="width=device-width, initial-scale=1.0">



&#x20;   <title>Student Management System</title>



&#x20;   <style>

&#x20;       \* {

&#x20;           margin: 0;

&#x20;           padding: 0;

&#x20;           box-sizing: border-box;

&#x20;           font-family: Arial, sans-serif;

&#x20;       }



&#x20;       body {

&#x20;           background: #f2f6ff;

&#x20;       }



&#x20;       /\* Header \*/

&#x20;       header {

&#x20;           background: linear-gradient(135deg, #4e73df, #6f42c1);

&#x20;           color: white;

&#x20;           padding: 25px;

&#x20;           text-align: center;

&#x20;       }



&#x20;       header h1 {

&#x20;           margin-bottom: 8px;

&#x20;       }



&#x20;       /\* Container \*/

&#x20;       .container {

&#x20;           width: 90%;

&#x20;           max-width: 1200px;

&#x20;           margin: 30px auto;

&#x20;       }



&#x20;       /\* Cards \*/

&#x20;       .cards {

&#x20;           display: grid;

&#x20;           grid-template-columns: repeat(4, 1fr);

&#x20;           gap: 20px;

&#x20;           margin-bottom: 30px;

&#x20;       }



&#x20;       .card {

&#x20;           background: white;

&#x20;           padding: 25px;

&#x20;           border-radius: 12px;

&#x20;           text-align: center;

&#x20;           box-shadow: 0 4px 12px rgba(0,0,0,0.1);

&#x20;       }



&#x20;       .card h2 {

&#x20;           color: #4e73df;

&#x20;           font-size: 30px;

&#x20;       }



&#x20;       .card p {

&#x20;           margin-top: 8px;

&#x20;           color: #555;

&#x20;       }



&#x20;       /\* Form \*/

&#x20;       .form-section {

&#x20;           background: white;

&#x20;           padding: 25px;

&#x20;           border-radius: 12px;

&#x20;           box-shadow: 0 4px 12px rgba(0,0,0,0.1);

&#x20;           margin-bottom: 30px;

&#x20;       }



&#x20;       .form-section h2 {

&#x20;           margin-bottom: 20px;

&#x20;           color: #333;

&#x20;       }



&#x20;       .form-grid {

&#x20;           display: grid;

&#x20;           grid-template-columns: repeat(3, 1fr);

&#x20;           gap: 15px;

&#x20;       }



&#x20;       input, select {

&#x20;           width: 100%;

&#x20;           padding: 12px;

&#x20;           border: 1px solid #ccc;

&#x20;           border-radius: 7px;

&#x20;           font-size: 15px;

&#x20;       }



&#x20;       input:focus, select:focus {

&#x20;           outline: none;

&#x20;           border-color: #4e73df;

&#x20;       }



&#x20;       button {

&#x20;           border: none;

&#x20;           padding: 12px 20px;

&#x20;           border-radius: 7px;

&#x20;           cursor: pointer;

&#x20;           font-size: 15px;

&#x20;           color: white;

&#x20;       }



&#x20;       .add-btn {

&#x20;           background: #4e73df;

&#x20;           margin-top: 15px;

&#x20;       }



&#x20;       .add-btn:hover {

&#x20;           background: #2e59d9;

&#x20;       }



&#x20;       /\* Student Table \*/

&#x20;       .table-section {

&#x20;           background: white;

&#x20;           padding: 25px;

&#x20;           border-radius: 12px;

&#x20;           box-shadow: 0 4px 12px rgba(0,0,0,0.1);

&#x20;       }



&#x20;       .table-header {

&#x20;           display: flex;

&#x20;           justify-content: space-between;

&#x20;           align-items: center;

&#x20;           margin-bottom: 20px;

&#x20;       }



&#x20;       .table-header h2 {

&#x20;           color: #333;

&#x20;       }



&#x20;       .search {

&#x20;           width: 250px;

&#x20;       }



&#x20;       table {

&#x20;           width: 100%;

&#x20;           border-collapse: collapse;

&#x20;       }



&#x20;       th {

&#x20;           background: #4e73df;

&#x20;           color: white;

&#x20;           padding: 14px;

&#x20;           text-align: left;

&#x20;       }



&#x20;       td {

&#x20;           padding: 13px;

&#x20;           border-bottom: 1px solid #ddd;

&#x20;       }



&#x20;       tr:hover {

&#x20;           background: #f5f7ff;

&#x20;       }



&#x20;       .edit-btn {

&#x20;           background: #f6c23e;

&#x20;           margin-right: 5px;

&#x20;       }



&#x20;       .delete-btn {

&#x20;           background: #e74a3b;

&#x20;       }



&#x20;       .edit-btn:hover {

&#x20;           background: #dda20a;

&#x20;       }



&#x20;       .delete-btn:hover {

&#x20;           background: #c0392b;

&#x20;       }



&#x20;       /\* Footer \*/

&#x20;       footer {

&#x20;           text-align: center;

&#x20;           padding: 20px;

&#x20;           margin-top: 30px;

&#x20;           background: #343a40;

&#x20;           color: white;

&#x20;       }



&#x20;       /\* Responsive \*/

&#x20;       @media(max-width: 800px) {

&#x20;           .cards {

&#x20;               grid-template-columns: repeat(2, 1fr);

&#x20;           }



&#x20;           .form-grid {

&#x20;               grid-template-columns: 1fr;

&#x20;           }



&#x20;           .table-header {

&#x20;               flex-direction: column;

&#x20;               gap: 15px;

&#x20;           }



&#x20;           .search {

&#x20;               width: 100%;

&#x20;           }



&#x20;           table {

&#x20;               font-size: 13px;

&#x20;           }

&#x20;       }



&#x20;       @media(max-width: 500px) {

&#x20;           .cards {

&#x20;               grid-template-columns: 1fr;

&#x20;           }



&#x20;           .container {

&#x20;               width: 95%;

&#x20;           }



&#x20;           table {

&#x20;               display: block;

&#x20;               overflow-x: auto;

&#x20;           }

&#x20;       }

&#x20;   </style>

</head>



<body>



&#x20;   <!-- Header -->

&#x20;   <header>

&#x20;       <h1>Student Management System</h1>

&#x20;       <p>Manage student information easily</p>

&#x20;   </header>





&#x20;   <div class="container">



&#x20;       <!-- Dashboard Cards -->

&#x20;       <div class="cards">



&#x20;           <div class="card">

&#x20;               <h2 id="totalStudents">0</h2>

&#x20;               <p>Total Students</p>

&#x20;           </div>



&#x20;           <div class="card">

&#x20;               <h2 id="maleStudents">0</h2>

&#x20;               <p>Male Students</p>

&#x20;           </div>



&#x20;           <div class="card">

&#x20;               <h2 id="femaleStudents">0</h2>

&#x20;               <p>Female Students</p>

&#x20;           </div>



&#x20;           <div class="card">

&#x20;               <h2 id="departmentCount">0</h2>

&#x20;               <p>Departments</p>

&#x20;           </div>



&#x20;       </div>





&#x20;       <!-- Add Student Form -->

&#x20;       <div class="form-section">



&#x20;           <h2>Add Student</h2>



&#x20;           <div class="form-grid">



&#x20;               <input type="text"

&#x20;                      id="studentName"

&#x20;                      placeholder="Student Name">



&#x20;               <input type="text"

&#x20;                      id="studentId"

&#x20;                      placeholder="Student ID">



&#x20;               <input type="email"

&#x20;                      id="email"

&#x20;                      placeholder="Email">



&#x20;               <input type="number"

&#x20;                      id="age"

&#x20;                      placeholder="Age">



&#x20;               <select id="gender">

&#x20;                   <option value="">Select Gender</option>

&#x20;                   <option value="Male">Male</option>

&#x20;                   <option value="Female">Female</option>

&#x20;               </select>



&#x20;               <select id="department">

&#x20;                   <option value="">Select Department</option>

&#x20;                   <option value="CSE">CSE</option>

&#x20;                   <option value="ECE">ECE</option>

&#x20;                   <option value="EEE">EEE</option>

&#x20;                   <option value="MECH">MECH</option>

&#x20;                   <option value="CIVIL">CIVIL</option>

&#x20;               </select>



&#x20;           </div>



&#x20;           <button class="add-btn" onclick="addStudent()">

&#x20;               Add Student

&#x20;           </button>



&#x20;       </div>





&#x20;       <!-- Student Table -->

&#x20;       <div class="table-section">



&#x20;           <div class="table-header">



&#x20;               <h2>Student Details</h2>



&#x20;               <input

&#x20;                   class="search"

&#x20;                   type="text"

&#x20;                   id="searchInput"

&#x20;                   placeholder="Search student..."

&#x20;                   onkeyup="searchStudent()">



&#x20;           </div>





&#x20;           <table>



&#x20;               <thead>



&#x20;                   <tr>

&#x20;                       <th>S.No</th>

&#x20;                       <th>Student ID</th>

&#x20;                       <th>Name</th>

&#x20;                       <th>Email</th>

&#x20;                       <th>Age</th>

&#x20;                       <th>Gender</th>

&#x20;                       <th>Department</th>

&#x20;                       <th>Action</th>

&#x20;                   </tr>



&#x20;               </thead>



&#x20;               <tbody id="studentTable">



&#x20;               </tbody>



&#x20;           </table>



&#x20;       </div>



&#x20;   </div>





&#x20;   <footer>

&#x20;       <p>© 2026 Student Management System</p>

&#x20;   </footer>





&#x20;   <script>



&#x20;       let students = \[

&#x20;           {

&#x20;               id: "ST101",

&#x20;               name: "Rahul",

&#x20;               email: "rahul@gmail.com",

&#x20;               age: 20,

&#x20;               gender: "Male",

&#x20;               department: "CSE"

&#x20;           },



&#x20;           {

&#x20;               id: "ST102",

&#x20;               name: "Priya",

&#x20;               email: "priya@gmail.com",

&#x20;               age: 21,

&#x20;               gender: "Female",

&#x20;               department: "ECE"

&#x20;           },



&#x20;           {

&#x20;               id: "ST103",

&#x20;               name: "Arjun",

&#x20;               email: "arjun@gmail.com",

&#x20;               age: 20,

&#x20;               gender: "Male",

&#x20;               department: "CSE"

&#x20;           }

&#x20;       ];





&#x20;       // Display Students

&#x20;       function displayStudents(data = students) {



&#x20;           let table = document.getElementById("studentTable");



&#x20;           table.innerHTML = "";



&#x20;           data.forEach((student, index) => {



&#x20;               table.innerHTML += `

&#x20;                   <tr>



&#x20;                       <td>${index + 1}</td>



&#x20;                       <td>${student.id}</td>



&#x20;                       <td>${student.name}</td>



&#x20;                       <td>${student.email}</td>



&#x20;                       <td>${student.age}</td>



&#x20;                       <td>${student.gender}</td>



&#x20;                       <td>${student.department}</td>



&#x20;                       <td>



&#x20;                           <button

&#x20;                               class="edit-btn"

&#x20;                               onclick="editStudent(${index})">

&#x20;                               Edit

&#x20;                           </button>



&#x20;                           <button

&#x20;                               class="delete-btn"

&#x20;                               onclick="deleteStudent(${index})">

&#x20;                               Delete

&#x20;                           </button>



&#x20;                       </td>



&#x20;                   </tr>

&#x20;               `;

&#x20;           });



&#x20;           updateDashboard();

&#x20;       }





&#x20;       // Add Student

&#x20;       function addStudent() {



&#x20;           let name = document.getElementById("studentName").value;

&#x20;           let id = document.getElementById("studentId").value;

&#x20;           let email = document.getElementById("email").value;

&#x20;           let age = document.getElementById("age").value;

&#x20;           let gender = document.getElementById("gender").value;

&#x20;           let department = document.getElementById("department").value;





&#x20;           if (

&#x20;               name === "" ||

&#x20;               id === "" ||

&#x20;               email === "" ||

&#x20;               age === "" ||

&#x20;               gender === "" ||

&#x20;               department === ""

&#x20;           ) {



&#x20;               alert("Please fill all fields");



&#x20;               return;

&#x20;           }





&#x20;           let student = {



&#x20;               id: id,

&#x20;               name: name,

&#x20;               email: email,

&#x20;               age: age,

&#x20;               gender: gender,

&#x20;               department: department



&#x20;           };





&#x20;           students.push(student);



&#x20;           displayStudents();



&#x20;           clearForm();



&#x20;           alert("Student added successfully!");



&#x20;       }





&#x20;       // Delete Student

&#x20;       function deleteStudent(index) {



&#x20;           if (confirm("Are you sure you want to delete this student?")) {



&#x20;               students.splice(index, 1);



&#x20;               displayStudents();



&#x20;           }



&#x20;       }





&#x20;       // Edit Student

&#x20;       function editStudent(index) {



&#x20;           let student = students\[index];



&#x20;           document.getElementById("studentName").value = student.name;

&#x20;           document.getElementById("studentId").value = student.id;

&#x20;           document.getElementById("email").value = student.email;

&#x20;           document.getElementById("age").value = student.age;

&#x20;           document.getElementById("gender").value = student.gender;

&#x20;           document.getElementById("department").value = student.department;





&#x20;           students.splice(index, 1);



&#x20;           displayStudents();



&#x20;       }





&#x20;       // Clear Form

&#x20;       function clearForm() {



&#x20;           document.getElementById("studentName").value = "";

&#x20;           document.getElementById("studentId").value = "";

&#x20;           document.getElementById("email").value = "";

&#x20;           document.getElementById("age").value = "";

&#x20;           document.getElementById("gender").value = "";

&#x20;           document.getElementById("department").value = "";



&#x20;       }





&#x20;       // Search Student

&#x20;       function searchStudent() {



&#x20;           let search =

&#x20;               document

&#x20;               .getElementById("searchInput")

&#x20;               .value

&#x20;               .toLowerCase();





&#x20;           let filteredStudents = students.filter(student =>



&#x20;               student.name.toLowerCase().includes(search) ||



&#x20;               student.id.toLowerCase().includes(search) ||



&#x20;               student.department.toLowerCase().includes(search)



&#x20;           );





&#x20;           displayStudents(filteredStudents);



&#x20;       }





&#x20;       // Dashboard

&#x20;       function updateDashboard() {



&#x20;           document.getElementById("totalStudents").innerText =

&#x20;               students.length;





&#x20;           document.getElementById("maleStudents").innerText =

&#x20;               students.filter(student =>

&#x20;                   student.gender === "Male"

&#x20;               ).length;





&#x20;           document.getElementById("femaleStudents").innerText =

&#x20;               students.filter(student =>

&#x20;                   student.gender === "Female"

&#x20;               ).length;





&#x20;           let departments = new Set(

&#x20;               students.map(student =>

&#x20;                   student.department

&#x20;               )

&#x20;           );





&#x20;           document.getElementById("departmentCount").innerText =

&#x20;               departments.size;



&#x20;       }





&#x20;       // Initial Display

&#x20;       displayStudents();



&#x20;   </script>



</body>

</html>

