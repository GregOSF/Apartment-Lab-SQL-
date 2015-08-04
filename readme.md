# Apartment Lab

## Solutions to Basic Challenges (GregOSF)

1. \dg

2. \dt

3. SELECT * FROM owners

4. INSERT INTO owners
	(name, age)
	VALUES
	('Donald', 56),
	('Elaine', 24),
	('Emma', 36);

5. SELECT name FROM owners

6. SELECT age FROM owners ORDER BY age

7. SELECT name FROM owners WHERE name = 'Donald'

8. SELECT age FROM owners WHERE age > 30

9. SELECT name FROM owners WHERE name LIKE 'E%'

10. INSERT INTO owners
		(name, age)
		VALUES
		('John', 33),
11. 	('Jane', 43)

12. UPDATE owners
		SET age = 30
		WHERE name = 'Jane'

13. UPDATE owners
		SET name = 'Janet'
		WHERE name = 'Jane'

14. DELETE FROM owners
  		WHERE name = 'Janet'
  		RETURNING *;

15. INSERT INTO properties
		(name, num_units)
		VALUES
		('Archstone', 20),
16.     ('Shithole', 37),
		('Crackhouse', 15)

17. SELECT * FROM properties 
		WHERE name != 'Archstone'
		ORDER BY name

18. SELECT count(*) FROM properties

19. SELECT age
		FROM owners
		ORDER BY age DESC 
		LIMIT 1

20. SELECT name FROM owners LIMIT 3

21. SELECT * FROM owners
		FULL OUTER JOIN properties
		ON owners.id = properties.id

22. UPDATE properties
		SET owner_id = 1
		WHERE name = 'Archstone'

23. SELECT * FROM owners
		INNER JOIN properties
		ON owners.id = properties.id

24. SELECT * FROM owners
		CROSS JOIN properties

## Solutions to Stretch Challenges

1. ALTER TABLE properties RENAME COLUMN name TO property_name

UPDATE properties
	SET owner_id = 2
	WHERE property_name = 'Crackhouse'

UPDATE properties
	SET owner_id = 3
	WHERE property_name = 'Shithole'

2. SELECT count(*) FROM properties WHERE (owner_id > 1) AND (owner_id < 3)


