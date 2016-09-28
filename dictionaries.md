# Python Dictionaries

Introduction to Python Dictionaries

Ben Taylor, Goucher College Digital Arts




## What is a dictionary?
.

A dictionary is a lot like a list, with one major difference:

Items in a **list** are accessed using **numbers.**

```
mylist[0]
```


Items in a **dictionary** are accessed using strings of **text.**


```
mydict["word"]
```

A dictionary can therefore be described as a data structure in which each piece of data (a *value*) is associated with a word (a *key*). 


Let's look at an example:

```
profile = {
			'name': 'Hootie',
			'occupation': '90s icon',
			'location': 'VH1'	
		  }

```


In the above example, `profile` is a dictionary. The first *key* is 'name', and it is associated with a *value*: 'Hootie'.

You could access each part of his profile like this:

```
print profile['name']
# the result is: 'Hootie'

print profile['occupation']
# the result is: '90s icon'

print profile['location']
# the result is: 'VH1'

```

Therefore, a dictionary is often a more descriptiive data structure than a list.


## Creating a dictionary

You can write a dictionary by hand, using curly brackets.

This creates an empty dictionary called `spanish`:

```
spanish = {}
```

This creates a dictionary that could translate english to spanish

```
spanish = {
           'hello': 'hola'
		  }
```
The word on the left is the key, and the word on the right is the value. We will use the key to look up a value, just like you use a word to look up a definition in a real-life dictionary.

We can add more items to our dictionary, separating them by commas:

```
spanish = {
           'hello': 'hola',
           'bye': 'adios',
           'what is up?': 'que pasa?',
           'niice': 'que rico'
		  }
```

Notice that there is no comma after the last item in the list.


## Accessing items in a dictionary


We can access the data in our dictionary by writing the name of our dictionary, `spanish`, followed by square brackets containing the word we wish to look up:

```
print spanish['hello']
# the result is: 'hola'
```

Again this is very similar to the way we looked up items in a list...

```
print mylist[0]
```

...except now we are using a word instead of a number.


## Looping through a dictionary

Just like you can loop through a list to access each line in a list, you can loop through each item in a dictionary if you need to.


The code for looping through the dictionary `spanish`:

```
for key in spanish:
	print spanish[key]
	
# the result would be...
'hola'
'adios'
'que pasa?'
'que rico'
```

Each time through the loop, 'key' will be equal to one of the keys in our dictionary. (The key is the word on the lefthand side of our dictionary.)

The first time through the loop, `key` will contain the string 'hello'.
The second time through the loop, `key` will contain the string 'bye'.



## More operations:

### Editing items in a dictionary

We can edit the values in our dictionary

```
spanish["hello"] = "diga" 

print spanish["hello"]
# the result is: 'diga'
```

### Adding items to the dictionary

Or we can add new items to our dictionary

```
spanish["where"] = 'donde'
```

### Is the word ____ in my dictionary?

```
if "hello" in spanish:
	print "Yes, I know how to say hello in Spanish"
else:
	print "No, I don't know how to say hello in Spanish."
```


# Dictionaries in practice


Let's look at an example of how a dictionary might be used in practice.

Let's imagine a census of the United States. In a census, the government gathers information about each citizen, and combiles it into a large data set.

The information about each person could be modeled as a dictionary:

```
Person = {
			name: "Hootie",
			occupation: "90s icon",
			location: "VH1"	
		  }
```

But, of course, in the US, there's not just one person, there are many people!

The census data, then, would probably be stored as a **list** of all the people in the country. Each item in the list would be a dictionary! This is how these datatypes can combine to create useful models of the world.

Let's first create a list:

```
us_census = [ 
				person1, 
				person2, 
				person3
			]

```

But, we need to replace each person with a dictionary describing them --

```
us_census = [
				{
					name: "Hootie",
					occupation: "90s icon",
					location: "VH1"	
		  		},
				{
					name: "Hootie",
					occupation: "90s icon",
					location: "VH1"	
		  		},
				{
					name: "Hootie",
					occupation: "90s icon",
					location: "VH1"	
		  		}
			]
```

OK, we have a census of 3 people.

To access values now will involve a bit more navigation!

First we need to choose which person we want to get information about -- meaning which item in the `us_census` list we want to access.

To access the first person in the list:

```
us_census[0]
```

Then we can access data about that person:

```
us_census[0]['name']
```

This would return the name of the first person in our census.



### Why learn to combine dictionaries and lists?

Because this is the way that the data of the world is stored. As we start our data visualizations, we'll look online for sources of data. We may use climate data or crime data, but most of the data we'll find will be some combination of lists and dictionaries. 




