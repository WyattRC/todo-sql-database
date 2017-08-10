# todo-sql-database

psql
create database todolist;
create table todos(                                                                                                           id serial primary key,                                                                                                          title varchar(250) NOT NULL,                                                                                                   details varchar,                                                                                                               priority integer NOT NULL,                                                                                                     created_at varchar NOT NULL,                                                                                                   completed_at varchar                                                                                                            );
INSERT INTO todos (id, title, details, priority, created_at) values (1, 'sweeping', 'the deck', 2, '08/20/2016');

todolist=# select * from todos;
 id |  title   | details  | priority | created_at | completed_at 
----+----------+----------+----------+------------+--------------
  1 | sweeping | the deck |        2 | 08/20/2016 | 

INSERT INTO todos (id, title, details, priority, created_at, completed_by) values (x, 'x', 'x', x, 'x', 'x'); x4

select * from todos;
 id |       title       |      details      | priority | created_at | completed_at 
----+-------------------+-------------------+----------+------------+--------------
  1 | sweeping          | the deck          |        2 | 08/20/2016 | 
  2 | vacuum            | living room       |        3 | 08/20/2016 | 08/21/2016
  3 | beat the dead dog | -lexi 2k17        |       10 | 08/20/2016 | 08/22/2016
  4 | empty pool        | clean walls after |        6 | 08/20/2016 | 08/25/2016
  5 | walk dog          | 1 mile trail      |        8 | 08/20/2016 | 08/20/2016
(5 rows)

SELECT * FROM todos
WHERE completed_at IS NULL;

SELECT * FROM todos
WHERE priority > 1;

UPDATE todos
SET completed_at = 08/20/2016
WHERE completed_at IS NULL;

DELETE FROM todos
WHERE completed_at NOT NULL;
