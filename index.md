# Welcome to my Quantum Engineer page

I created this page to explore the budding field of qunatum software engineering, i.e. accessing quantum computing and qunatum information through code. Quick background check, I have completed a PhD in Quantum Optics and Quantum Information and now work in machine learning research. This page is my attempt to understand the current state of quantum computing industry and gauge if it is possible for non-physics-phds to enter the field. I will try to keep this page as close to the practical engineering as possible and not go too deep into the physics and theory. However, some of the physics might be too cool not mention, so I will be exploring ways to make it more accessible to the uninitiated. Enjoy.

## Prerequisites
The only must-have prerequisite to follow this content is Python and numpy familiarity.
The good-to-have prerequisite are basic and advanced mathematics such as linear and matrix algebra and calculus.
Obviously if you have taken undergrad or graduate Physics/Quantum, then you may find the concepts familiar, but hopefully I wont be going into much of that.

# Chapter 1 - Quantum primitives and data structures
## Refresher of Python Data Structure Basics
Python has 4 basic data primitives - int, float, bool and string.
Python also has 4 inbuilt data structures - list, tuple, dict and set.
Most other complex data structures can be built upon these datastructures.
For example, a numpy ndarray is a nested list with some additional constraints, properties and operations. I will give one example of each -
### Construction
A numpy array of rank 0 is a python primitive. A numpy array of rank 1 is a list of numpy arrays of rank 0. A numpy array of rank n is a list of numpy arrays of rank n-1.
### Constraints
All elements of the rank-n list of the numpy ndarray must be of the same length. 
### Properties
Numpy ndarrays have a shape property, which is a tuple whose ith element is the length of the length of rank-i list.
### Operations
The '+' operation is redefined for numpy ndarrays. Only 2 ndarrays of equal shape can be added, resulting in a new ndarray of the same shape whose elements are elementwise sum of the two original ndarrays.

Thus a new data structure can be constructed from python primitives and data structure that have its own set of constraints, properties and operations. In mathematics this is known as a space, for example numpy ndarrays live in vector space where adding/subtracting/multiplying/transposing ndarrays gives you a new ndarray. So that puts us the right frame of mind to explore what is known as the Hilbert space of quantum objects.

## Hilbert space
What is a Hilbert space? Simple, it is a vector space.

### Wait is that it?
Yup. The Hilbert space which is where all our quantum engineering will happen is just a vector space with a few additional constraints and properties. Which means we can just use modified numpy arrays for everything we will do here. So good news right, if you know numpy you have everything you need.

### I dont believe you? What is this additional constraints and properties?
Lets explore that in all its detail.




You can use the [editor on GitHub](https://github.com/niranjansd/quantum-for-engineers/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/niranjansd/quantum-for-engineers/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
