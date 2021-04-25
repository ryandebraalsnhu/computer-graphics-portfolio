# Computer Graphics Portfolio
https://github.com/ryandebraalsnhu/computer-graphics-portfolio

## How do I approach designing software?

Personally, I always employee a "fail fast" philosophy, which is sometimes known as 
"defensive programming". (Contieri, 2020) Whenever I write code, I immedietly try 
to determine if the data is valid. If it isn't, I stop working with it immediately 
and return a well formatted exception. It is pointless to try to "shove bad data" 
through the business logic.

Very often I see code which looks like this:

```
if (collection != null) {
    if (collection.Data != null || collection.Data.length < 1) {
        for (var d in collection.Data) {
	        if (d != null) {	        
 	            if (d.ID != null && d.ID > 0) {
		            //Business logic goes here...
                } else {
					//Invalid ID...
				}
	        } else {
				//Data in loop is null...
			}
        }		
	} else {
		//Data in collection is null...
	}	
} else {
    //Collection is null...
}
```

This is needlessly convoluted "spagetti code". This same logic could be refactored to read 
more cleanly and be more robust by simply testing the data and stopping progress (fail fast) 
as soon as the data isn't viable:

```
if (collection == null || collection.Data == null || !collection.Data.Any())
    return Error("An invalid collection has been specified.");

for (var d in collection.Data) {
    if (d == null || d.ID == null || d.ID < 1)
        continue; 

    //Business logic goes here...  	
}
```

## What new design skills has your work on the project helped you to craft?

Working with OpenGL has given me a better understanding of how C++ organizes it's 
dependancies. I usually work with C#, which allows you to very easily grab a dependancy 
either from the managed code bases (i.e. System.Web.dll) or by linking to a class library 
project within your solution.

I found it challenging and interesting to have the "raw" code for dependancies to be so 
readily at your finger tips. If need be, a developer could fork an existing dependancy
and customize it to their particular needs. I now have a much better understanding of 
"Dependancy Hell". (Allen, 2016)


## What design process did you follow for your project work?

While working on my project, I tried to be as iterative as possible. I would not have been 
able to produce the final project had I not spent the prior six weeks using my existing 
codebase as the start to each week's assignment.

## How could tactics from your design approach be applied in future work?

The ability to organize work efforts and execute them in a timely manner, in a logical order 
is a skill that will server a developer well not only in their professional career but also 
in life.

## How do I approach developing programs?

When writing code it is important to validate the data you are working with on every level.
When you receive the data from an external source, validate that it is not null and that it 
is in the expected format. When iterating across a collection validate that the collection 
itself is not null and that it has conents. When working with objects, be sure to validate 
each field's data type.

## What new development strategies did you use while working on your 3D scene?

During the course of this project, I used alot more guess and check than I am normally 
comfortable with using. Without the aid of CAD I needed to constantly build and run 
my application to determine if the picture in my head matched what was rendered on to
the screen.

## How did iteration factor into your development?

It was essential. The shear complexity of the final project was the culmination of over 
40 hours work of work, which just wouldn't have been possible to do without delegating
those efforts over the duration of the entire course.

## How has your approach to developing code evolved throughout the milestones, which led you to the project’s completion?

I think the existing development strategies that I use in my professional life worked, 
however if I were able to give advise to my past self (or to future students in your class)
it would be to better familiarize myself with the way C++ structure it's applications.

I lost hours of productively simply trying to get header files to read from eachother in the 
correct order. When it finally did work, I had sort of a "Frakenstein" system cobbled together.

## How can computer science help me in reaching my goals?

I've been using "computer science" since I was 5 years old. It is an essential part of my life
and not only has it provided me with a comfortable living but it has helped me to develop 
useful skillsets in all areas of my life. The ability to break down situations into logical
steps and then execute them to in focused "sprints" has helped me do everything from: getting 
a paycheck to assembling furniture from Ikea.

## How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future educational pathway?

This class will serve as an example of how it is important to completely absorb the content 
before jumping into an assignment. I think I needlessly made things much more difficult for 
myself when I started a new assignment, coded for 4 hours, and they once I ran into a roadblock 
went back to Brightspace only to discover that I've been coding down a blind alley due to a 
fundamental misunderstanding of a concept that would have already been presented to me.

## How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future professional pathway?

I have a new found respect for C++ developers. I wouldn't pursue it as a career, but I definetly 
have a better understanding of the need to be iterative when creating things. Even C# is essentially
just a highly wrappered version of underlying C++ functionalities.

## Citations

Allen, A. (2016, August 15). What is dependency hell? Retrieved April 25, 2021, from https://searchitoperations.techtarget.com/definition/dependency-hell
Contieri, M. (2020, May 26). Fail fast PHILOSOPHY, Explained. Retrieved April 25, 2021, from https://hackernoon.com/fail-fast-philosophy-explained-si963vk9

