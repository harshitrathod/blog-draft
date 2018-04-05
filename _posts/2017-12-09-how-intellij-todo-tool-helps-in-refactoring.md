---
title: How IntelliJ TODO tool helps in Refactoring
date: 2017-12-09T10:10:11+00:00
author: Harshit Rathod
layout: post
feature-img: "assets/img/intellij-todo/bg.png"
tags:
  - IntelliJ
  - Refactoring
comments: true
---
Every developer needs to perform refactoring in his Professional career. You need Refactoring when you feel your code is not maintainable or scalable. With complex design some time is it very hard to develop a new feature and refactoring is essential. Refactoring is a very critical task because it can open a door for bugs.

When I start refactoring, the first thing I do is analyze entire code end to end. I will not code utile I get a good understanding of impact. When I am going through the code I need a way to add comments to a line or method level. This is where IntelliJ TODO tool helps.

### **What is IntelliJ TODO tool?**

It's tool window where you can able to refer all comment which you mentioned in your Tool pattern setting. IntelliJ is continuous scanning project for this TODO pattern and when the pattern matches, display comment on tool window. By default, IntelliJ have two TODO pattern **//TODO** and **//FixMe**.  These matches any comment Starting with **//TODO** and **//FixMe**

To see all your TODO comments open TODO tool windows from **View -> Tool Windows -> TODO or (Alt + 6)**

{: .center}
![TODO Tool window]({{ "/assets/img/intellij-todo/todo1.png" }})

You have all your TODO Comment displayed over here. You have 3 option to limit your scope. It means if you select "Project" scope, scan happens on all project files. For more information, you can refer: [TODO tool Window](https://www.jetbrains.com/help/idea/todo-tool-window.html)

&nbsp;

### How to create Custom TODO pattern?

You can define your own TODO pattern in IntelliJ.Once you add this pattern, IntelliJ scan for this pattern and display matching items in IntelliJ tool window.  Go to **Setting -> Editor -> TODO **for adding new pattern

{: .center}
![Add TODO pattern]({{ "/assets/img/intellij-todo/todo2.png" }})

As you can see we have 2 default pattern already configured. Click on Plus Icon to add new Pattern

{: .center}
![Add new TODO Pattern]({{ "/assets/img/intellij-todo/todo3.png" }})

You need to define Your pattern here. I have configured **\bhello\b.* **which will map all comment starting from hello. You can use [Regular Expression Syntax Reference](https://www.jetbrains.com/help/idea/regular-expression-syntax-reference.html) To define Your Pattern. You can also change the color scheme of comment also. After saving changes you can able to see all your comment starting with **Hello **in TODO tool Window

{: .center}
![View custom TODO comment]({{ "/assets/img/intellij-todo/todo4.png" }})

### TODO comment with Refactoring :

Now we know how to add TODO pattern we can use it in our refactoring. When I start Refactoring I have one JIRA Id for a task. I will create one TODO pattern with this Id. For example, I have 1245 as Jira Id so I create a pattern like **\b1245\b.*.  **After this, I will start my code analysis and when I need to add some points I will add a comment with 1245 in a prefix. Now I can see all comments in TODO tool window.

In a large project, It is possible that you have so many TODO comments. Finding particular comment will become a pain in such situations. You can create your TODO filter so that Only specific comments will be filtered.

### Create TODO Filter:

Go to **Setting -> Editor -> TODO **and click plus to add a filter.

{: .center}
![Add TODO filter]({{ "/assets/img/intellij-todo/todo5.png" }})

Select Pattern which will be included in this filter and save changes. Now on TODO tool window open filter menu.![]({{ "/assets/img/intellij-todo/todo6.png" }}) Select Your filter and your all comment will be filtered by selected pattern.

Now I have all my comment filtered, I can work on my code to resolve it. Now It's easy to go to impacted code through TODO tool. I also can track how much work is pending by a number of comments in TODO tool window.

When I am done with refactoring and committing my code, I can select  "**Check TODO**" options in my "**Before Commit"** section. What it will do is scan all files and check if any TODO item is pending or not. You can also apply a filter to scan particular pattern.

{: .center}
![Scan TODO while Commit]({{ "/assets/img/intellij-todo/todo7.png" }})

### Conclusion:

I developed this technique over the time while working on many refactoring tasks. This is like creating my refactoring checklist which tracks my progress. By doing this systematically we can reduce the probability of bugs.

I am happy to have some feedback to improve this technique further!
