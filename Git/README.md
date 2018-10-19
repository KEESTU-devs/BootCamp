# GitHub and Git commandline

### Getting Started

Be sure to have terminal open and be in your root directory

```$xslt
$ cd
```

Watch this 30 minute video, and follow along

https://www.youtube.com/watch?v=HVsySz-h9r4

**STOP** 10 minutes, take a break

**GO**

OK, lets try it for yourself.

#### Cloning a Repo

Go to github.com and login. Click on your profile in the top right corner and select "your profile"

Once on your profile,  on the bottom left you will see organisations, and one of them should be called
**KJRSdevs**. Click on that one. 

There you will see all the Repositories that belong to KJRSdevs. Following the instructions from the video or googling how to do it. 
I want you to clone CaylaCakes in a folder that you create called Projects

**Acceptance Criteria**
> if you did this correctly you should be able to

```$xslt
$ cd Projects/CaylaCakes
$ git pull -r

> Already up to date.
> Current branch master is up to date.
```

#### Creating a repo

Go to github.com, click on your profile on the top right corner

Now click the Plus button and create a repository called MyFirstRepo. Check the box that says initialize with a readme.

Clone that repo to your projects folder

now open that project with sublime text

Select the README.md, and write a recap of what you learned. 

Save it, and now go through the process of commiting.

```$xslt
$ git add .
$ git commit -m "I updated the readme with a summary of how to use git"
$ git push origin master
```

**Acceptance Criteria**
> If you did this correctly

You should be able to see your updated readme on the github website in your new project.