# Communicating with markdown 

GitHub is about more than code. It’s a platform for software collaboration, and [Markdown](https://docs.github.com/en/get-started/learning-about-github/github-glossary#markdown) is one of the most important ways developers can make their communication clear and organized in issues and pull requests. This course will walk you through creating and using headings more effectively, organizing thoughts in bulleted lists, and showing how much work you’ve completed with checklists. You can even use Markdown to add some depth to your work with the help of emoji, images, and links.

## Overview

In this activity, you will be able to use markdown to:

- [Add headers.](#headers)
- [Create links.](#links)
- [Include images.](#images)
- [Quote code examples.](#code-examples)
- [Create lists and task lists.](#lists-and-task-lists)

## Steps

### Headers

**What is _Markdown_?** Markdown is a [lightweight syntax](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) for communicating on GitHub. You can format text to add a heading, lists, **bold**, _italics_, tables, and many other stylings. You can use Markdown in most places around GitHub:

- Comments on [issues](https://docs.github.com/issues/tracking-your-work-with-issues/about-issues), [pull requests](https://docs.github.com/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests), and [discussions](https://docs.github.com/discussions/collaborating-with-your-community-using-discussions/about-discussions)
- Files with the `.md` or `.markdown` extension
- Sharing snippets of text in [Gists](https://docs.github.com/github/writing-on-github/editing-and-sharing-content-with-gists/creating-gists)

**What is a _header_?** A header is a larger bit of text at the beginning of a section. There are six sizes.

```md
# This is an `<h1>` header, which is the largest

## This is an `<h2>` header

###### This is an `<h6>` header, which is the smallest
```

The previous code would look like this: 

# This is an `<h1>` header, which is the largest

## This is an `<h2>` header

###### This is an `<h6>` header, which is the smallest

The README.md file of your repository should already have an **h1** header. Modify the README.md file as follows to include different headers:

1. Include an **h2** header titled **Description**.
2. Move the description of the repository under the **h2** header, and add a little more text to it.
3. Add an **h2** header titled **Contents**. You will later add **h3** headers with the contents of your repository.
4. Add an **h2** at the end of the file titled **References**. We will add links later.
5. You can preview the markdown you wrote if you click on **Preview** next to the **Edit** button.
6. Make a commit of the file. Remember to add a meaningful commit message.

### Links

You can create an inline link by wrapping link text in brackets [ ], and then wrapping the URL in parentheses ( ). For example:

```md
[Git pro book](https://git-scm.com/book/en/v2)
```

Looks like: 

[Git pro book](https://git-scm.com/book/en/v2)

#### Tasks

Add the following links to the **References** section of your README.

1. Github documentation: https://docs.github.com/en
2. Github glossary: https://docs.github.com/en/get-started/learning-about-github/github-glossary
3. Git documentation: https://git-scm.com/doc

### Images

You can display an image by adding ! and wrapping the alt text in [ ]. Alt text is a short text equivalent of the information in the image. Then, wrap the link for the image in parentheses ().

For example, the next code:

```md
![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, 
of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)
```

looks like:

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)

You can display an image from your repository, add a link to an online image, or upload an image. For more information, see "[Uploading assets](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#uploading-assets)."

**Note**: When you want to display an image that is in your repository, use relative links instead of absolute links.

Here are some examples for using relative links to display an image:

| Context |	Relative Link |
| --- | --- |
| In a .md file on the same branch	| /assets/images/electrocat.png |
| In a .md file on another branch	| /../main/assets/images/electrocat.png |
| In issues, pull requests and comments of the repository |	 ../blob/main/assets/images/electrocat.png?raw=true| 
| In a .md file in another repository |	/../../../../github/docs/blob/main/assets/images/electrocat.png |
| In issues, pull requests and comments of another repository |	../../../github/docs/blob/main/assets/images/electrocat.png?raw=true |

**Note:** The previous table was made using markdown. You can check the raw markdown of this file to see how it was made.

For more information, see "[Relative Links](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#relative-links)."

#### Tasks

Follow the next steps in your repository:

1. Add an **h3** header to your **Contents** section titles **Images**.
2. Instead of creating a new file in your repository, upload an image to the repository.
3. Modify the README file, and include the image to the file after the Images section you just created. 
3. Make a commit to the file.

### Code examples

You can call out code or a command within a sentence with single backticks. The text within the backticks will not be formatted. For example, the following text:

\```
git status
git add 
git commit
\```

would look like:

```
git status
git add
git commit
```

In addition to code blocks, some code blocks should be rendered differently depending on the language, such as JavaScript or command-line text. For example:

\```python
print("Hello world")
\```

```python
print("Hello world")
```

\``` javascript
const myVar = "Hello, world!";
\```

```javascript
const myVar = "Hello, world!";
```
For more information, see "[Creating and highlighting code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)."

#### Tasks

Follow the next steps in your repository:

1. Add a **h3** header to your **Contents** section titled **code examples**.
2. Add a snippet of code for a python program that adds two numbers.
3. Commit your changes.

### Lists and task lists

You can make an unordered list by preceding one or more lines of text with -, *, or +. For example, the markdown:

```md
- Item 1
* Item 2
+ Item 3
```

looks like:

- Item 1
* Item 2
+ Item 3

To order your list, precede each line with a number. For example, the markdown:

```md
1. Item 1
2. Item 2
3. Item 3
```

looks like:

1. Item 1
2. Item 2
3. Item 3

You can create a nested list by indenting one or more list items below another item.

```md
1. Item 1
    - Subitem 1
    - Subitem 2
    - Subitem 3
2. Item 2
3. Item 3
```

1. Item 1
    - Subitem 1
    - Subitem 2
    - Subitem 3
2. Item 2
3. Item 3

To create a task list, preface list items with a hyphen and space followed by [ ]. To mark a task as complete, use [x]. For example, the markdown:

```md
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete
```

looks like:

- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete

#### Tasks

Follow the next steps in your repository:

1. Create a **h3** header in the **Contents** section titled **lists**.
2. Create a task list with the next items:

```md
Turn on GitHub Pages
Outline my portfolio
Introduce myself to the world
```

3. Make a commit with your changes.

## Finish

After you finish this activity, you should know:

- Have a better understanding of markdown.
- Use markdown to format a page with headers, links, images, and lists.
- Make commits inside github.

## Resources

- [Github markdown guide](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)