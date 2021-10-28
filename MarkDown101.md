# Writing Notes Using MarkDown

## Overview
* How to Verify that you have an application
* How to install an Editor
* Purpose of MarkDown
* MarkDown Examples; Italicing, Bolding, Listing
* Embedding Code Into MarkDown Notes
* Embedding hyperlinks into MarkDown Notes
* Embedding images into MarkDown Notes
* How to `push` notes to `GitHub`


### How to Verify that you have an application
* To verify that you have an application hold `Command` and press `Space` to unveil the _Spotlight search_ and type the name of the application into the the search bar


### How To Install An Editor
* To install the `visual-studio-code` editor, execute the command below from the terminal

```
brew install --cask visual-studio-code
```

### Purpose of MarkDown
* The purpose of MarkDown is to have shorthand way of writing HTML
* Leon advocates for MarkDown particularly for new programmers to take notes in
* Using MarkDown and Github in this course will enable a sort of _hive mind_; Everyone will know what everyone knows.

### MarkDown Examples

#### Italicizing
* To italicize a phrase, or some text, _wrap_ the text in underscores _.

#### Bolding
* To bold a phrase, or some text, **wrap** the text in double asterisks **.

#### Listing
* To create a List, begin each line with a single asterisk *.
* This is another item in the list
* This is the third item in the list
* You can create sublists by appending a tab before an asterisk within a list.
    * This is a sublist item
    * This is another sublist item
    * And this is a third sublist item
    

### Embedding Code Into MarkDown Notes
* To embed code in-line, `wrap` a phrase or text, with single backticks `.
* To embed multiline code, wrap a body of text in triple backticks, on a new line

```python
print("Hello world!")
```

According to the slides, the code above is the python equivalent of the java snippet below

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello world!");
    }
}
```

### Embedding hyperlinks into MarkDown Notes
* To embed a link in MarkDown, wrap the phrase you would like become a link in square brackets [].
    * Follow the square brackets with a wrapping of the link in parenthesis.
* [Here](https://school.zipcode.rocks/users/leon) is an example of a link to your student portal!


### Embedding Images Into MarkDown Notes
* To embed an image in MarkDown, prefix a hyperlink with a bang !
    * `![](some-link-to-image.jpg)`

![](https://crayongirllinz.files.wordpress.com/2015/01/rubber-ducky.jpg)

### How to `push` notes to `GitHub`
1. To create a new repository in github, navigate to [github.com/new](https://github.com/new)
2. Select the organization / account that we would like add the repository to
3. Enter the name of repository
4. Click `Create Repository`
5. Copy the line affixed with `git remote add origin`
6. Navigate to the directory containing the notes (In this demo, the name of the directory containing the notes is `my-notes`)
7. Execute the command below to initialize this directory as a local `git` repository
    * `git init`
8. Paste the command that was copied from `git` (the one affixed with `git remote add origin`)
8. Execute the command below to index all files
    * `git add .`
9. Execute the command below to add all indexed files to staging
    * `git commit -m "I just made my first commit"`
10. Execute the command below to `push` all staged files to the remote repository
    * `git push -u origin main`
    * `git push -u origin master`


# Intro MarkDown Video/Lecture Link
Click [Here](https://drive.google.com/file/d/1T9Hrluz23WVggsZkCkMyawJe3FqZWtFb/view?usp=sharing)