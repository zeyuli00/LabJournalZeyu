# Lab Journal
A lab journal template for students following courses using RStudio and Git. Adapted from the original project by [Rob Franken](https://robfranken.github.io/LabJournal/). This setup will allow you to publish your R-projects as a website using an easy workflow.

To use this, follow the steps below.


## Preparation

1. Make sure R and R-studio are installed;
2. Make sure the `rmarkdown`-package is installed in R-studio (with "install dependencies");
3. Make sure that you have a GitHub account;
4. Make sure that Git is installed. You can download and install it for your operating system from here: https://git-scm.com/install/. 


## Forking the repository

In this step you'll make a personal copy of this repository on your GitHub account, which you can customize and use for your own purposes. This is done by "forking" the repository. To do this:

1. Fork the repository using the fork button in the top right hand corner of Github, to make a personal copy of this lab journal;
2. Under your repository name, navigate to 'Settings'; click on 'Pages' on the sidebar; select the main-branch as your publishing source, and "serve" from the "docs"-folder. This means that the files in the docs folder will be published as a website. Save your settings.


You now have a personal copy of this repository on your account, which publishes html files (aka Github pages) as a website.

## Inviting collaborators:
Navigate to 'Settings'; click on 'Collaborators', and invite the lecturers of your course (e.g. rensec). After acceptance, the lecturers have access to you repository and can make contributions.


## Clone the repository:
1. In RStudio, go to File -> New Project -> Version Control -> Git;
2. Specify that you want to use the forked repository for your own purposes. 

The forked repository at your local path contains all of the files you need. All you need for it to work is (the latest version of) R and R-studio installed.

## Customize your lab journal:
1. Navigate to the repository on your computer and open the 'labjournal.Rproj' file. This should automatically open R-studio, and your current working environment will be inside this project.
2. Inside R-studio you should see a files tab in the bottom right hand corner; 
3. Customize the 'index.Rmd' from the heading "my lab journal" as you wish within R-studio, to make it your own. This will be the "front page" of your lab journal;
4. Make sure to install the `remotes` and `klippy` packages. Commands are included in the index.Rmd.


## Journal your work
1. To add files to your lab journal, create .Rmd files in the root directory of your repository. To create an .Rmd file, go to File -> New File -> R Markdown in R-studio. 
Choose HTML as the output format, and save the file in the root directory of your repository. Most likely, the file will contain some example code; you can delete this and replace it with your own content.
2. Add your code (this is where you do your actual work).
3. Use the "knit" button in the top right hand corner of the .Rmd file to compile it. This will create an .html file with the same name as your .Rmd file, which is what will be published on your website.

To maintain your personal notes and working scripts separately, create a dedicated folder. If you don't want this folder to be accessible to others, remember to add its name to the '.gitignore' file. Additionally, modify your 'site.yml' to ensure that the same content is excluded there as well. Keep in mind that any items within this folder will not be compiled.


## Commit your changes
When you have made changes to your .Rmd file that you're happy with, you "commit" your changes; this is git terminology to save your changes to the repository. A commit creates a point that you can revert to in the future, and also forces you to describe what you did.
To do this:
1. Save your file;
2. Go the Git tab in the top right hand corner of R-studio; your file should appear there. Select your file to "stage" it, and click "commit".
3. In the commit message, describe what you did (e.g. "added a new .Rmd file with my work on assignment 1"). This is important for you and others to keep track of your changes. 
A dialog box will pop up describing the result, you can close it, as well as the commit dialog.

## Add your new .Rmd to the website
1. Open _site.yml_ in R-studio; this file contains the structure of your website, and the .Rmd files that are included in it.
2. To add your new .Rmd file to the website, add a new line under "Menu:". You can copy the example for "Page 1", replacing "lab1.html" with the HTML file that was created when you compiled your .Rmd file, and "Page 1" with the name you want to appear on the website. Save the file.
3. Recompile the lab journal website using the "build website" button on the "build" tab function in the top right hand corner of R-studio. 
4. When compilation is complete, go to the Git tab, select all files that appear there (CTRL-A works) and commit them.
5. Click "Push" in the Git tab to push your changes to GitHub. This will update your website with the new .Rmd file you added. 
6. Your personal lab journal website will be published at: https://{USERNAME}.github.io/LabJournal/

As you add new .Rmd files to your project, you can add them to your website by following the workflow starting from "Journal your work" until here. If you make changes to your files, you simply save your file, commit and push to GitHub, and your website will be updated with the changes you made. The list of commits (visible on Github as well as in RStudio) allows you (and us) to keep track of your changes, and revert to previous versions if needed.

## Useful resources: 
1. Working with [Git](https://happygitwithr.com/index.html) and [GitHub Desktop](https://docs.github.com/en/desktop)
2. Getting the hang of R Markdown: [The Definitive Guide](https://bookdown.org/yihui/rmarkdown/) and [Cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/)
