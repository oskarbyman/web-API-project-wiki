# Important information for Deadline 3


:bangbang:&nbsp;&nbsp;**This chapter should be completed by Deadline 3** *(see course information at [Lovelace](http://lovelace.oulu.fi))*

---
<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Chapter summary</strong>
</summary>

<bloquote>
In this section you must implement a RESTful API. <strong>The minimum requirements are summarized in the&nbsp;<a href="">Minimum Requirements</a>&nbsp;section of the Project Work Assignment. If you do not meet the minimum requirements this section WILL NOT be evaluated. </strong>
<h3>CHAPTER GOALS</h3>
<ul>
<li>Implement a RESTful API</li>
<li>Write tests for the API</li>
</ul>
</bloquote>

</details>

---
<details>
<summary>
:heavy_check_mark:&nbsp;&nbsp;&nbsp;&nbsp; <strong>Chapter evaluation (max 20 points)</strong>
</summary>

<bloquote>
You can get a maximum of 20 points after completing this section. More detailed evaluation is provided in the evaluation sheet in Lovelace.
</bloquote>

</details>

---

# RESTful API implementation

## List of implemented resources

<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Content that must be included in the section</strong>
</summary>

<bloquote>
A list of all implemented resources. Consider that you do not need to implement every resource you initially planned. &nbsp; The minimum requirements are summarized in the Minimum requirements section from the Project work assignment. <em>Do not forget to include in the <a href="doc/README.md">README.md</a> file which is the path to access to your application remotely.</em>

</bloquote>

</details>

---

:pencil2: *List your resources here. You can use the table below for listing resources. You can also list unimplemented resources if you think they are worth mentioning*

|  Resource name       | Resource url | Resource description | Supported Methods    | Implemented |
|:-------------------: |:------------:|:--------------------:|:--------------------:|:-----------:|
|users collection|/api/users|Collection of all users|GET, POST|Yes|
|user item|/api/users/{user}|A single user|GET, PUT, DELETE|Yes|
|moves by user|/api/users/{user}/moves|All moves created by a user|GET, POST|Yes|
|user's move|/api/users/{user}/moves/{move}|A move created by a user|GET, PUT, DELETE|Yes|
|workouts by user|/api/users/{user}/workouts|All workouts created by a user|GET, POST|Yes|
|user's workout|/api/users/{user}/workouts/{workout}|A workout created by a user|GET, PUT, DELETE|Yes|
|moves in user's workout|/api/users/{user}/workouts/{workout}/moves|Moves wrapped in a users workout|GET, POST|Yes|
|move in user's workout|/api/users/{user}/workouts/{workout}/moves/{position}|A move in a users workout based on its position|GET, PUT, DELETE|Yes|
|moves collection|/api/moves|All moves in the database|GET, POST|Yes|
|move item|/api/moves/{move}|A move in the database|GET, PUT, DELETE |Yes|
|workouts collection|/api/workouts/|All workouts in the database|GET|Yes|
|workout item|/api/workouts/{workout}|A workout in the database|GET|Yes|
|moves in a workout|/api/workouts/{workout}/moves|All the moves in a certain workout in the database|GET|Yes|
|a move in a workout|/api/workouts/{workout}/moves/{position}|A move in a workout based on its position|GET|Yes|
---

## Basic implementation
<details>
<summary>
:computer:&nbsp;&nbsp;&nbsp;&nbsp; <strong>TODO: SOFTWARE TO DELIVER IN THIS SECTION</strong>
</summary>

<bloquote>
<strong>The code repository must contain: </strong>
<ol>
	<li>The source code for the RESTful API&nbsp;</li>
	<li>The external libraries that you have used</li>
	<li>We recommend to include a set of scripts to setup and run your server </li>
	<li>A database file or the necessary files and scripts to automatically populate your database.</li>
	<li>A <a href="documents/README.md">README.md</a> file containing:
		<ul>
			<li>Dependencies (external libraries)</li>
			<li>How to setup the framework.</li>
			<li>How to populate and setup the database.</li>
			<li>How to setup (e.g. modifying any configuration files) and run your RESTful API.</li>
			<li>The URL to access your API (usually <em>nameofapplication/api/version/</em>)=&gt; the path to your application.</li>
		</ul>
	</li>
</ol>
<strong>NOTE: Your code MUST be clearly documented. </strong>For each public method/function you must provide: a short description of the method, input parameters, output parameters, exceptions (when the application can fail and how to handle such fail). 
&nbsp;<strong>In addition should be clear which is the code you have implemented yourself and which is the code that you have borrowed from other sources. Always provide a link to the original source. This includes links to the course material.</strong>
</bloquote>

</details>

---
:pencil2: *You do not need to write anything in this section, just complete the implementation.*

---

### RESTful API testing
<details>
<summary>
:computer:&nbsp;&nbsp;&nbsp;&nbsp; <strong>TODO: SOFTWARE TO DELIVER IN THIS SECTION</strong>
</summary>

<bloquote>
<strong>The code repository must contain: </strong>
<ol>
	<li>The code to test your RESTful API (Functional test)
		<ul>
			<li>The code of the test MUST be commented indicating what you are going to test in each test case.</li>
			<li>The test must include values that force error messages</li>
		</ul>
	</li>
	<li>The external libraries that you have used</li>
	<li>We recommend to include a set of scripts to execute your tests.</li>
	<li>A database file or the necessary files and scripts to automatically populate your database.</li>
	<li>A <a href="documents/README.md">README.md</a> file containing:
		<ul>
			<li>Dependencies (external libraries)</li>
			<li>Instructions on how to run the different tests for your application.</li>
		</ul>
	</li>
</ol>
Do not forget to include in the <a href="doc/README.md">README.md</a> the instructions on how to run your tests. Discuss briefly which were the main errors that you detected thanks to the functional testing.

Remember that you MUST implement a functional testing suite. A detailed description of the input / output in the a REST client plugin.

In this section it is your responsibility that your API handles requests correctly. All of the supported methods for each resource should work. You also need to show that invalid requests are properly handled, and that the response codes are correct in each situation.
</bloquote>

</details>

---
:pencil2: *You do not need to write anything in this section, just complete the implementation.*

---

## REST conformance

<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Content that must be included in the section</strong>
</summary>

<bloquote>
Explain briefly how your API meets REST principles. Focus specially in these three principles: <strong>Addressability, Uniform interface, and Statelessness</strong>. Provide examples (e.g. how does each HTTP method work in your API). Note that Connectedness will be addressed in Deadline 4.
</bloquote>

</details>

---


Addressability: All the resources in the API are addressable via an URI. 

Uniform interface: The API uses the standard fixed HTTP methods. For example: The user specific items can be accessed with GET, PUT or DELETE methods

Statelessness: All requests happen in isolation and don't rely on previous requests.


---

## Extras

<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Details on extra features</strong>
</summary>
<bloquote>
This section lists the additional features that will be graded as part of the API but are not required. In addition to implementing the feature you are also asked to write a short description for each.
</bloquote>

</details>

### URL Converters

<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Fill this section if you used URL converters</strong>
</summary>
<bloquote>
Write a short rationale of how URL converters are used, including your thoughts on the possible trade-offs. Go through all URL parameters in your API and describe whether they use a converter, what property is used for converting, or why it's not using a converter.
</bloquote>
</details>

---

No URL converters were used since only one of the parameters required converting to int. This however cascaded as many model.query code lines which bloat the code visually. This is a improvement that could be done with a refactor if there is time before the final deadline.

---

### Schema Validation

<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Fill this section if you used JSON schema validation</strong>
</summary>
<bloquote>
Write a short description of your JSON schemas, including key decision making for choosing how to validate each field. 
</bloquote>
</details>

---

Schema validation is done in every POST and PUT method. The following schemas were implemented
user_schema, which requires that the request contains only the username
move_schema, which requires that the request contains a name and a description for the move. The user is parsed from the request URI
move_list_item_schema, which requires that the request contains a move name which will be added to the workout move list. Has optional parameters for repetitions and the position in the workout order. The position is assigned automatically to the last position of the workout unless specified.
workout_plan_schema, which requires that the request contains a name for the workout. Rest of the needed information is parsed from the request URI

---

### Caching

<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Fill this section if you implemented server side caching</strong>
</summary>
<bloquote>
Explain your caching decisions here. Include an explanation for every GET method in your API, explaining what is cached (or why it is not cached), and how long is it cached (and why). If you are using manual cache clearing, also explain when it happens.
</bloquote>
</details>

---
No caching has been implemented yet.

---

### Authentication

<details>
<summary>
:bookmark_tabs:&nbsp;&nbsp;<strong>Fill this section if you implemented authentication</strong>
</summary>
<bloquote>
Explain your authentication scheme here. Describe the authentication requirements for each resource in your API, and your reasoning for the decisions. In addition, provide a plan for how API keys will be distributed, even if the distribution is not currently implemented.
</bloquote>
</details>

---

No authentication has been implemented yet

---

## Resources allocation
|**Task** | **Student**|**Estimated time**|
|:------: |:----------:|:----------------:|
|Design, Implementation|Oskar Byman|12h| 
|Design, Implementation, Testing|Eemil Hyv??ri|6h| 
|Design|Antti Luukkonen|3h| 
|||| 


