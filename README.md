<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0"> Data Information & Management System</title>
<style> body {
 






<title>Hotel
 
font-family: Arial, sans-serif; margin: 0;	padding: 0;
background-color: #f4f4f4;
}
header {
background-color: #4CAF50; color: white;	padding: 15px;
text-align: center;
}
nav {
display: flex;
justify-content: space-around; background-color: #333;
}
nav a {	color: white;
 
padding: 14px 20px; decoration: none;
text-align: center;
 
text-
 
}
 

 
nav a:hover {
background-color: #ddd;
}
 

color: black;
 

 
.container { 20px;
1200px;
margin: 0 auto;
}
.section-title {
 
padding: max-width:
 
background-color: #4CAF50; color: white;
padding: 10px; margin-top: 20px; text-align: center;
}
.card {
background-color: white;
box-shadow: 0 4px 8px rgba(0,0,0,0.1);
 
padding: 20px; align: center;
 
margin: 20px;	text-
 
border-radius: 8px;
}
.input-group {
margin: 10px 0;
}
.input-group label {

 
display: block; bottom: 5px;
}
 
margin-
 
.input-group input, .input-group select, .input-group textarea { width: 100%;	padding: 10px;	border-radius: 5px;
border: 1px solid #ddd;

 
}
.button {
background-color: #4CAF50; color: white;
 
padding: 10px 20px; border: none;
radius: 5px;
 

border-
 
cursor: pointer;
}
.button:hover {
background-color: #45a049;
}
.form-group {
margin-bottom: 15px;
}
label { font-size: 18px; color: #333; display: block;
margin-bottom: 5px;
}
input, textarea {
width: 100%;
padding: 10px;	font-size:
 
16px; #ccc;

}
 
border: 1px solid border-radius: 5px;
box-sizing: border-box;
 
textarea { height: 100px;
}
.submit-btn { width: 100%;
 
 

padding: 12px;
background-color: #4CAF50; color: white;	font-
size: 18px;	border: none; border-radius: 5px;
cursor: pointer;
margin-top: 10px;
}
.submit-btn:hover { background-color: #45a049;
}
table { width: 100%;
border-collapse: collapse; margin: 20px 0;
}
table, th, td {
border: 1px solid #ddd;
}	th, td { padding: 10px;
text-align: left;
}
th {
background-color: #4CAF50; color: white;
}
.search-bar { margin: 20px 0;
}
.search-bar input { width: 100%;	padding: 10px;	font-size: 16px; border: 1px solid #ccc;
border-radius: 5px;
 
 


}
</style>
</head>
<body>
<header>
<h1>Hotel Customer Details for Security Purpose</h1>
</header>

<nav>
<a href="#dashboard">Dashboard</a>
<a href="#input-data">Input Data</a>
<a href="#customer-details">Customer Details</a>
<a href="#admin-view">Super Admin View</a> </nav>

<!-- Dashboard Section -->
<section id="dashboard">
<h2 class="section-title">Dashboard</h2>
<div class="card">
<img src="C:\Users\HEMANTH\Desktop\hotel management.jpg"align="center" width="400" height="200"/>
<p><b>Welcome to the Hotel Nisarga. Customer details for real-time tracking by the Super Admin.</b></p>
</div>
</section>

<div class="container">
<!-- Customer Details Section -->	<section id="customer-reports">
<h2 class="section-title">Add New Customer Details</h2>
<form id="detailsForm">
<div class="input-group">
<label for="customer-name">Customer Name</label>
<input type="text" id="customer-name" placeholder="Enter Customer Name" required>
 
 

</div>
<div class="input-group">
<label for="mobile-no">Mobile Number</label>
<input type="number" id="mobile-no" placeholder="Enter Mobile Number" required>
</div>
<div class="form-group">
<label for="check-in-date">Check-in Date:</label>
<input type="date" id="check-in-date" required>
</div>
<div class="form-group">
<label for="check-out-date">Check-out Date:</label>
<input type="date" id="check-out-date" required>
</div>
<div class="form-group">
<label for="age">Age:</label>
<input type="number" id="age" placeholder="Enter Customer's Age" required>
</div>
<div class="form-group">
<label for="address">Address:</label>
<textarea id="address" placeholder="Enter Customer's Address" required> </textarea>
</div>
<div class="form-group">
<label for="email">Email:</label>
<input type="email" id="email" placeholder="Enter Customer's Email" required>
</div>
<button type="button" class="submit-btn" onclick="addDetails()">Submit Report</button>
</form>

<!-- Search bar for customer details -->
<h2 class="section-title">Search Customer Details</h2>


 
 

<div class="search-bar">
<input type="text" id="searchBar" onkeyup="searchDetails()" placeholder="Search by Customer Name...">
</div>
<!-- Table to display customer details -->
<	h2 class="section-title">Customer Details</h2>
<table id="detailTable">
<thead>
<tr>
<th>Customer Name</th>
<th>Mobile Number</th>



<th>Check-in Date</th>
<th>Check-out Date</th>
<th>Age</th>
<th>Address</th>
<th>Email</th>
</tr>
</thead>
<tbody>
<!-- Customer details will be added here dynamically -->
</tbody>
</table>
</section>
</div>

<!-- Super Admin View Section -->
<section id="admin-view">
 
 

<h2 class="section-title">Super Admin View</h2>
<div class="card">
<img src="C:\Users\HEMANTH\Desktop\hotel.webp" alt="Admin Icon">
<p>The Super Admin can view all hotel data and generate reports for policy formulation and the efficient implementation of security purposes.</p>
</div>
</section>

<footer>
<p style="text-align:center; padding:10px; background-color:#333; color:white;">&copy; 2024 Hotel Data Information & Management System. All rights reserved.</p> </footer>

 
<script>
// Function to add details to the table addDetails() {
 

function
 




var	table	=
 
document.getElementById("detailTable").getElementsByTagName("tbody")[0]; var customerName = document.getElementById("customer-name").value;
var mobileNo = document.getElementById("mobile-no").value;
var checkInDate = document.getElementById("check-in-date").value; var checkOutDate = document.getElementById("check-out-date").value; var age = document.getElementById("age").value; var address =
document.getElementById("address").value; var email = document.getElementById("email").value
// Insert new row
var newRow = table.insertRow();
newRow.insertCell(0).innerHTML = customerName; newRow.insertCell(1).innerHTML = mobileNo; newRow.insertCell(2).innerHTML = checkInDate;
newRow.insertCell(3).innerHTML = checkOutDate; newRow.insertCell(4).innerHTML = age;
 

 
newRow.insertCell(5).innerHTML = address; newRow.insertCell(6).innerHTML = email;
// Clear form after submission document.getElementById("detailForm").reset();
}

// Function to search reports by costmuer name function searchDetails() {
var input = document.getElementById("searchBar").value.toUpperCase();	var table = document.getElementById("detailTable");	var tr = table.getElementsByTagName("tr");

for (var i = 1; i < tr.length; i++) {
var td = tr[i].getElementsByTagName("td")[0]; // Get first column (costmuer Name)
if (td) {
var txtValue = td.textContent || td.innerText;

 
if (txtValue.toUpperCase().indexOf(input) > -1) {
} else {
tr[i].style.display = "none";
}
}
}
}
</script>
</body>
</html>
 
