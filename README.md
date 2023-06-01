# PHcsv
CSV library for JS
You can use CSV in your page.
Apache License 2.0


## USAGE
There are 2 methods.
- Element.toCSV()
- Element.downloadCSV()

:bulb:*Please follow the specification.*


### toCSV()
HTMLTableElement.toCSV
Parameters: Booleans
	You can choose whether to include each element in the result or not.
	Choose 'true' if you want to include element.
	Defaults are all 'true'.
Return: String
Example:
```html
<table id="simpleTable">
	<tr>
		<td>1</td>
		<td>Alex</td>
		<td>Male</td>
	</tr># PHcsv
CSV library for JS
You can use CSV in your page.
Apache License 2.0


## USAGE
There are 2 methods.
- Element.toCSV()
- Element.downloadCSV()

:bulb:*Please follow the specification.*


### toCSV()
HTMLTableElement.toCSV
Parameters: Booleans
  You can choose whether to include each element in the result or not.
  Choose 'true' if you want to include element.
  Defaults are all 'true'.
Return: String
Example:
```html
<table id="simpleTable">
  <tr>
    <td>1</td>
    <td>Alex</td>
    <td>Male</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Bob</td>
    <td>Male</td>
  </tr>
  <!-- can contain 'thead','th',and 'tfoot' -->
</table>

<table id="formattedTable">
  <caption>Members List</caption>
  <thead>
    <tr>
      <th>NAME</th>
      <th>AGE</th>
      <th>SEX</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cate</td>
      <td>24</td>
      <td>Female</td>
    </tr>
    <tr>
      <td>Daniel</td>
      <td>31</td>
      <td>Male</td>
    </tr>
    .
    .
    .
  </tbody>
  <tfoot>
    <tr>
      <th>Number</th>
      <td>5</td>
  </tfoot>
</table>
<!-- caption isn't included in result. -->

```
```javascript
let table1 = document.getElementById('simpleTable');
let table2 = document.getElementById('formattedTable');
cosole.log(table1.toCSV());
console.log(table2.toCSV(true,true,false));

/*
>>simpleTable
"1","Alex","Male"
"2","Bob","Male"

>>formattedTable
"Cate","24","Female"
"Daniel","31","Male"
.
.
.
//'tfoot' isn't included because of 3rd parameter.
*/
```


### downloadCSV()
HTMLTableElement.downloadCSV(thead,th,tfoot)
Parameters: Same as 'toCSV()'.
Return: none;
  Show a alert of confirming to download.
Example:
```javascript
table.downloadCSV(true,true,false);
```
	<tr>
		<td>2</td>
		<td>Bob</td>
		<td>Male</td>
	</tr>
	<!-- can contain 'thead','th',and 'tfoot' -->
</table>

<table id="formattedTable">
	<caption>Members List</caption>
	<thead>
		<tr>
			<th>NAME</th>
			<th>AGE</th>
			<th>SEX</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Cate</td>
			<td>24</td>
			<td>Female</td>
		</tr>
		<tr>
			<td>Daniel</td>
			<td>31</td>
			<td>Male</td>
		</tr>
		.
		.
		.
	</tbody>
	<tfoot>
		<tr>
			<th>Number</th>
			<td>5</td>
	</tfoot>
</table>
<!-- caption isn't included in result. -->

```
```javascript
let table1 = document.getElementById('simpleTable');
let table2 = document.getElementById('formattedTable');
cosole.log(table1.toCSV());
console.log(table2.toCSV(true,true,false));

/*
>>simpleTable
"1","Alex","Male"
"2","Bob","Male"

>>formattedTable
"Cate","24","Female"
"Daniel","31","Male"
.
.
.
//'tfoot' isn't included because of 3rd parameter.
*/
```


### downloadCSV()
HTMLTableElement.downloadCSV(thead,th,tfoot)
Parameters: Same as 'toCSV()'.
Return: none;
	Show a alert of confirming to download.
Example:
```javascript
table.downloadCSV(true,true,false);
```
