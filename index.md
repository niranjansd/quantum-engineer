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

## Quantum States
Before we get to quantum states, lets take 1 quick detour to understand an illustrative example. If you have dabbled in ML, you might already know about the probability distribution vector which is often the final output of an ML model. Consider a dummy example, you build an ML model that identifies which fruit is present in an image. Each image contains 1 of 3 fruits, apple, orange or banana. Let us study what the output of this model looks like -
- Output of the model is an array.
- Length of the array is equal to the number of classes, in this case 3.
- The values of the array correspond to the predicted probability of the class in an arbitrary but fixed order. Lets say the order we fix is ['apple', 'orange', 'banana'] and the output of the model is [0.2, 0.3, 0.5]. This means that the model predicts 0.2 is the probability of the image being of an apple, 0.3 is the probability of an orange, 0.5 is the probability of a banana. This definition gives us two more constraints.
  - The sum of the output array is 1, since it is the sum of all the outcome probabilities.
  - All the element of the array much be >= 0.

Two key concepts to note here
 1. the definition of a `basis`. The output [0.2, 0.3, 0.5] is not just an array of numbers. Each number represents an object, in this case that object is a fruit. The fruit probability state is [0.2, 0.3, 0.5] and its 'basis' is ['apple', 'orange', 'banana']. Reordering the basis vector implies also reordering our state vectors, but it does not change the underlying information.
 2. The output array [0.2, 0.3, 0.5] captures everything we know about a specific image in a specific basis. We could measure the image in a completely new basis. For example, we could modify the basis to whether there is an apple in the image or not. In this case the new basis would be ['present', 'absent']. Then the new probability vector in this new basis would be [0.2, 0.8].

Now we are ready to define a quantum state data structure. We shall start with the simplest quantum state, a quantum bit or qubit. A qubit is a quantum object whose basis is of length 2. It is analogous to a classical bit which has only 2 possible states 0 or 1.
- Thus both the classical bit and qubit have a basis of length 2, which we can denote for convenience as ['0', '1'].
- If the classical bit is in state '0', its probability vector is [1., 0.]. If it is in state '1', its probability vector is [0., 1.]. The classical bit cannot be in any other state.
- The quantum bit can have any probability density vector, i.e it can be [0.5, 0.5], or [0.25, 0.75].
- What is more is that the probability density of [0.5, 0.5] actually describes many states. 


A qubit is a quantum bit, i.e like a classical bit, it has 
A Quantum state
- is an array.
- has a basis.
- 





Let understand the basic terminology of quantum states using analogies with numpy arrays.

Consider a numpy array of rank 1 is an array of numbers. e.g. a = [0, 3, 5]
But they dont have to represent just numbers, they could represent objects. For example, we can define a `basis` = ['Apple', 'Banana', 'Grapes']. Then we could define a new data structure called a `fruit state` with some constraints and properties.
### Constraints
- Length of the fruit state array is equal to the length of the basis. (In this example, length is 3.)
- The sum of the 

A quantum state is just a vector of state



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
