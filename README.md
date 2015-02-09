//# store
mysql store database//

CREATE TABLE`store`.`CustomerOrders` (
  `idCustomerOrders` INT NOT NULL,
  `Name` VARCHAR(45) NOT NULL,
  `Phone` VARCHAR(45) NOT NULL,
  `email` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`idCustomerOrders`)
  
)
;




CREATE TABLE `store`.`Products` (
  `idProduct` INT NOT NULL ,
  `idManufacturers` INT NULL,
  `Type` DECIMAL(10) NOT NULL,
  `Price` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`idProduct`)
)
;



CREATE TABLE  `store`.`Inventory` (
  `idProduct` INT NOT NULL,
  `idStore` INT NOT NULL,
  `quantity` INT NOT NULL,
  PRIMARY KEY (`idProduct`, `idStore`)
)
;




CREATE TABLE `store`.`Manufacturers` (
    `idManufacturers` INT NOT NULL,
    `Name` VARCHAR(45) NOT NULL,
    PRIMARY KEY (`idManufacturers`)
)
;




CREATE TABLE IF NOT EXISTS `store`.`SoldItems` (
  `idProduct` INT NOT NULL,
  `idSales` INT NOT NULL,
  `quantity` INT NOT NULL,
  PRIMARY KEY (`idProduct`)
)
;


CREATE TABLE  `store`.`Stores` (
  `idStore` INT NOT NULL,
  `Name` VARCHAR(45) NOT NULL,
  `Address` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`idStore`)
)
;


CREATE TABLE `store`.`Suppliers` (
  `idSupplier` INT NOT NULL,
  `Name` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`idSupplier`)
)
;


CREATE TABLE `store`.`Sales` (
  `idSales` INT NOT NULL,
  `idCustomer` INT NOT NULL,
  `idStore` INT NOT NULL,
  `date` DATETIME NOT NULL,
  `totalSale` DECIMAL(30) NOT NULL,
  PRIMARY KEY (`idSales`)
)
;


