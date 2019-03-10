
<html>
<head>
<title>Fancy title</title>
</head>
<link rel="stylesheet" href="bootstrap/css/bootstrap.min.css">
<script src="bootstrap/js/bootstrap.min.js"></script>
<!--<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>-->
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="jquery-3.3.1.min.js"></script>
<body>
<article id="sysinfo"></article>
<article id="cpuinfo"></article>
<article id="meminfo"></article>
<script>
$.ajax({url: "cpuinfo.php",type: "POST", cache: false}).done(function( html ) {
    $("#cpuinfo").append(html);
});
$.ajax({url: "meminfo.php",type: "POST", cache: false}).done(function( html ) {
    $("#meminfo").append(html);
});
$.ajax({url: "sysinfo.php",type: "POST", cache: false}).done(function( html ) {
    $("#sysinfo").append(html);
});
</script>
</body>
</html>