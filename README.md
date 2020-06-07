# Tugas4-web5
Tugas pemograman web dasardasar 4 yang ke-5 (login)

<?php
session_start();
$user = $_POST["usr"];
$pass = $_POST["pass"];
//==============================
$dbuser = "admin";
$dbpass = "admin";
//==============================
if($user == $dbuser && $pass == $dbpass){
	echo "<script>alert('Sucess');window.location = ('dashboard.php')</script>";
} else {
    if(isset($_SESSION["salah"])){
        $_SESSION["salah"]++;
    } else{
        $_SESSION["salah"] = 1;
    }
    echo "<script>alert('Wrong password or username'); window.location = ('index.php')</script>";
}

Penjelasan :
» Script dibuat dengan php.
» Script menunjukan proses login suatu situs dengan session start ); sebagai permulaan program
» $user dibuat untuk kolom pengguna sedangkan $dbuser adalah input untuk $user
» $pass dibuat untuk kolom password sedangkan $dbpass adalah input untuk $pass
» Jika input atau masukan sesuai maka akan muncul alert "success"
» Jika salah input atau masukan maka akan muncul alert "wrong password or username".
