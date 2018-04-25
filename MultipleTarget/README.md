To manage different environment with multiple targets, we can follow following things:

1. Go to your project target and Duplicate the Target like this:

![alt text](https://raw.githubusercontent.com/sagar7662/apienvironment/master/Images/Screen%20Shot%202018-04-25%20at%201.31.45%20PM.png)

  
2. Go to your project target(Duplicate target), select "Build Settings" and then search for "Other swift flags" like this:

![alt text](https://raw.githubusercontent.com/sagar7662/apienvironment/master/Images/Screen%20Shot%202018-04-25%20at%201.14.04%20PM.png)

3. Store "-DDEVELOPMENT" in Other swift flags.

4. Change your scheme to check whether you are working with development or production.

5. Now, do a global declaration in Appdelegate class like this:

#if DEVELOPMENT

let urlType = "Developemt"

#else

let urlType = "Production"

#endif
