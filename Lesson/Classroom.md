# Using Classroom for Github
For the remaining exercises in the course I plan to use [Classroom for Github](https://github.com/education/classroom). Here, I'll give you a sense of how Classroom for Github works and what you need to do to accept your assignments and turn in the exercises.

## Classroom for Github
Classroom for Github is basically an application that helps you make private copies of an assignment that you can modify and submit as your answers for the exercises. I create some template for an assignment that normlally would include the following:

- A basic description of the assignment
- A list of problems for you to solve/answer
- Some "starter" Python code or codes that you need to modify for the assignment
- Some data files to use with the Python scripts

For each exercise, I will post a link to the assignment. When you click the link, you will be taken to a webpage where you can accept the assignment [1]. When you accept the assignment a copy of it will be made in your personal Github repositories[2], and you will be asked to make changes to the Python code and main document for each assignment. More on that below.

## Working on the assignment
For most assignments you will be modifying the "starter" Python code that will be provided as part of the files copied to the assignment repository when you accept the assignment. After you get the code working, you will have questions to answer by modifying the main assignment document.

### Modifying the "starter" code
Here are some suggestions for working with the "starter" code.

- **Download the "starter" code**. You should first download a copy to your computer where you plan to work on the assignment. This computer should have a working installation of [Anaconda](Anaconda.md). You can download a copy of the code by clicking on it in the list of files you see for the assignment and then right-clicking on the **Raw** button above the Python code and selecting "Save Link As..." or the equivalent in your web browser. This will allow you to download a copy of the Python code to your computer.
- **Open Spyder**. Since you have a working Anaconda installation, you will have the [Spyder program](https://pythonhosted.org/spyder/), and Spyder will make it easy to modify and test your Python code. In the Linux computers in the computer classroom, you can launch Spyder by typing

    ```bash
    $ spyder
    ```
It may take a minute or two to open. In Windows you should have an application you can launch from the Start Menu, and on a Mac you can open the Anaconda Launcher on your Desktop and find Spyder there.
- **Load the "starter" code in Spyder**. Once you open Spyder you should see something like the window below.

    ![Spyder](Images/Spyder.png)<br/>
You can open your code in Spyder by going to "File -> Open..." in the Menubar. Select the code you downloaded and you're ready to start editing.
- **Make changes and test**. You can edit your Python code in Spyder just like a normal editor and make whatever changes you would like. After you have made some changes and would like to test them, save your file using "File -> Save" in the Menubar. Now you can have Spyder run your code by clicking on the green play button at the top of the window or pressing the F5 key. Your code will run and the results (plots, printed text, errors, etc.) will be output to the IPython console on the bottom right panel. If you need more space to see the console, you can drag the margins on the console frame to make it bigger.
- **Upload your modified code**. After you have made some change to the code that you want to save, you should upload a copy to your assignment repository on Github. You can do this by clicking on the **Upload files** button on the main page of the assignment repository and selecting the Python code you have been editing on your computer. When you upload the file, be sure to include a nice short commit message in the **Commit changes** box stating what you changed in the code since the last time you uploaded. To save the changes you click the **Commit changes** button. You are encouraged to upload a new copy of the Python code **every time** you make a change, such as fixing one of the problems in the starter code.

## Answering the questions
In your assignment repository you have a document titled `README.md` that contains the instructions for the assignment. This document is what is displayed by default in Github when you view the main page of a repository, and it is written in a simple language called [Markdown](https://daringfireball.net/projects/markdown/). Markdown allows you to write text in a normal text editor or on a webpage and then have that text converted from plain text to a nicely formatted document using simple formatting styles. I would like for you to enter your answers to the questions in the assignment in the `README.md` document, as well as embedding any plot figures. To edit your `README.md` file, you can do the following:

1. **Open the `README.md` for editing**. Click on the `README.md` in the list of files in the assignment repository, and then click on the **pencil icon** in the toolbar above the `README.md` to edit the document. The toolbar should look like the image below.

    ![Editing toolbar](Images/Edit-README.png)

2. **Make your changes**. After you click on the **pencil icon** you will see the Markdown version of the assignment document, and this is what you should edit. At the bottom of the `README.md` you will find a section that starts with `# Answers`. This is the section you should edit to add answers and plots for the assignment problems. Adding *italics* and **bold** text is easy, and if you would like more information on formatting you should take a look at the Github page on [Github-flavored Markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/).
3. **Preview your changes**. After you have made your changes, it is a good idea to click on **Preview changes** to make sure the changes you have made are formatted the way you expect. Markdown is pretty easy to use, but sometimes things don't end up looking the way you might like. **Preview changes** is in the editing bar above the document text, as shown below.

    ![Preview changes](Images/Preview-changes.png)

4. **Save your changes**. After you are done editing, you can save your changes by adding a commit message and clicking on the **Commit changes** button. As above, it is a good idea to make a short note of what you changed when you make changes in the **Commit changes** box.
5. **Check out the "pro" tips**. Below you will find some tips for using Github that will help you produce nicer looking plots and Markdown files, and to get the most out of using a resource like Github.

## Pro tips
Below is a short list of tips that might help you in preparing your answers for the assignments.

- **Save your stuff often**! You are strongly encouraged to commit (save) your changes regularly. For instance, each time you fix one of the issues in the "starter" Python code, you should upload a new copy and commit the changes with a short commit message. It might seem like extra work, but you can always go back to earlier versions of what you have saved on Github, so making frequent saves will ensure that you can find an older, working version of code in the event that you accidentally delete part of the code or otherwise break things.
- **You can always go back**. One of the best things about using Github is that you are able to go back to previous versions of the documents you save. For instance, if you decide to remove a `for` loop from your Python code, and later realize this was [a huge mistake](https://youtu.be/46Kv4rBJi68), you will be able to go back to earlier versions of the Python code that have been saved in Github. To go back to an earlier version simply click on the **History button** for one of the files in your Github repository, as shown below.

    ![History button](Images/Edit-README.png)
Once you pull up the document history you can click on the hash (the set of 7 numbers/letters listed to the right of a given version) to see the changes made for that save, or click on the `<>` button to see the version of the file at that time in the past.
- If you want to put you images into your answers document (`README.md`), I encourage you to upload copies of the images to the `Images` directory and then embed them using the Markdown format for images:

    ```
    ![Text in case image does not display](Images/filename.png)
    ```
You start with an `!`, put some simple text (2-4 words) about the image between square brackets `[]`, and then add a link to the image between parentheses `()`. Check out the example for Exercise 2 if this is unclear.
- **Use good quality images**. By default, Spyder will display your images in the IPython console window, and the image quality is just OK. If you would like to make nicer images to include in your answers to the problems, you can run you Python code outside of Spyder by typing

    ```bash
    ipython your-script.py
    ```
If your code is working, this should result in your plot popping up in a separate window and when you save the plot it will be at a higher resolution than the equivalent in the IPython console in Spyder. It is always nice to produce the best looking plots you can!

### Footnotes
[1]: Note that the first time you accept an assignment you will need to authorize the application on Github. This will not work if you have not verified your email address for your Github account.<br/>
[2]: A repository on Github is basically like a folder for a given assignment/project.
