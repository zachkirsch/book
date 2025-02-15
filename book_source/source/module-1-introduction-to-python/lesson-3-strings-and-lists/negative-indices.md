# Negative Indices


<div style="position: relative; padding-bottom: 62.5%; height: 0;">
    <iframe src="https://www.loom.com/embed/2c14882d5c6f4328961b933d58c5c7d9?sharedAppSource=personal_library" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
</div>

---

One clever notion in Python is the idea of a "negative index" that allows you to index into a string starting at the end. To understand this, it helps to refer to the normal indices of a string.  

Suppose we had the following string and slice:  

```python
s = 'hello world'
print(s[2:len(s) - 2])
```

This is the same idea of slices that we saw in the last slide. To understand why this prints `llo wor` , we can think of the picture showing the indices of the `str` Tas shown in the following image ( *Hint: Think of where `2` and `len(s)-2` fall on this picture* ).  

```{image} https://static.us.edusercontent.com/files/O6DgXxSxp4AtJg2JsGibHOpf
:alt: hello world string indexing
:width: 744
:align: center
```

Asking Python to go " `n` before the end" is such a common task, they provide another scheme for indexing that uses negative numbers! The idea is you start at the last character ( `'d'` ) being at index `-1` (since it is at index `len(s) - 1` in our indexing scheme), the second to last ( `'l'` ) being `-2` , etc. Pictorially, the negative indices are shown in the following image.  

```{image} https://static.us.edusercontent.com/files/oeDlJkGmqUtQXpUmO1wtDBXH
:alt: hello world string with negative indexing
:width: 744
:align: center
```

This means you can get the same output as above by referring to index `-2` instead of `len(s) - 2` , just like in the code below.  

```python
s = 'hello world'
print(s[2:-2])
```

Notice that the end index is still exclusive, we are just able to use `-2` as the end index instead of `len(s)-2` .  

##  Pause And Think  

Before running the code in the next cell, what do you think it would print?  

```python
s = 'hello world'
print(s[10:2:-2])
```

