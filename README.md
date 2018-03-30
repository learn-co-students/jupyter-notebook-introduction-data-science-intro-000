
# Jupyter Notebook CodeAlong

### Introduction

So far, many of the readings and all of the labs you have been working with have been interactive.  You are working in an environment that allows us to both display text, and run Python code.  In this lesson, we explore the software powering these interactive documents, Jupyter.

### Jupyter Background

Jupyter is a web application that allows someone to create and work with documents that have live code.  It's a very popular tool among data scientists, as it allows for both explanation of thinking behind code as well as the code itself.

### Introduction to cells

The notebook itself consists of cells.  Double click on this content and to see what I mean.  Once we double click on a cell, we are in insert mode.  This means that we are able to edit the cells, just as you would if this were a word document.  We can tell that we are in insert mode because of the green border around the cell.  

Now, after being in insert mode for this cell, change some of the content.  Write anything, we can always undo it.  We can undo the changes of a cell by making sure we are in insert mode and then pressing command+z on a mac or control+z on windows.

To get out of insert mode and write the current changes and see the effect of the current changes, press shift + enter.

### Adding and Deleting Cells

We have already seen, to alter the contents of a cell we simply double click on that cell, bringing us into insert mode, and then change the contents.  Now let's see how to add, and delete cells from escape mode.

#### Adding cells

If we wish to quickly add a new cell we can do so with the following steps: 

* Make sure we are not in insert mode, but in escape mode
    * To get into escape mode, press the escape key.  You will no longer see a cell bordered in green.
* Then press the letter "b"
    * Once in escape mode, press the letter b

#### Deleting cells

To delete a cell we once again should be in escape mode, and then press the "x" key.

Of course, we'll want a way to undo our deletion.  You can press d to undo deletion of a cell.  Notice that this is different from cmd+z.  Pressing cmd+z undoes our changes inside of a cell, but pressing d from escape mode is to undo changing a cell in it's entirety.

### Types of Cells

The current cell and every other cell in this lesson has been a markdown cell, meaning that it allows us to write text and stylize that text.  For example, if you surround some text with stars on either side the text **becomes bold**.  That's markdown.

Cells can also have a type of Python code.  If we are writing in a cell that is for Python, everything in that cell must be valid Python or we will see an error.


```python
This is a python cell without valid Python so we wil see an error
```

So a cell must either be of type Python, in which case all of the contents must be valid Python, or a cell must be of type markdown.  It cannot be both.  We can quickly change a cell from markdown to code with some keyboard shortcuts.

From escape mode, we change a cell to type code by pressing the letter y.  Add a new cell by pressing the letter b, then type j to change that cell into type code.  Again, press shift + enter to save the changes of the cell.  To change the cell from code to markdown, from escape mode press the letter m.

### Working with Python in Jupyter

Ok, now that we know a little bit about adding and deleting cells, as well as changing cell types from markdown to Python, let's focus on working with Python in Jupyter.  We'll go into a large amount of detail about working with a Jupyter notebook in Python, but the main takeaway is this: if we see a Python cell, we should press shift + enter on that cell. 

The major gotcha in with working with Python code is that Python will only execute the Python cells that are run. So for example, just seeing the cell where we define `name` to `'bob'` below does not write that cell to memory.


```python
name = 'bob'
```

If we try to reference that variable later on, Python will tell us that it is not defined.  


```python
name
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-1-18697449d7c4> in <module>()
    ----> 1 name
    

    NameError: name 'name' is not defined


To execute or run a cell, we must press shift + enter from escape mode on that cell.  Upon running a show, Python will show the the last line of the cell's return value underneath.  Let's see this.


```python
age = 14
age
```




    14



As you can the variable `age` is set to 14, so when the cell is run `14` is displayed underneath.

One tricky thing to note is that assigning a varible **does not** have a return a value.  So even though the cell is run, if assigning a variable is the last line of a cell, nothing is displayed underneath.


```python
hometown = 'NYC'
```

Notice, even after pressing shift + enter on the code above, nothing is displayed below.  But if we reference the variable `hometown`, we see that the cell was run as the variable was defined.


```python
hometown
```




    'NYC'



> Yes, it's pretty confusing, but all we need to know is that just because we don't see something below a cell after pressing shift + enter, does not mean it is not run.  In the case of assignment, it is because the return value of assignment in None, and `None` does not show an output. 


```python
None
```

### Working through labs and readmes 

As you read through labs we encourage you to press shift + enter on each of the Python cells.  Often in labs, we will assign variables to data early on.  Then we will ask you to work with data stored in those variables.  To avoid going to the top of the lab to press shift + enter, it's best just to press that while reading along. 

The same thing goes for working through a Readme.  The Readmes will often assign data to variables, and it may be nice to work with data stored in those variables later on.  So it's a good idea to press shift + enter.  And now that you know how to work with Jupyter notebooks, you can always modify the notebooks with new code to test your understanding.

### Summary

In this lesson, we learned about Jupyter notebooks.  We saw that in Jupyter notebooks, we can either be in insert mode or escape mode.  While in insert mode, we can edit the cells, and undo changes within that cell with command+z or ctl+z.  In escape mode, we can add cells with "b", delete a cell with "x", and undo deletion of a cell with "d".  We can also change the type of a cell to markdown with "m" and to Python code with "j".  

Then we saw how to work with Python code in Jupyter notebooks.  We saw that to have our code in a cell executed, we should press shift + enter.  And if we do not do this, then we may assume that variables are assigned in Python that is not assigned.
