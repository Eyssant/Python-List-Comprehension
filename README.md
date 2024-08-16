

<!DOCTYPE html>
<html lang="en-US">
<head>
<meta charset="utf-8">
<meta name="keywords" content="Python List Comprehension"/>
<meta name="Description" content="Python List Comprehension"/>
      
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/gh/google/code-prettify@master/loader/run_prettify.js"></script>

</head>
<body>


<div class="container-fluid pt-2 pb-2 pl-4 pr-4">
<div class="row">
<div class="col-lg-2 d-none d-lg-block">
  
</div>
<div class="col-lg-8 p-2 bg-white" style=" box-shadow: 10px 0 5px -2px hsl(240, 20%, 93%);"> 


<h1><strong>Python - List Comprehension</strong></h1><hr class="m-1">

<p>List comprehension is a technique of creating new lists using other iterable and in fewer lines of codes. The iterable object which can be used in this technique can be any data structure like list, tuple, set, string and dictionary, etc. An iterable created by using range() function can also be used here.</p>
<p>The syntax used in list comprehension generally contains three segments:<p>
<ul>
<li><strong>iterable: </strong>iterable object like list, tuple, set, string, dictionary, etc.</li>
<li><strong>transformation function: </strong>a transformation function that needs to be applied to the iterable.</li>
<li><strong>filters: </strong>filters/conditions which are required to apply on iterable.</li>
</ul>

<h2>Syntax</h2>
<pre class="prettyprint notranslate">
#list comprehension syntax
list = [tranform_func(i) for i in iterable if filters]

#which is equivalent to...
for i in iterator:
  if filters:
    list.append(tranform_func(i))
</pre>
<br>


<h3>Example: List comprehension using various iterable</h3>
<p>Below example describes how to apply different transformation functions on a given iterable.</p>	
<pre class="prettyprint notranslate">
#creating list of squares of natural numbers
MyRange = range(1,6)
NewList = [i*i for i in MyRange]
print(NewList)

#creating list of odd numbers
MyTuple = (1, 2, 3, 4, 5, 6, 7, 8)
NewList = [i for i in MyTuple if i%2!=0]
print(NewList)


#creating list of characters (in uppercase) of a string 
MyString = 'Hello'
NewList = [i.upper() for i in MyString]
print(NewList)

</pre>
<br>

<h3>Output</h3>	
<pre class="prettyprint notranslate">
[1, 4, 9, 16, 25]

[1, 3, 5, 7]

['H', 'E', 'L', 'L', 'O']

</pre>
<br>

<h2>List Comprehension and transformation function</h2>
<p>In above examples, transformation function is defined inside the list comprehension syntax. Alternatively, it can be defined outside of it, which gives the user to create more innovative function.</p>
<h3>Example: Create Grades using List Comprehension</h3>
<p>In below example, a function called <i>grade()</i> is created which is used inside list comprehension syntax to categorize iterator's element.</p>
  
<pre class="prettyprint notranslate">
def grade(x):
  if x &lt; 0:
    return 'Invalid'
  elif x &gt;= 0  and x &lt; 30:
    return 'Fail'
  elif x &gt;= 30  and x &lt; 50:
    return 'Grade C'
  elif x &gt;= 50  and x &lt; 75:
    return 'Grade B'
  elif x &gt;= 75  and x &lt;= 100:
    return 'Grade A'
  else:
    return 'Invalid'

MyList = [20, 45, 67, 90, -1, 89, 102]
NewList = [grade(i) for i in MyList]
print(NewList)
</pre>

<br>
<h3>Output</h3>    
<pre class="prettyprint notranslate">
['Fail', 'Grade C', 'Grade B', 'Grade A', 'Invalid', 'Grade A', 'Invalid']
</pre>

<br>
<h3>Example: Find Prime Numbers using List Comprehension</h3>
<p>A function called <i>prime</i> is created which is further applied on iterator using list comprehension technique to find out prime elements of the iterator. Please see the example below for more details.</p>
   
<pre class="prettyprint notranslate">
def prime(x):
  i = 2
  if x &gt;= 2: 
    count = 0 
  else: 
    count = None
  while i &lt;= x-1:
    if x%i==0:
      count = 1
      break;
    i = i + 1
  if count == 0:
    return x

MyRange = range(1,20)
NewList = [prime(i) for i in MyRange if prime(i) is not None]
print(NewList)
</pre>
<br>
<h3>Output</h3>   
<pre class="prettyprint notranslate">
[2, 3, 5, 7, 11, 13, 17, 19]
</pre>
<hr class="m-0">
<br><div class="recommend p-0 m-0 pl-2">
  <h3 style="color: hsl(225, 100%, 20%); font-size: 24px;">Recommended Pages</h3>
  <ul>
  <li><a href="https://en.wikipedia.org/wiki/List_comprehension">Wikipedia: List Comprehension</a></li>
  <li><a href="https://docs.python.org/3/tutorial/datastructures.html#tut-listcomps">Python.org: List Comprehension</a></li>
  <li><a href="https://www.datacamp.com/community/tutorials/python-list-comprehension">DataCamp: List Comprehension</a></li>
  <li><a href="https://alphacodingskills.com/python/pages/python-list-comprehension.php">AlphaCodingSkills: List Comprehension</a></li>
  <li><a href="https://www.youtube.com/watch?v=1HlyKKiGg-4">YouTube: List Comprehension</a></li>
  </ul>
</div>
<hr class="m-0 mt-3">
</div> 
<div class="col-lg-2 d-none d-lg-block"> 

 </div>
 </div>
</div>

</body>
</html>
