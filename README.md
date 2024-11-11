# Blood-Bridge

## DB Setup
CREATE DATABASE bloodbridge;

USE bloodbridge;


CREATE USER 'DBAdmin'@'localhost' IDENTIFIED BY 'bloodbridge';

GRANT SELECT, INSERT, UPDATE, DELETE ON bloodbridge.* TO 'DBAdmin'@'localhost';

FLUSH PRIVILEGES;


CREATE TABLE register (
         id INT AUTO_INCREMENT PRIMARY KEY,
         fullname VARCHAR(255) NOT NULL,
         email VARCHAR(255) NOT NULL UNIQUE,
         password VARCHAR(255) NOT NULL,
         blood_type VARCHAR(10)
     );

CREATE TABLE request (
         id INT AUTO_INCREMENT PRIMARY KEY,
         requester_id INT NOT NULL,
         location VARCHAR(255) NOT NULL,
         blood_type VARCHAR(10) NOT NULL,
         urgency VARCHAR(50),
         date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
         status VARCHAR(50) DEFAULT 'pending',
         FOREIGN KEY (requester_id) REFERENCES register(id) ON DELETE CASCADE
     );


## Bloodbridge Video



https://github.com/user-attachments/assets/3a54a005-eda0-4f11-8a0b-a8728f193330




https://github.com/user-attachments/assets/483495c7-9465-45dc-a019-e94778f4255d



https://github.com/user-attachments/assets/64eff317-3c6d-4888-861f-ba7d2cf1466a



https://github.com/user-attachments/assets/fca7978b-32e7-4b94-8cb4-8992e58634b9



## Youtube Link

https://youtu.be/74udJuHHb6g
