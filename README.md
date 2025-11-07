# Java_JPA_Hibernate-lab-02_Case2_Solved

## Exercise

Identity of entity definition

Goal

Learn how to define simple and composite identity of entity in terms of Java Persistence API. 

Subject

There is a Department entity (with fields: companyName, name and description) and 3 cases to defined identity for it:

1.	Single identity

2.	Composite with identity as separate class (using @EmbeddedId)

3.	Composite with identity fields inside the entity class (using @IdClass)


**CASE 2#** :

Composite with identity as separate class (using @EmbeddedId)

6.	Open class edu.jpa.entity.DepartmentKey. This class represents the entity identity (company name + department name).

7.	Define this class as implementing java.io.Serializable (composite-id class must implement Serializable)

8.	Open class edu.jpa.entity.Department_2

9.	Specify class-level annotation @Entity. This lets JPA runtime to know that this particular class should be treated as an entity.

10.	Specify field-level annotation @EmbeddedId for field id (of type DepartmentKey).

## Solution

```
USE JPA_DB_02;

SHOW TABLES;

SELECT companyName, departmentName, description FROM Department_2;
```

<img width="1919" height="847" alt="image" src="https://github.com/user-attachments/assets/5b799809-c534-456a-af2c-33f18b45cbb1" />
