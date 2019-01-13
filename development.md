# **GEOG5990M Programming for Geographical Information Analysis: Core Skills**
### **[Hannah Wheldon](https://github.com/hannahwh05)** - **201284811** Username: [hannahwh05](https://github.com/hannahwh05)
---
## Development and Issues
---

This program was developed using code from my Assessment 1 agent-based model (ABM) for this module. That model can be seen on my GitHub repository at: <https://github.com/hannahwh05/GEOG5990M_Programming>.

During development of the model, I aimed to make it as adaptable as possible so that a different environment could easily be imported and consequently the number of drunks could be changed. Frequently, this meant starting with a specific function suited to this project and then generalising from there.  

Initially, I wanted to find the coordinates of the pub exit so I could determine the drunks’ starting point. However, I then realised this could be adapted to find any set of coordinates for doors within the environment, provided a value or “ID” was input. I could therefore use this function to find each drunk’s house door. 

When defining the way my drunk moved, I wanted to make it clear that their movements were random and that they were not just going directly to their homes, so I called the function “stumble”. To start with I made the function very similar to my “move” function from my ABM, but with the addition of a condition where it could only move if it was within a value of the environment that was equal to zero. I soon realised then that they would not be able to arrive home as their house values would not be equal to zero. I also adjusted the torus to create the appearance of town walls so that drunks could not just cross space and time! 

This version was working for a while during the simulation but then it would break, due to “list index out of range”. Ultimately the drunks would take a very long time to reach their homes as they wondered aimlessly around the environment. I thought of a way of giving them direction by creating a function that would calculate the distance to their homes. At first, I just input the pub door coordinates but thought that the drunks would need constant updates on their distance to make it home. As a result, I changed this to general X and Y coordinates that could be input. I then defined the current and potential distances within the stumble function. This made the drunks movements less randomised, so I introduced a “randomness” variable to the stumble function, making them appear more drunk. 

When updating Spyder to 3.3.2 I found that despite the backend being set to inline, an additional blank window, called Figure 1, was being created every time I ran the model. When matplotlib.pyplot is mentioned in the code it creates a popup window. To resolve this I have added the following lines to a couple of point in the code so that plots are printed to the console:

```
shell = IPython.get_ipython()
shell.enable_matplotlib(gui='inline')
```
 
Due to time constraints and difficulties adjusting specific colours in the environment, I was unable to overlay the density map on top of the animation. 

---

[< Assessment 2:](https://hannahwh05.github.io/Assessment2)

   [< The Model](https://hannahwh05.github.io/model2)

   [> Potential Additions to the Model](https://hannahwh05.github.io/additions)
