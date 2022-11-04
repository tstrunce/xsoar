*Mock Incident*

<?php
session_start();
$email=$_POST['email'];
$number=rand();
$message="Hello ,"."\n"."This is the password retrieval request, please click on following given link to retrieve the password\n"."http://demos.koding.info/resetpassword/resetpassword.php?id=".$number."\n\nRegards,\nKoding.info";
$_SESSION['resetid']=$number;
mail($email,"Password",$message,"From: tstrunce");
echo '<h3>The password is sent to your email at '.$email.' Please Do check spam folder as well >:)';
?>
