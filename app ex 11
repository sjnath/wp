<!DOCTYPE html>
<html >
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Contact Form - PHP/MySQL Demo Code</title>
</head>

<body>

<legend>Contact Form</legend>
<form action="one12.php" method="post" >
<p>
<label for="Name">Name </label>
<input type="text" name="name" id="txtName">
</p>
<p>
<label for="email">password</label>
<input type="text" name="pwd" id="txtEmail">
</p>
<p>
<label for="phone">Confirm passwodd</label>
<input type="text" name="pwd2" id="txtPhone">
</p>
 
<p>
<input type="submit" name="Submit" id="Submit" value="Submit">
</p>
</form>

</body>
</html>

----------------------
php code

<?php

$name= $_POST['name'];
$pwd= $_POST['pwd'];
$pwd2= $_POST['pwd2'];

$servername = "localhost";
$username = "root";
$password = "";
$dbname = "dbase";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);
// Check connection
if ($conn->connect_error) {
  die("Connection failed: " . $conn->connect_error);
}
if($pwd == $pwd2)
{
$sql = "INSERT INTO user VALUES ('$name', '$pwd', '$pwd2')";

if ($conn->query($sql) === TRUE) {
  echo "New record created successfully";
} else {
  echo "Error: " . $sql . "<br>" . $conn->error;
}

$conn->close();
}
else {

echo "Mist matched input";

}
?>
