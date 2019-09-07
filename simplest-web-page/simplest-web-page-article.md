# Simplest web page 

## Guides

[MDN Getting started with web development](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

Why not enough:

- does not incorporate modern web practices
- too in depth

[https://www.learnenough.com/](https://www.learnenough.com/html)

Why not enough:

- by topic (HTML separate from CSS separate from HTML, ...)
- paying

Bootcamps:

- [freeCodeCamp](https://learn.freecodecamp.org/)

Why not enough:

- small examples which do not cover the whole

## Philosophy

- just enough to be dangerous
- comprehensive
- driven by questions

## Goal

Lots of people have the need to quickly share some of their information in a way they like. Sadly enough, lots of people are not really familiar with a way to do this.

Of the people who are not familiar with programming but still have the courage to give it a try lots of people give up because their app falls over.

I want to show:

- things aren't hard to learn
- you have to do things structured or they fall over
- it doesn't take a lot of time to make something decent
- making something is fun
- sharing what you make is fun

Showing it doesn't take a lot to build a functioning app that is decently tested. Since I have a QA background I'll put extra stress on the testing part.

Requirements:

- functioning app
- thoroughly tested

Functioning app:

- UI
- API

Decently tested

- E2E tests
- UI tests
- API tests
- continuous integration

What this tutorial doesn't teach:

- UX goes through the window
- security goes through the window

There's freedom in DIY.

Tutorial will follow [MDN documentation](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web) as a guideline but will be different in some respects:

- in this tutorial I don't dwell too much on the inner workings of concepts. Just enough to be dangerous
- broder scope: complete overview of modern web development practices

So in a way this tutorial does less (goes less in depth) and in a way it does more (covers more concepts).

It's not because I don't mention something it doesn't exist. I just don't mention it as not to confuse. However, nothing in this tutorial is not true, it can just be very incomplete.

## Value of this contribution

Existing tutorials:

- [MDN: Getting started with the Web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

I was inspired by these :

- for myself to freshen up concepts
- accessible introduction with questions
- start from absolute basics and improve
- integrated with modern best practices
  - testing
  - version control
  - automation system

E.g. MDN documentation doesn't mention testing.

Doesn't just introduce concepts, goes through the reasoning why they're needed and how things are related. Based on my own experiences.

[Other tutorials exist](https://meiert.com/en/blog/minimal-web-development/) but they often go already too much into detail (beginners don't care about ES6, ES7 or ES8 but just about making something work)

## First step

### Holy Trinity

Starting from a blank page is always hard. Let's think about what we want our web page to accomplish.

```
create and share content
```

In web development there's something called the Holy Trinity of HTML, Javascript and CSS.

- HTML structures content
- Javascript is used to modify that HTML
- CSS describes how the HTML content should be presented

As you may have noticed above, in the Holy Trinity both Javascript and CSS refer to HTML. So that makes you think: could we create a web page with only HTML? Well, yes!

### HTML-only

From [MDN HTML basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics):

**HTML = elements**. Elements wrapped or enclosed or in whatever constellation but in the end it's just elements. HTML elements are like atoms.

How do we know which elements we can use? There's an organisation called w3c which has standardized what elements can be used. A reference of all these elements can be found [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

We open the html candy shop mentioned above but there's so many choices! There are elements related to text (e.g. `<p>` for paragraphs), elements related to multimedia (e.g. `<img` for images), for forms, for buttons, whatever you can think of.

Let's stick to text for now. We create a html document called `html-only-page.html` and within we put a single paragraph element:

```
<p>I am a paragraph</p>
```

If we now open the html file with a browser like Chrome, you'll see the browser will display the text we want. The html file contains nothing more than a single element with some text but that's already a web page!

Interesting to note is the browser doesn't just display `<p>I am a paragraph</p>` but interprets the elements. It doesn't display the paragraph tags because it know `<p></p>` means we want to display just the text.

### Deployment

Now we have a web page we're ready to share it with the world. Now the `index.html` file is just a file on our computer and of course nobody else has access to our computer.

If we want to share it we need a server. The server will take care of requests by other browsers. Basically some browser will ask the server to give it the web page and the server will [give it](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works). We could make our own computer the server but that would mean it has to be on 24 hours a day. It's clearly better to use an external server provider.

The most popular choice to host static html pages like the one we just created is to use [GitHub Pages](https://pages.github.com/). However, to use GitHub Pages you need both knowledge of the command line and Git.

The command line is a [text interface](https://www.codecademy.com/articles/command-line-commands) for your computer instead of the graphical user interfaces (GUI) most of us are used to in daily life (for example the Spotify app is a graphical user interface). To use it effectively you need to know some basic commands which would be too much for a tutorial like this.

Git is a kind of computer language which helps tracking changes between files. It can be used in a command line or GUI way but in the end the concepts needed to use it effectively would be outside the scope of this tutorial.

There are other options like [surge](https://surge.sh/) which has the benefit you don't need a version control system like Git but you still need to know your way around the command line.

So in the end the best option for us now turned out to be [Neocities](https://neocities.org), the successor of Geocities (fittingly known for its 90s looking sites which is exactly what we're aiming for here).

To use Neocities to host your `index.html` file you need to:

- open a Neocities account
- go to the [Neocities dashboard](https://neocities.org/dashboard)
- add the `index.html` file to Home
- open your site

### What you did

#### Learn HTML elements

You got to know HTML, the most fundamental building block of the web. In essence most of web development is just changing HTML elements in one way or another. Difference with what we just did is instead of manually changing the HTML elements in some files, the HTML elements are changed dynamically (for example with Javascript).

But so even these dynamic sites in the end just deal with HTML elements. There can be lots of layers of complexity built on top of it but in the end the basics are easy to understand. And that's reassuring. Things get only easier from here on.

#### Deployment

You learned how to share the web page you created with others on a server. Manually doing it on Neocities isn't the best way to do it but it got the trick done, the site is there and people can open it!

### What you didn't do

#### Static site

The Holy Trinity consists of HTML, Javascript and CSS. This tutorial didn't touch Javascript or CSS. The use of Javascript determines the difference between a static and dynamic site. The difference between static and dynamic lies in the moment the HTML is created:

- static sites generate all the HTML on the server and then hand it over to the browser
- dynamic sites change the HTML after they received it from the server

For example say you want a button on your site which remove some text when you click on it. Removing the text is changing the HTML so you need a dynamic site (with Javascript) to make this work

### Surge

No need to create account, just type `surge` in terminal, follow instructions and open link.

### Git

So in order to deploy we have to make a small detour to Git.

To work with Git we can either use an application or the command line. Although using an application seems the easiest way it's actually the hardest way. If you use git it's important to know what is really happening and I find it's hard to see that with an application.

We use Git because it helps tracking changes between files. It also helps us to save our code safely on a server, so not on your own computer.

The most important thing to know about Git is the [different stages a file can be in](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository).

All we want to do is put our files on a server so we'll need to do the following:

- install Git
- create a GitHub account
- create a repository
- clone the repository
- add changes to staging
- commit changes
- push changes to server

Installing Git [depends on the operating system](https://www.atlassian.com/git/tutorials/install-git) you're using.

Cloning means you copy the code that's on the server to your own computer.

### Summary

HTML = elements.

Browsers interpret elements.

Git helps saving our code on a server.

## App

I was reading `Three Men in a Boat`, thoroughly liking it, and this book by Jerome K. Jerome contains lots of memorable quotes. So let's do humanity a service and make these quotes more readily available.

You can ask up to 3 quotes but not more (too much is too much). If

### Frontend

Actually, most of the times I skip the CSS part. I made a few web apps and all of them have that most distinctive 90s look. I prefer to call that a serious look but I was told several times it's "butt ugly". De gustibus et colorbus. So for the sake of simplicity in this tutorial I will forsake the Holy Trinity (in the Middle Ages that would make me end up at the stake, in modern times you just get harassed by UX designers which is a far better fate) and stick to [Duality](<https://en.wikipedia.org/wiki/Holy_Spirit_(Christian_denominational_variations)>).

### Backend

- server
- application
- database

## Testing

- ask for quote
  - you get quote text and author
- can't ask for more than 3 quotes

## Challenges

It's hard to explain something as easy as possible. For example Git is very useful and even necessary if you want to use GitHub Pages but you can't explain how to use Git without explaining some basic like the file type changes.

Difficult to avoid Git or command line for deployment.

[Neocities](https://neocities.org/): <3 Geocities
Surge: uses command line
GitHub Pages: uses command line + Git

Installation instructions can quickly go way too much in depth if you have no idea of what the reader is using.
