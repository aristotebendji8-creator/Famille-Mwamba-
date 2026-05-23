<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Famille Mwamba</title>

<style>
body{
background:#111;
color:white;
font-family:Arial;
text-align:center;
padding:20px;
}

h1{
color:gold;
}

.container{
background:#222;
padding:20px;
border-radius:15px;
max-width:400px;
margin:auto;
}

input{
width:90%;
padding:12px;
margin:10px;
border:none;
border-radius:10px;
}

button{
padding:12px 20px;
background:gold;
border:none;
border-radius:10px;
font-weight:bold;
cursor:pointer;
}

.profile{
margin-top:20px;
padding:15px;
background:#333;
border-radius:10px;
}

.role{
color:gold;
font-weight:bold;
}
</style>
</head>

<body>

<h1>👑 Famille Mwamba 👑</h1>

<div class="container">

<h2>Créer un compte</h2>

<input type="text" id="name" placeholder="Nom complet">

<input type="text" id="phone" placeholder="Numéro téléphone">

<input type="password" id="password" placeholder="Mot de passe">

<select id="role">
<option>Membre</option>
<option>Leader</option>
<option>Admin</option>
</select>

<br><br>

<button onclick="createAccount()">Créer le compte</button>

<div class="profile" id="profile"></div>

</div>

<script>

function createAccount(){

let name = document.getElementById("name").value;
let phone = document.getElementById("phone").value;
let password = document.getElementById("password").value;
let role = document.getElementById("role").value;

if(name=="" || phone=="" || password==""){
alert("Remplissez tous les champs");
return;
}

document.getElementById("profile").innerHTML = `
<h2>Profil créé ✅</h2>

<p><strong>Nom :</strong> ${name}</p>

<p><strong>Téléphone :</strong> ${phone}</p>

<p class="role">${role}</p>

<p>Créateur : Aristote</p>
`;

}

</script>

</body>
</html>
