# PHP_Test


## Referenciar driver
Apache ---- config --------- init.php ------ pdo 

//Depende versión PHP ---- http://localhost/dashboard/phpinfo.php

extension=php_sqlsrv_82_nts_x64.dll
extension=php_sqlsrv_82_ts_x64.dll
extension=php_pdo_sqlsrv_82_nts_x64.dll
extension=php_pdo_sqlsrv_82_ts_x64.dll


===============
## conexion.php
    <?php

    class Cconexion{

    function ConexionBD(){

    $host='localhost';
    $dbname='dbprueba';
    $username='sserver';
    $password ='root';
    $puerto=1433;

    try{
    $conn = new PDO ("sqlsrv:Server-$host,$puerto;Database-$dbname",$username, $password);
    echo "Se conectó correctamen a la base de datos";
    }
    catch(PDOException $exp){
    echo ("No se logró conectar correctamente con la base de datos: $dbname, error: $exp");
    }
    return $conn;
    }

    ?>


=======================
## index.php

![image](https://github.com/elvisdev0/PHP_Test/assets/57382598/e695536f-b9aa-4ac8-a76e-09405ca14358)

https://chatgpt.com/share/031ccab2-36f3-477a-9fd1-2b2e8ebd9bd7

