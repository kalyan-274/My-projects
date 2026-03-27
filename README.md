<!DOCTYPE html>
<html>
<head>
<title>Simple Login Page</title>

<style>
body{
font-family: Arial, sans-serif;
background: linear-gradient(120deg,#2980b9,#6dd5fa);
height:100vh;
display:flex;
justify-content:center;
align-items:center;
}

.login-box{
background:white;
padding:30px;
border-radius:10px;
width:300px;
text-align:center;
box-shadow: 10px;
box-shadow:0 0 40px rgba(0,0,0,0.3);
}

input{
width:90%;
padding:10px;
margin:10px 0;
border:1px solid #ccc;
border-radius:5px;
}

button{
background:#2980b9;
color:white;
border:none;
padding:10px;
width:95%;
border-radius:5px;
cursor:pointer;
}

button:hover{
background:#1f6391;
}

#message{
color:red;
font-size:14px;
}
</style>

</head>

<body>

<div class="login-box">
<h2>Login</h2>

<form onsubmit="return validateLogin()">

<input type="text" id="username" placeholder="Username" required>

<input type="password" id="password" placeholder="Password" required>

<button type="submit">Login</button>

<p id="message"></p>

</form>
</div>

<script>

function validateLogin(){

var user=document.getElementById("username").value;
var pass=document.getElementById("password").value;

if(user==="admin" && pass==="1234"){
alert("Login Successful");
return true;
}
else{
document.getElementById("message").innerHTML="Invalid Username or Password";
return false;
}

}

</script>

</body>
</html>