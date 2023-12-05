# lab_p41_bd
mkdir lab_p41
cd lab_p41
sqlite3 lab_p41_bd
CREATE TABLE mosfet(id INTEGER PRIMARY KEY NOT NULL, quantity INTEGER, max_Uce FLOAT, max_Ube FLOAT, max_Ice Float, name VARCHAR(20), type VARCHAR(2));
INSERT INTO mosfet(id, quantity, max_Uce, max_Ube, max_Ice, name, type) VALUES(101, 43, 50, 20 ,8 ,'IRF840PBF', 'N');
INSERT INTO mosfet(id, quantity, max_Uce, max_Ube, max_Ice, name, type) VALUES(102, 25, 55, 20, 110,'IRF3205PBF', 'N');
INSERT INTO mosfet(id, quantity, max_Uce, max_Ube, max_Ice, name, type) VALUES(103, 64, 60, 20, 50, 'IRFZ44NPBF', 'N');
INSERT INTO mosfet(id, quantity, max_Uce, max_Ube, max_Ice, name, type) VALUES(104, 32, 200, 20, 18, 'IRF640NPBF', 'N');
INSERT INTO mosfet(id, quantity, max_Uce, max_Ube, max_Ice, name, type) VALUES(105, 21, 20, 0.2, 21,'2N7000', 'N');
INSERT INTO mosfet(id, quantity, max_Uce, max_Ube, max_Ice, name, type) VALUES(106, 30, 40, 20, 15, 'LKJ483PO', 'P');
SELECT * FROM mosfet;
SELECT * FROM mosfet ORDER BY quantity;
SELECT * FROM mosfet ORDER BY quantity DESC;
SELECT id, name FROM mosfet where type = 'N';
SELECT id, name, max_Ice FROM mosfet WHERE max_Ice >= 10 and max_Ice <=20 ORDER BY name;
INSERT INTO mosfet(id, quantity, max_Uce, max_Ube, max_Ice, name, type) VALUES(107, 47, 60, 15, 30, 'KOP5782IJ', 'P');
UPDATE mosfet SET type = 'P' WHERE id = 102;
SELECT max_Ube, COUNT(*) FROM mosfet GROUP BY max_Ube;
SELECT COUNT(*) FROM mosfet;
DELETE FROM mosfet WHERE quantity < 25;
SELECT COUNT(*) FROM mosfet;
.exit
размер файла 8кб
