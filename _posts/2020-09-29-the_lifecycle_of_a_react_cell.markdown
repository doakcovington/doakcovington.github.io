---
layout: post
title:      "The Lifecycle of a React Cell"
date:       2020-09-29 20:12:54 +0000
permalink:  the_lifecycle_of_a_react_cell
---


A Component is the powerhouse of a React cell. Well, not really...but sort of? React lifecycle can be challenging to understand, but much like biology, if you break it down, it can be easier to grasp.

Let's start at the top level. Components can either be classes or functions. In biology, structure determines function. So as not to confuse the use of the word 'function,' when referring to the biological examples, I will instead use the word 'role.' So in React, Components can either be classes or function and in biology, structure determines role. The same is true for React components.

Components that have the structure of a class have more features than components that are defined as functions. The structure determines features. Inside the cell wall of the class, a class component must have a subclass called render()

A cell needs energy to survive. We can think of render() as providing our component the energy in order to operate. Without render() the class component is nothing.

## The Lifecycle of a Class Component 

The cell lifecycle allows a cell to grow and divide. The component lifecycle allows a React application to grow and divide in a different sort of way. Each lifecycle has two different phases; the Render phase and the Commit phase.

**Mounting**

During the "Render phase" of Mouting, two methods are called; constructor() and render(). We've already gone over why render() is essential, but what about constructor() ? constructor() is sort of like DNA, which is the blueprint for life. Not every class component needs a constructor, just like not every cell has DNA. The constructor is used for initializing local state and binding event handler methods to an instance of a class. This lays the foundation for the role of the component.

During the "Commit phase" (after the component is mounted) componentDidMount is called. This method is used to set up any long processes or fetching data from an endpoint. This allows your component to display something while fetching your favorite Anatomy & Physiology diagrams from some far off endpoint.

**Updating**

Usually, when a cell reproduces, it duplicates its content and divides into two similar cells. Whenever a component's state or props change, it gets re-rendered (reproduced). There is no division, but the component is changing and growing.

componentDidUpdate is called after the component is rendered and updated. This can be used to compare the current props to previous props. We could check to see if the genetic code for eye color has changed.

**Unmounting**

Here we are, at the end of the component lifecycle. This is when the component will be deleted and cleared from the DOM. Cell death occurs when the cell ceases to carry out its role. componentWillUnmount() is called when a component is no longer needed to carry out its role. This method is called just before it gets deleted.

**Summary**

A Component is the powerhouse of a React cell. There are two different types of components that determine the features of the component. A Class Component goes through a lifecycle that includes creation, updating, and deletion.


