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



    CREATE TABLE Facturas (
    id INT PRIMARY KEY IDENTITY(1,1),
    fecha DATETIME DEFAULT GETDATE(),
    base_imponible_0 DECIMAL(18, 2),
    base_imponible_12 DECIMAL(18, 2),
    iva DECIMAL(18, 2),
    total DECIMAL(18, 2)
    );

    CREATE TABLE DetallesFactura (
    id INT PRIMARY KEY IDENTITY(1,1),
    factura_id INT FOREIGN KEY REFERENCES Facturas(id),
    descripcion VARCHAR(255),
    cantidad INT,
    precio DECIMAL(18, 2),
    iva_tasa DECIMAL(18, 2)
    );












![image](https://github.com/elvisdev0/PHP_Test/assets/57382598/e695536f-b9aa-4ac8-a76e-09405ca14358)

https://chatgpt.com/share/1e3b74ad-e685-4804-b5fd-b094bc36dea8

https://www.youtube.com/watch?v=K8MJtUmo8nk

inicio / final
