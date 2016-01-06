#To Do List

You are going to make a to do list yeah! It will let you view your items, add new items, and complete items.

Concerpts Covered:
- Creating a form that uses POST
- Creating a MySQL table
- Accessing the table from PHP
- Inserting a new record into the table
- Updating the records that are already there

###Steps

1. Build a form - Create a form that submits with a POST to the current page.  

2. Create the ListItems MySQL table - In phpMyAdmin, create a new table called ListItems.  

3. Connect to the database - Create a database connection using PDO to connect to the table you have created.  

4. Save the list items - The form that you have POSTing to the current page, have it INSERT the new list item to the ListItems table.  

5. Displaying the list items - Use a SELECT statement to retrieve the items from ListItems.  

###Resources
php.net - http://php.net/ This is the offical documenation for PHP, look here when looking for a function or seeing what something does

PHP The Right Way - http://www.phptherightway.com/ - This has general information on PHP, it is up to date so you won't be reading old best praticies.

###Detailed Steps

#### Build a form
Forms are all over the internet as a way of submitting user inputted data. Here is a basic form with one input.
```HTML
<form action="file-you-want-to-submit-to.php" method="POST>
   <input type="text" name="name" value="">
   <input type="submit" name="save" value="Click to Save">
</form>
```
Let's look at the first line of the form.
```HTML
<form action="file-you-want-to-submit-to.php" method="POST>
```

The action is where the data will be sent to. 
The method is what HTTP method is used to send the data. You can use either POST or GET

With PHP, a form submitted with the POST method has its data in the global $_POST variable.  A form submitted with the GET method will have its data in the global $_GET variable.

When you click on the submit button, the page will reload (if you used the current page as the action) or go to the page specfied. On that page you can then access your data values in the global $_POST or $_GET variables.

You can see what is in global variables by printing them to the screen using print_r(). print_r() is like print or echo, only it takes an array as an input.

```
$string = 'Hello';
echo $string; //This will print out: Hello
print $string; //This will print out: Hello
print_r($string); //This will print out: Hello

$array = array('hats','shoes');
echo $array; //This will print out: Array
print $array; //This will print out: Array 
print_r($array); //This will actually print out the items in your array
```

So when you want to print out what is in an array, use print_r();

Wrapping the print_r in `<pre>` tags puts the data in a more friendly to read format. 

```PHP
print '<pre>';
print_r($_POST);
print '</pre>';
```
Now you can see that the data you submitted in the form is indeed in the global variable. Now let's do something with that data.


