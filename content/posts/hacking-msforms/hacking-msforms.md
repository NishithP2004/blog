+++
title = "Hacking Microsoft Forms"
date = "2021-12-29T10:00:00+05:30"
author = "Nishith P"
authorTwitter = "NishithP2004" #do not include @
cover = "https://miro.medium.com/max/1400/0*tj0vXkPS5NPeU9sw.png"
tags = ["Bug Bounty", "MS Forms", "Ethical Hacking"]
keywords = ["Hacking MS Forms", ""]
description = ""
showFullContent = false
readingTime = true
hideComments = false
Toc = true
+++

# Hacking Microsoft Forms

![Microsoft Forms](https://miro.medium.com/max/1400/0*tj0vXkPS5NPeU9sw.png)

From the growth of Online learning during this pandemic — students, researchers have been on a hunt for hacks on **Microsoft Forms** which could give them an unfair advantage in their tests, pop quizzes etc.

There have been many on YouTube who have claimed to have found such _treasures_ by inspecting the source code, trying other tricks, etc but it's all just clickbait to attract viewers.

What I am going to share today will change all that…

As all of you may have read from the subject line of this story, yes I have found a way to **_hack_**  Microsoft Forms but its not quite what you may expect —

# Summary

*   Whenever a form is submitted, an API POST request is made to the **_/formapi/api/${API\_Key}/users/${User\_Key}/forms(${FormID})/responses_** endpoint
*   By intercepting the POST request, a user/attacker can put a new entry / null string, thereby bypassing the required field / adding a new option completely.
*   Due to the absence of Server-side checks, the same reflects in the forms responses available to the form owner.

# Intercepted Payload

```json
{“startDate”:”2021–12–02T18:38:36.784Z”,”submitDate”:”2021–12–02T18:38:40.820Z”,”answers”:”\[{\\”questionId\\”:\\\[REDACTED\]},\\”answer1\\”:\\${New Option} OR null \\”}\]”}
```

# Summary — Translated For Layman

*   When a user submits a form, the webpage / the form (Client) sends a message to the server saying that this user has submitted “X” as the response for a particular question with a **unique id** “Y” and the server saves the same in its database which is made available for the form owner to view as the responses.
*   By acting as a middle man and intercepting the message, the attacker can change the message sent by the webpage to say that the particular user has sent “Z” as the response for a particular MCQ based question where Z is _not in the options available_ / is an **invalid** input.
*   Due to the absence of server-side checks to confirm whether the option is one of the valid options, one can manipulate **Ratings**, **Net Promoter Scores**, and also add a new Option in an **MCQ / Checkbox / Dropdown** based Question.
*   The same gets saved in the Database and is sent to the Form owner as a part of the set of responses.
*   One problem with this attack that limits its impacts is that the attacker can manipulate only his / her response and not other users responses.

# Attack Scenario

*   When corporates use this form for their internal competition for employees, any misuse may bring in reputational issues for the corporates and in turn, it will harm Microsoft’s brand image,
*   Large corporates running a certain campaign for the public through these forms can face huge revenue loss and reputational harm if there is scope for misuse through options beyond the listed ones.
*   Microsoft forms are predominantly used in schools for the conduct of examinations. Any potential attack or misuse can play havoc with students’ lives and can cause irreparable loss for the students and their families.

This Bug affects both quizzes and normal Forms.

# Steps to Reproduce Bug

*   Create a new Form on MS Forms.
*   Open the Form.
*   Follow the steps as shown in the POC attached below.

# PoC (Proof Of Concept)

[![Proof Of Concept](https://img.youtube.com/vi/rg2zylBbxUQ/0.jpg)](https://www.youtube.com/watch?v=rg2zylBbxUQ)

**_Disclaimer_**_: By reading this article, you agree to use this information only for educational purposes and not to cheat in your tests/pop quizzes and I, as the author of this article, take no responsibility for any ill practices from your end._
