# Important information for Deadline 2


:bangbang:&nbsp;&nbsp;**This chapter should be completed by Deadline 2** *(see course information at [Lovelace](http://lovelace.oulu.fi))*

---
<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Chapter summary</strong>
</summary>

<bloquote>
In this section students must design and implement the database structure (mainly the data model).

In this section you must implement:
<ul>
<li>The database table structure.</li>
<li>The data models (ORM)</li>
<li>Data models access methods (if needed)</li>
<li>Populating the database using the models you have created</li>
<ul>
</bloquote>
<strong>In this section you should aim for a high quality small implementation instead of implementing a lot of features containing bugs and lack of proper documentation.</strong>
<h3>SECTION GOALS:</h3>
<ol>
<li>Understand database basics</li>
<li>Understand how to use ORM to create database schema and populate a database</li>
<li>Setup and configure database</li>
<li>Implement database backend</li>
</ol>
</details>

---

<details>
<summary>
:heavy_check_mark:&nbsp;&nbsp;&nbsp;&nbsp; <strong>Chapter evaluation (max 5 points)</strong>
</summary>

<bloquote>
You can get a maximum of 9 points after completing this section. More detailed evaluation is provided in the evaluation sheet in Lovelace.
</bloquote>

</details>

---

# Database design and implementation

## Database design
<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Content that must be included in the section</strong>
</summary>

<bloquote>
Describe your database. The documentation must include:
<ul>
<li>A name and a short description of each database model. Describe in one or two sentences what the model represents.</li>
<li>An enumeration of the attributes (columns) of each model. Each attribute must include:
	<ul>
		<li>Its type and restrictions (values that can take)</li>
		<li>A short description of the attribute whenever the name is not explicit enough. E.g. If you are describing the users of a "forum", it is not necessary to explain the attributes "name", "surname" or "address" </li>because their meanings are obvious.
		<li>Characteristics of this attribute (e.g. if it is unique, if it contains default values)</li>
	</ul>
</li>
<li>Connection with other models (primary keys and foreign keys)</li>
<li>Other keys</li>
</ul>
You can use the table skeleton provided below

For this section you can use a visual tool to generate a diagram. Be sure that the digram contains all the information provided in the models. Some tools you can use include: <a href="https://dbdesigner.net">https://dbdesigner.net/</a>, <a href="https://www.lucidchart.com/pages/tour/ER_diagram_tool">https://www.lucidchart.com/pages/tour/ER_diagram_tool</a>, <a href="https://dbdiffo.com/">https://dbdiffo.com/</a>

</bloquote>

</details>

---

:pencil2: *The table can have the following structure*

|**Name** | **Type**|**Restrictions**|**Description**|**Characteristics** | **Links**|
|:------: |:-------:|:--------------:|:-------------:|:-----------------: |:--------:|
|Name of the attribute|Attribute type|Values that the type can take|Description of the attribute|Uniquenes, default...| keys and foreign keys|
	
User:
Contains data of the user.
|**Name** | **Type**|**Restrictions**|**Description**|**Characteristics** | **Links**|
|:------: |:-------:|:--------------:|:-------------:|:-----------------: |:--------:|
|id|Integer|None|||Primary key| 
|username|string(64)|None||Unique, not nullable|| 	
	
Workout Plan:
Workout plan that contains a number of moves.
|**Name** | **Type**|**Restrictions**|**Description**|**Characteristics** | **Links**|
|:------: |:-------:|:--------------:|:-------------:|:-----------------: |:--------:|
|id|Integer|None|||Primary key| 
|name|string(64)|None||not nullable||
|creator_id|Integer|None|Creator of the plan||User ID| 	
|workout_moves|Integer|None|MoveList of the workout plan||MoveList ID| 	

MoveList:
A list of the workout moves and the amount of repetitions
|**Name** | **Type**|**Restrictions**|**Description**|**Characteristics** | **Links**|
|:------: |:-------:|:--------------:|:-------------:|:-----------------: |:--------:|
|id|Integer|None|||Primary key| 
|position|Integer|None||not nullable||
|plan_id|Integer|None|Plan the move list is a part of||User ID| 	
|move_id|Integer|None|The workout move in the list|not nullable||	
|repetitions|Integer|None|Amount of move repetitions in the plan for the move|not nullable||	
	
Workout Move:
A workout move with a description.
|**Name** | **Type**|**Restrictions**|**Description**|**Characteristics** | **Links**|
|:------: |:-------:|:--------------:|:-------------:|:-----------------: |:--------:|
|id|Integer|None|||Primary key| 
|name|string(64)|None||not nullable||
|creator_id|Integer|None|Creator of the move||User ID| 	
|description|string(64)|None||not nullable||	
	

:pencil2: *Do not forget to include a diagram presenting the relations*

![image](https://user-images.githubusercontent.com/36500268/155485666-6d05b58c-4a83-4f50-aa1b-000d75c8305e.png)
	
---

## Database implementation
<details>
<summary>
:computer:&nbsp;&nbsp;&nbsp;&nbsp; <strong>TODO: SOFTWARE TO DELIVER IN THIS SECTION</strong>
</summary>

<bloquote>
<strong>The code repository must contain: </strong>
<ol>
<li>The ORM models and functions</li>
<li>A <var>.sql dump</var> of a database or the <var>.db file</var> (if you are using SQlite). You must provide a populated database in order to test your models.</li>
<li>The scripts used to generate your database (if any)</li>
<li>If you are using python, the requirements.txt file.</li> 

<li>A README.md file containing:
	<ul>
		<li>All dependencies (external libraries) and how to install them</li>
		<li>Define database (MySQL, SQLite, MariaDB, MongoDB...) and version utilized</li>
		<li>Instructions how to setup the database framework and external libraries you might have used, or a link where it is clearly explained. </li>
		<li>Instructions on how to setup and populate the database.</li>
	</ul>
</li>
<li> If you are using python a `requirements.txt` with the dependencies</li>
</ol>

</bloquote>

</details>

---

:pencil2: *You do not need to write anything in this section, just complete the implementation.*

---

## Resources allocation 
|**Task** | **Student**|**Estimated time**|
|:------: |:----------:|:----------------:|
|Desgin + Implementation|Eemil Hyv??ri|6hrs| 
|Design + Update Wiki|Antti Luukkonen|3hrs| 
|Design|Oskar Byman|2hrs| 
|||| 
|||| 
