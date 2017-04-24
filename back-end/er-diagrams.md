# ER Diagram

An Entity Relationship Diagram \(ERD\) is a visual representation of different data using conventions that describe how these data are related to each other.  
In the given ER diagram, the elements inside rectangles are called entities while the items inside diamonds denote the relationships between entities.

* **Entity:**
  An entity can be a person, place, event, or object that is relevant to a given system. Entities are represented in ER diagrams by a rectangle and named using singular nouns.
* **Relationship:**
  A relationship describes how entities interact. Relationships are represented by diamond shapes and are labeled using verbs.
* **Cardinality:**
  Cardinality is the number of instance of an entity from a relation that can be associated with the relation.
  * **One-to-one:**
    When only one instance of an entity is associated with the relationship, it is marked as
    **1:1**
    .
  * **One-to-many:**
    When more than one instance of an entity is associated with a relationship, it is marked as
    **1:N**
    .
  * **Many-to-one:**
    When more than one instance of an entity is associated with the relationship, it is marked as
    **N:1**
    .

<center><img src ="../images/er-diagram/er-diagram-1.png"></center>

<center>ER diagram used in Taxi App Backend Architecture</center>

* **User:**
  * User plays one out of two roles: Rider and Driver
  * User is a Rider.
  * User is a Driver.
* **Rider:**
  * One Rider can add many new trip requests.
  * One Rider can take many trips.
* **Driver:**
  * One Driver can recieve many trip requests.
  * One Driver has many trips to process.
* **Trip:**
  * One Trip is taken by one Rider.
  * One Trip has one Driver.



