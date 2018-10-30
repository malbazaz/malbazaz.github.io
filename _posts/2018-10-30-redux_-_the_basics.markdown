---
layout: post
title:      "Redux - The Basics"
date:       2018-10-30 22:53:56 +0000
permalink:  redux_-_the_basics
---


It took some time to fully comprehend how react and redux work. Unfortunately, I found the Redux especially daunting and I feel its because the material around it complicated the explanations (in order to stay true to what it is). I felt that I understood the material in the course but when it came to its application, especially as I was building the App and finished the React part, I started struggling. I will attempt in explaining how Redux works in React, in a simplified matter and in an applicable manner but whilst attempting my best to stay true to what it does and how it functions. If I do a poor job or fail in explaining by distorting from the truth, please do let me know. 

Where do we start from?

So I will skip the React part but here is a quick guide on what to do: - Build a React app hard-coded first and then test it with functions such as fetch and see whether the page renders the data from the API you are getting. If you done this and you are now tackling Redux, this page is the right place for you.

As a good exercise, write down what you want to your components to do. Go over each component and give it a uniqug goal (whether it is Presentational Components (aka Dumb Components) and the Containers (aka Smart Components), it shouldn't matter.)

Create an action folder and action file for each specific Object/Class. In those files you are going to move any function to them. You should have actual functions that will enable you to do what you want to do in the Container components - Make sure to export them. You will also have support functions, used by those functions that you will export. Those functions are dispatch functions (they dispatch a certain type of action with a certain state). Comes the reducer. If I lost you let me explain it in more details:

Actions are like functions but they do not interact directly with data that we have. They don't have any idea of the data available, if anything they could return external data (through fetching). These actions do interact directly with the Components though. From what I have seen, I tend to categorize these actions as either they interact with the API and bring/take the data with the API or they interact between the Reducer(bear with me in explaning the reducer) and the Components.

Let's go quickly to the reducer so I can continue explaining the second category of actions. But first, you need to understand that in Redux - everything is stored in one place called the Store. In this store, you will have the different instances of state, whereby a copy of it gets created everytime state or anything in the store is changed/re-rendered.

A reducer is something that will take an action and a state, apply the action to the state and return a single value, the new state. So now that we defined reducers, you should create reducers that will encompasses cases that  if called upon by the functions being dispatched. So each case will render some action to the state, so that there is a new instance of that state that is created. Don't forget to combine all the reducers you created through combineReducers. will take the state being passed and the action prompting it to update the state. All reducers are joined together in the state through a combineReducers function.

So once we applied the reducer, as I explained there is some change, and this change will trigger the store to make a new instance that will represent this change. So now that the store is updated thanks to what we've done in the reducer, it needs to be represented in the component. Now comes the final piece how does the store re-render the change in the store.

The provider component is the key to connecting the components to the store. We're connecting what we hold internally that will be passed as props to the component. You will need a connect function and mapStateToProps at minimum. Look it up how it works. You might also need mapDispatchToProps, but there is a way around just calling the function - look it up as well, as I'm here to share with you how it works conceptually. Connecting back to the component enables to pass on the props to the component and represent the changes that we're done as we triggered it ourselves in the first or as it was triggered by an external element such as fetching. This is the circle of Redux.

