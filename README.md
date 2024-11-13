# Database-systems

CREATE TABLE CommunityHealthWorkers (
chw_id varchar(10) PRIMARY KEY,
names_n varchar(15) NOT NULL,
email varchar(20) NOT NULL,
contacts int NOT NULL,
date_of_birth date NOT NULL,
status varchar(10) NOT NULL,
start_date date NOT NULL,
supervisor_id varchar(10) NOT NULL,
FOREIGN KEY (supervisor_id) REFERENCES Supervisor(supervisor_id)
);
CREATE TABLE Supervisor (
supervisor_id varchar(10) PRIMARY KEY,
contacts int NOT NULL,
names_n varchar(20) NOT NULL
);

CREATE TABLE Assignment_t (
assignment_id varchar(10) PRIMARY KEY,
assignment_date date NOT NULL,
description varchar(50),
chw_id varchar(10) NOT NULL,
FOREIGN KEY (chw_id) REFERENCES CommunityHealthWorkers(chw_id)
);
