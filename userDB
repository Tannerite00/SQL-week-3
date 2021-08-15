create database if not exists users;

use users;
SET foreign_key_checks = 0;

create table user(
	id int(12) not null auto_increment,
	username varchar(25) not null,
	email varchar(50) not null,
	password varchar(50) not null,
	primary key (id)
	
);
create table posts(
	id int(12) not null auto_increment,
	post_value varchar(300) not null,
	user_id int(12) not null,
	date_posted datetime default current_timestamp,
	primary key (id),
	foreign key (user_id) references user(id)
);
create table comments(
	id int(12) not null auto_increment,
	post_id int(12) not null,
	user_id int(12) not null, 
	comment_value varchar(300) not null,
	date_posted datetime default current_timestamp,
	primary key (id),
	foreign key (post_id) references posts(id),
	foreign key (user_id) references user(id)
);
