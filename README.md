### REMEMBER!!!
**Learning to code is like drinking from a fire hose, Try to drink as much water as you can with out drowning**

**NEVER get frustrated, or spend more than 15 minutes on any one problem, always reach out to Keenan for help**

**Have fun**

## Getting Started

Before we dive in, lets Make sure that you have the tools necessary to develop.

Use `command + space` to search your mac for the following applications

* Slack
* SublimeText3 
* Terminal

If you are missing any of these Applications stop here and contact Keenan.


## Part 1, Slack

Slack is the most popular way for development teams to communicate right now. It is simple, powerful and easy to use. 
If you dont have a account in slack, reach out to Keenan and he will send you an invite. Otherwise you can open the Slack App
and log in. 

You will see 3 channels as well as direct messages.
   
Channels: `cayla-cakes`, `general`, `random`
   
To keep good record of conversations and decisions, only talk about the topic for each channel. For example, in `cayla-cakes` we should only talk 
about development of cayla-cakes project. 

General messages belong to the general channel and random conversations belong to the random channel.

Slack also allows direct messaging

**Try it now**

`Open Slack -> login to kjrsdevs -> explore the app`


## Part 2, Sublime Text 3

Sublime Text 3 is the free text editor of choice for many developers. It offers much in the way of customization, but starts 
out as a very bare bones editor.

*Until you need more from  your editor, sublime text should get the job done. Even now I still use Sublime when my normal editor is running slowly.*

#### Simlink

Creating a simlink is a quick way to "hotkey" an application. For example, if you wanted to open a project with Sublime Text 3
you would have to open the Sublime Text 3 app -> File -> Open Project and then choose your project. This is no the developer way. 
Instead we are going to create a simlink so we can open the app from our command line.

 > Make sure Sublime Text 3 is installed in the Applications folder
 
 Open the Terminal app
 > `command + space` then type terminal and hit enter
 
In terminal, copy each command one at a time hitting enter after each one.
> **note** the `$` means that what ever comes after it is to be entered in terminal. You do not need to copy the `$`

``` 
$ cd
$ ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```
 
 If you got an error message, contact Keenan
 
 Now you can open the project you are working on with Sublime Text 3 by typing `subl .` in the working directory. We will go over that later.
 
 **Try It Out**
 
 `Open Terminal`
 ```$xslt
$ cd Desktop
$ subl .
```

What happened?
 
 
 ## Part 3, Terminal
 
 **Terminal Commands Cheatsheet**
 
 Where am I? `pwd `        
 What's around me? `ls`         
 How do I get around `cd place/ (forwards), cd .. (backwards)`            
 What does this command do? `man <command>`           
 How do I create a folder? `mkdir folder_name `            
 I want to copy something `cp thing new_thing `
 I wanna move a thing `mv thing new/location/thing `            
 I wanna to delete a thing `rm file`, or `rmdir folder`, or `rm -r folder`              
 Show me the contents of a file `cat file`, `less file`              
 I want to search for keywords `cat <file> | grep “keyword” `         
 How can I do that command again? up-arrow, `!!`, or `history `
 How do I clean up this mess? `clear ` or `command + k`         
 I tried running a program and it won't stop `ctrl+c`      
 Say something `say "something`    
 
 #### Getting Started
 
 Terminal is how you will open projects, run servers, commit code, and debug.
 
 First Open Terminal, and navigate to your desktop directory
 
 ```$xslt
$ cd Desktop
```

from here lets see what your desktop has on it
```$xslt
$ ls 
```
WOAH pretty cool right? You can see all the folders (directories) and files that exist on your desktop.

Ok, lets try to see some hidden things that Apple doesn't want the average user to see.
```$xslt
$ ls -a
```
BOOM, see those strange directories . .. and the strange files .ds_store and .localized?
>We dont really care about those files, but its cool that Terminal can show you things that are hidden. 

Terminal can also execute programs, lets try it
```$xslt
$ say "Hello World!"
```
Pretty cool right, the say command told the Mac Operating system to read outloud the text you gave it.

### My First Program

Lets use terminal to create our first program. A simple script that can print some code.
 
 first navigate back to the root directory
 ```$xslt
$ cd
```

Now navigate to your Desktop
```$xslt
$ cd Destop
```

Now lets create a Folder (directory) called Hello World
```$xslt
$ mkdir HelloWorld
```

now lets navigate into that directory
```$xslt
$ cd HelloWorld
```

now lets create a file called hello_world.js
```$xslt
$ touch hello_world.js
```

now, lets open this directory with Sublime Text 3
```$xslt
$ subl .
```
> note that you could open a specific file with subline by typing subl file_name. Using the dot syntax tells sublime that you want to open the whole directory

Now from here open the hello_world.js file and paste this in

```ecmascript 6
console.log('Hello World!')
```

Save the file (command + s) and go back to your terminal.

now run this command

```$xslt
$ node hello_world.js
```

What did you see?

#### My second program
> This one will have less walk through code, refer to the above tutorial for help

In the HelloWorld folder (directory), lets create a new file called add.js

Now in sublime text, select the add.js file and lets create a javascript function

```ecmascript 6
function () {
  
}
```

lets have our function take in 2 arguments that we will add together

```ecmascript 6
function add (arg1, arg2) {
  arg1 + arg2
}
```

now that our function adds stuff together we need it to return the result of the addition

```ecmascript 6
function add (arg1, arg2) {
  const result = arg1 + arg2
}
```

a const is a constant, here we are saying that result is equal to arg1 + arg2 and
that result will be constant and never change in this function again.

But we still need to return the result

```ecmascript 6
function add (arg1, arg2) {
  const result = arg1 + arg2
  return result
}
```

At the bottom of the file, lets console log the function with arguments of 2 and 8

```ecmascript 6
console.log(add(5,5))
```
 
 the whole file should look like this 
 
 ```ecmascript 6
function add (arg1, arg2) {
  const result = arg1 + arg2
  return result
}

console.log(add(2,8))
```
GREAT!!! Now lets save (command + s) and lets try out our new function

in terminal
```$xslt
$ node add.js
```

Wonderful, the console should have output 10. Take a moment to think about what is happening. 

> You created a function (a program) that takes 2 arguments and adds them together, then assigns them to a constant
> and returns the result. Then you said, console I want you to log the add function with arguments 2 and 8.

We can simplify this function to save some code, this is called refactoring. Its important to keep your code small and 
efficient for easy reading

We dont need assign result to a constant here because we are just returning it. A refactor woud look like this

```ecmascript 6
function add (arg1, arg2) {
  return (arg1 + arg2)
}

console.log(add(2,8))
```

**STOP** 10 minutes

experiment on your own now, try creating a subtraction function, a division or multiplication function. Play around here and see what you can do.

**GO**

Lets revisit why we used a constant. Constants are good for assigning a value to an object to be used later.
If I wanted the add function to return some text along with the result I would have to use 'interpolation'. Lets look at this example

```ecmascript 6
function add (arg1, arg2) {
  const result = arg1 + arg2
  return `The result of ${arg1} and ${arg2} is ${result}`
}

console.log(add(2,8))
```

before running this command, can you guess what it will return?

Try it now

By using the ` (the tick above the left tab key) you and type a string (text) and interpolate javascript into the string using ${}'s

Go ahead and add string interpolation to your other functions and try them out.

You have reached the end of the Intro, niceeee. Now its time to get going. Click [here](https://github.com/KJRSdevs/BootCamp/tree/master/Git) to get started on your first assignment.

Also, if you made it this far, then you are golden. I know its a lot, and its super confusing. And we havent even scratched the surface. 
But you have taken the first steps to learning how to make the computer do things for you, and not just use a computer.

**Take a break**

Coding is a lot of challenge for your mind. Mental exhaustion is real, and if you are feeling tired take a breather. Like any sport
you don't want to over do it starting out. However you will need to build up the mental endurance going forward.  

Some companies have hack-a-thons that people can participate in. I did a 48 hour hack-a-thon once where me and a team of 5 worked for 48 hours straight 
at the office. We slept in our cars when we needed sleep. It was super fun, and I can't wait to do another one. But if I had done that when 
I was first learning, I think I would have quit and never returned to code again.  Take your time learning, dont drown. But do push yourself
harder and harder to become better and better 