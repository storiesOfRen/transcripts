00;00;05;02 - 00;00;17;25
Ren Estep
Hi and welcome to the Imagine Dat podcast where we explore software development concepts I'm Ren Estep, a software engineer who likes coding, drawing and running like a snail.

00;00;18;02 - 00;00;24;15
Milu Franz
I am Milu Franz also a software engineer who enjoys learning something new every single day.

00;00;25;11 - 00;00;48;19
Ren Estep
Our current season will take the format of a book club where we will be reading 99 Bottles of OOP by Sandy Metz, Katrina Owen and T.J. Sturgess. This book follows the 99 bottles problem where you build and transform your solution as you go with clean code and best practices in mind. There is a link in the show notes as to where you can buy the book.

00;00;54;02 - 00;01;35;05
Milu Franz
Today we will be discussing Chapters one and two. Chapter one covers four possible solutions to the 99 bottles problem. The incomprehensibly complex solution. The second one, which is that a speculatively general solution. Also the concrete abstraction And finally, the shameless green solution, which is what we will be mainly focusing on. Chapter two covers test driven development behind the shameless green solution

00;01;35;05 - 00;01;50;02
Ren Estep
All right. So before hopping into the chapters, let's talk about the writing style of this book. From reading, how easy or hard do you think it is to understand the topics presented.

00;01;53;10 - 00;02;12;04
Milu Franz
I thought they were really straightforward. It was really easy to understand the casual and crisp way the chapters were written. I personally really enjoyed the examples and analogies that the authors use through the first two chapters.

00;02;14;01 - 00;02;48;23
Ren Estep
You know, I think I think so, too. I think the language that they use is very conversational, which made things a little bit easier and more comfortable to get into. Also, like the way they explained it was much more in tune to someone who is new to learning the subject. While you could still learn being a senior developer also. It's just super understandable.

00;02;49;23 - 00;03;05;24
Milu Franz
Yeah, I think it's the way they they kind of like broke every explanation in small parts kind of like, why do we take this position and hear all the reasons? So, yeah, I agree completely agree. I feel like anybody could really understand and read this with ease.

00;03;08;13 - 00;03;17;06
Ren Estep
So with that, let's go ahead and jump into chapter one, which is titled Rediscovering Simplicity.

00;03;18;12 - 00;03;33;24
Milu Franz
So to help learn why I'm reading this book, you're supposed to come up with your solution to the 99 bottles problem. And then start reading. Right. Once you have read the chapter, how did you feel about your solution?

00;03;34;00 - 00;04;37;20
Ren Estep
Well Milu, after reading the chapter, I felt like I immediately needed to refactor my solution. Like, total face-palm. First I forgot that there was a helper function and essentially that would have probably made writing my solution go a little bit faster because I essentially just wrote the same thing. Just it would have been faster had I just used the thing that was given to me right But also, after reading the function, or all the solutions, mine was closest to incomprehensibly complex, which I mean is essentially like you've oversimplified it to the point that it is now complex.

00;04;37;27 - 00;04;58;25
Ren Estep
Like, I understand it because I wrote it. Right? But like then if I handed it off to someone else and was just like, "peace out, bro, enjoy that". I should not assume that there would be able to understand that there is a lot of nested conditionals going on.

00;04;58;25 - 00;05;36;15
Milu Franz
Yeah, same same. I only found out there was a helper function after talking to you. So I feel the same way. Like I wasted some time and I could have made my life easier by taking their helper function. But I'm a firm believer of they don't repeat yourself that DRY principle. So I kind of had a similar experience. My solution also resembled the incomprehensibly complex solution they presented, which it was.

00;05;36;26 - 00;06;02;25
Milu Franz
It was interesting. Like you asked or we asked, like, how do we feel about this solution? I felt like it was a great solution. And when they started kind of breaking it apart and it showed me, I mean, it's like I'm rambling a lot, but I it was eye opening really, because I feel like for a long time I, I've been respecting this.

00;06;02;25 - 00;06;17;16
Milu Franz
Don't repeat yourself. Rule a little too hard. So it was really nice to kind of, like, go through why it's not always a good idea to be so strict on not repeating stuff on your code.

00;06;19;20 - 00;06;53;22
Ren Estep
Well, to that, like later, later on in the chapter and reading, they talk about not kind of like not jumping so far ahead. Right. Whereas like I was like, well, this obviously can be this and just move on. Like, I went like ten steps ahead, not thinking that those steps might not be the best.

00;06;54;23 - 00;07;30;21
Milu Franz
Yeah, I agree. I think it's also experience like I think the more we have worked or the more we have worked on code. Like, we know that if we create like a function eventually is going to change in different ways. So we tried to abstract as much that we know we can change. And I feel like like I like this book, like one of the lessons I got from it, which I feel like I'm answering a future question of this episode, but I kind of like the idea of like not going to ahead of yourself and kind of like focusing on solving the current problem.

00;07;30;27 - 00;07;32;04
Milu Franz
That was a good lesson for sure.

00;07;33;10 - 00;07;45;06
Ren Estep
I like that you say you feel like you're answering a future question and then you go, you talk about it not, not, not going ahead of yourself.

00;07;45;06 - 00;08;04;19
Milu Franz
That it's true, little meta. When the chapter came to the conclusion that the shameless green was the best out of the four solutions, what were your initial thoughts and what in the chapter made you go, Yeah, I can see that

00;08;07;02 - 00;08;20;00
Ren Estep
Well. So one of the great things that I'm finding in this book is how well they're putting the concepts of clean code but in like a relatable way. Right.

00;08;22;02 - 00;08;44;22
Ren Estep
So first, evaluating the solutions by asking domain questions. So like putting that into play. If per say, I would have thought to ask domain questions before heading into building out my solution.

00;08;47;19 - 00;08;52;10
Ren Estep
I probably probably would have come to a different solution.

00;08;55;27 - 00;09;48;06
Ren Estep
So and like in the book, they they use those domain questions to kind of evaluate on cost and value which I feel like allows for greater knowledge into your code. But then also after reading each solution, the book covered different ways to evaluate the code, via like different metrics which those were really quite new to me. I had never even really heard about those type of metrics when reviewing code So that was that was a neat thing coming in, especially with clean code practices.

00;09;50;06 - 00;10;34;25
Ren Estep
The drying out only when you need to And also with the shameless green, the, the good enough concept is like you know, sometimes when like especially if you're like you're in a prototyping phase, right? And you have an issue and you're in your GitLab board or in your JIRA board and like it's not it's not super well-defined, but so it leaves wiggle room where you could be like, oh, I can fit this in here, too.

00;10;35;10 - 00;10;47;06
Ren Estep
But then you're like, you know, you should really just answer or like, fix what the simplest problem is. In the issue will.

00;10;48;04 - 00;11;01;07
Milu Franz
Leave and stuff out of scope. Yeah. Yeah, I completely agree. I think that that that's a very good, good point. Definitely good thoughts on this chapter. Did I cut you off? I'm sorry. I thought they were done.

00;11;01;14 - 00;11;07;07
Ren Estep
No, no, you're totally cool. I was going to ask, what did you think?

00;11;08;06 - 00;11;33;25
Milu Franz
So. So the first exercise they shared in the chapter, that's the one that resembled my solution. Right. And I think I just said that before. I know I'm the last answer, but I found it very interesting when these chapter analyzes and points out all the reasons why this is not the best solution and how it adds unnecessary complexity to the code.

00;11;36;16 - 00;12;00;22
Milu Franz
And code is always changing, so it will take longer for the person that will work on it next to understand it, which at cost for your project. It just, I mean, it just it was like a snowball, right? Like kind of taking it to the extreme going ahead of yourself and trying to not have any duplication in your code somehow.

00;12;01;25 - 00;12;03;25
Milu Franz
Snowballed in like.

00;12;03;29 - 00;12;27;26
Milu Franz
Higher cost of the cost for your project and how others will have to or you will have to really explain your solution to someone else. Like how I don't know. It just it just felt like a snowball effect on some of the decisions you will take when solving a problem at the beginning. So, yeah, those are my initial thoughts.

00;12;27;27 - 00;12;31;15
Milu Franz
I'm not sure if this is a good answer for it. I think about it, but it's fun.

00;12;33;16 - 00;12;35;05
Ren Estep
No, I think it's a good answer.

00;12;37;25 - 00;12;40;27
Milu Franz
So what was the coolest thing you learned from Chapter one?

00;12;42;22 - 00;13;20;29
Ren Estep
OK, I mentioned this before, but the good enough concept, so jumping so far head into abstraction is not always the best solution because you don't know what the future holds. But also, like for the beginning of the problem, the shameless green it's simple that sometimes programmers especially senior programmers will be like, that's too simple. There's there's got to be a better solution to this.

00;13;21;10 - 00;13;46;12
Ren Estep
But and it gets laughed off. But like it did cover the problem and it looked clean. It was easy to read. So the good enough concept is definitely a one of the coolest things that I learned from this chapter. Yeah.

00;13;47;02 - 00;14;15;18
Milu Franz
So much like the coolest things that I learn from this chapter are the coolest thing, I think is that everything is a tradeoff. I think that's kind of like, they hit on this point right at the start. And so whenever you're willing to accept increases in the complexity of your code along some dimensions, there's always a cost for it and that everything is a balance right or refactoring until you don't have any repetitive code, probably links to less code.

00;14;15;29 - 00;14;47;12
Milu Franz
Plus looking code, but also not as easy to understand I also really like getting deep into the metrics to evaluate code. You mentioned this before, but like you said, I also I mean, I've heard every source lines of code metric, which I know it's not very reliable, right? Because measuring programmer productivity by counting the lines of code is just not really, I don't know, it just doesn't make much sense.

00;14;48;14 - 00;15;12;26
Milu Franz
But the other two metrics that they mentioned, those were also new to me. And I don't know. I mean, I feel like we should probably try to maybe not every single line of code we write, but I feel like this will be a good metric to apply. Maybe like every every month or every two months like a specific feature or on a merge request.

00;15;13;01 - 00;15;36;20
Milu Franz
See, I don't know, just for fun, I guess. But to see or to measure your code in a way But I think that and I know we haven't really dove deep in what we do, what were these metrics and I don't know if you feel like it will be too long to talk a little bit about them. Like I know I have like a few or like short explanations of what they are.

00;15;38;22 - 00;15;45;17
Ren Estep
No, no, go ahead if you want to if you want to explain them. I will listen up full ear.

00;15;46;02 - 00;16;12;10
Milu Franz
And so I don't know. I mean, maybe everybody that is listening, if someone is listening, maybe they already read the chapters and they already know these. But if they're not and they're just getting a little summary I feel like they could get a little bit of good info here. So one of them was the psychometric complexity metric, which is an algorithm that counts the number of unique executions pass through a body of source code.

00;16;12;20 - 00;16;52;28
Milu Franz
So like it kind of seems like if you have a lot of conditionals, it makes it kind of counts all the path that you will take if you know these values X or Y and what would happen. And the other one, they they mention is the assignments, branches and conditions, the ABC metric, which is another algorithm that counts more than just conditionals, it counts variables, it counts function calls, message sends, which that refers to kind of calling a function and also conditionals as the previous one that I mentioned.

00;16;53;15 - 00;17;15;19
Milu Franz
So this one is a little more robust and a little more reliable and I'm not exactly sure where we could submit our code to get a result using the ABC metric but I definitely want to look it up. I think it will be kind of fun to maybe submit a merge request and see what are the results.

00;17;20;15 - 00;17;46;23
Ren Estep
I think, so, you use react so in and when you use your testing library, it's usually like React test. It's based in Jest right. And I think some of the metrics actually like for your, your testing, getting the percentage on testing, I think they actually will go through at least the assignment branches and conditions.

00;17;47;20 - 00;17;49;10
Milu Franz
Oh, OK. makes sense.

00;17;49;15 - 00;17;58;09
Ren Estep
As in as a count for how many per page or document.

00;18;01;05 - 00;18;24;13
Milu Franz
Yeah, like I'm not sure, but that makes sense because I know like I've been working on testing this past couple of weeks and I know that they can have like react test library or Jest I guess Jest, you know, when you when you see how much coverage you have it can also point out or it points out the lines of code that you haven't covered yet.

00;18;25;00 - 00;18;26;13
Milu Franz
So it's pretty smart.

00;18;27;01 - 00;18;52;13
Ren Estep
Yeah. So moving on from chapter one, we have chapter two titled Test Driving Shameless Screen And as you said in the intro, this chapter was about test driven development.

00;18;57;10 - 00;19;12;07
Milu Franz
This chapter gave you the chills Yes. I think we all know it's a good thing to do, but not many people do it

00;19;12;07 - 00;19;15;09
Ren Estep
Yeah. Yes. Yeah.

00;19;16;01 - 00;19;42;14
Milu Franz
So let's talk about our initial thoughts on chapter two. So chapter two was interesting for me because it goes a step by step on the practice of writing tests before writing code. It I thought it was probably the best explanation of the TDD concept. I know like I studied it in school and I know I've read a few chapters about it in the past.

00;19;44;20 - 00;19;58;15
Milu Franz
But I think if someone is going to get someone that has never used test driven development in the past reads this chapter, it will get it so quickly. I felt like it was it was really good.

00;19;59;15 - 00;20;35;07
Ren Estep
I agree with that wholeheartedly. Like, it was way easier to understand test driven development after reading this chapter. But also like, while, in my day to day practices, my tests may not be written out beforehand. I do have, I do have a user stories which could easily be translated into tests. So like...

00;20;35;07 - 00;21;00;24
Milu Franz
it's it's hard. I mean, I feel like test human development is something that it's really hard to get used to and I will argue that for frontend development, like if you're working with React, it just feels like very to me and I could be wrong but it feels like it will be an impossible practice for me when I'm writing frontend code.

00;21;01;15 - 00;21;21;20
Milu Franz
Like for the backend it feels like yeah, that makes sense because you're, you're creating these functions. I don't know, how to explain it, but for the frontend I feel like you're building these UI and it changes a lot. Like I, I just don't see myself really applying test driven development for react. What do you think, how do you feel about it?

00;21;23;13 - 00;22;11;16
Ren Estep
Well, I, I live in the realm of research and development, prototyping so like our, our concepts for our front end changed drastically from a day to day process, usually speaking. So like a lot, a lot of, a lot of my work is just noodling about in code. So like the test driven development is a little hard or is a little hard in that realm because like my component might completely change and like.

00;22;11;16 - 00;22;16;16
Milu Franz
We kind of like our waste of time, right? And you create tests for it and then they will, they will, even need it the next day.

00;22;17;22 - 00;22;57;04
Ren Estep
I mean, it's still good to create tests for them, but doing it beforehand and then like having that concept where you can even if you like, you know, in your test in test driven development it's like if you, you then write the code that answers the test, right? When you then have a change that needs to happen. In theory, you should be able to inject that into your code without changing the original code.

00;22;57;16 - 00;22;57;27
Ren Estep
Right.

00;23;00;09 - 00;23;04;12
Ren Estep
And then your test doesn't break. It still works.

00;23;06;16 - 00;23;21;20
Ren Estep
And in my projects, that's not always the case because it's like you'll just take the same component, empty it out, and then I have a completely different vibe

00;23;22;08 - 00;23;50;15
Milu Franz
Yeah. OK, so I think that's the difference. Like, you said it really well, so I'm backend I feel like you're testing for functions or functionality, right? So you're like, this is a small function. This is what it's returning because, you know, like, it's very like, this is what it gets this what returns and it is good, no. But works for the frontend or at least would react to testing library is more like the user interactions with the browser.

00;23;50;28 - 00;24;10;18
Milu Franz
And I feel like the UI changes a lot even. I mean, I'm not working on prototype work and it still changes a lot. So that's I think that's why I find it so difficult to create tests before you end up creating the UI. But yes.

00;24;12;12 - 00;24;19;09
Ren Estep
I totally, totally get it. However, it is more understandable now because of the chapter.

00;24;20;16 - 00;24;47;25
Milu Franz
Yeah, for sure. This was helpful. So test driven development works like write test, make it work, make it better, in simplest terms. So essentially this chapter illustrates how to incrementally create tests and then use these tests to drive the development of code. How do you see yourself incorporating what you learned from this chapter into your daily coding practice?

00;24;48;16 - 00;25;20;19
Ren Estep
So I may have jumped ahead on myself earlier, but to reiterate that point, in my daily coding practice, I noodle around quite a bit playing and prototyping, but that doesn't mean that. It doesn't mean I couldn't incorporate test driven development. I think I would just need to be much more aware of it.

00;25;21;09 - 00;25;33;10
Milu Franz
It will take a little more time to, right. I mean, i feel like for prototyping, you guys are going really fast. Yeah, I do feel like testing at it does add a little bit of time to whatever you're doing.

00;25;35;08 - 00;25;44;08
Ren Estep
Yeah. What about you? You you have you have left the world of prototyping and are now in production commercial.

00;25;44;22 - 00;26;23;10
Milu Franz
Commercial production. Commercial production. Yes, yes. And I am using TDD, I'm working on the backend for sure. Which has been a transition. No, I mean, I feel. Like. No. Yeah, it was a change for sure. But it has been a good change. I do feel like because driven development or testing in general, because I wasn't doing much of testing my prototypes either, but it just has helped me to get my functions to be more concise, kind of like smaller units that are easier to test which is nice.

00;26;26;16 - 00;26;39;19
Milu Franz
I find this concept really hard. I well which I just, I mentioned this before, I do find it hard to apply when you're working on the front end because it changes so much as you're creating your UI.

00;26;40;25 - 00;26;53;06
Ren Estep
So out of curiosity, if I interject my question here, what did you think that was the biggest concept that you took away from this chapter?

00;26;53;29 - 00;27;20;10
Milu Franz
I think to write tests that confirm what your code does without any knowledge of how your code does it. I feel like that was like a good way to put it. Because when you're working on tests and you're not as experienced building tests for your code, it can... The question that I kept asking myself was, what am I supposed to test?

00;27;21;17 - 00;28;13;19
Milu Franz
So I feel like these are kind of just testing what your code does if you don't know what it's supposed to do. Like if you were like a third party, I feel like that's the best way to test it. And I really like that lesson from this chapter. And also that tests are not the place for abstraction. And I've actually come across these these past weeks where wherever I'm testing, it's taking all these data in and my brain just kept looking for solutions to like, how can I simplify this data I need to form and my tests, I started to get really complex just because I didn't want to copy and paste some of the data. Right. And so I feel like that was a good lesson for sure.

00;28;14;29 - 00;28;51;05
Ren Estep
I think I think that maybe my biggest takeaway is to keep the to keep each test to a singular item of performance. Yeah, yeah, yeah, yeah. So, like, just, you know, like instead because I'm golly, I know I have tests out there that are like, all right, I'm just going to, I'm going to, I'm going to test I'm going to get everything done.

00;28;51;05 - 00;29;11;02
Ren Estep
In this one test. I'm going to make sure this make sure this button opens this and see if this goes there. And then click this button to make sure that this interaction happens. All in one test. And I'm like probably not the best idea to keep it that way.

00;29;12;16 - 00;29;15;21
Milu Franz
But also, like integration tests. Isn't that like.

00;29;17;00 - 00;29;33;01
Ren Estep
Oh, yeah, yeah, that is true. Like versus a traditional unit test where you're testing a methodology that is part of like the UI unit tests that kind of get like muddled right? Is that.

00;29;33;09 - 00;29;34;24
Milu Franz
Yeah, frontend testing is hard.

00;29;35;14 - 00;30;00;22
Ren Estep
You're, you're doing like you're doing a little, little column A: unit test, little column B: integration because like if you want to test this particular interaction, you may still have to go through like button, click this button, click that. Now this is available. Now I can test that

00;30;00;22 - 00;30;22;05
Ren Estep
Yup, absolutely. I feel like front end testing can get really muddy yeah, for sure. And I've been working with integration tests lately and those are quite long, but they're only testing one thing though. In order to get to that thing. Yeah, it's a bunch of steps.

00;30;23;02 - 00;30;55;27
Ren Estep
Yeah. I feel like it it depends also like upon your, your state management almost with the, with those type of things because like you could in theory componentize the different blocks and then you only have to test test the one interaction. But depending on where your state is managed is whether or not you can actually do that yeah.

00;30;56;22 - 00;30;58;05
Ren Estep
Test driven development.

00;30;59;21 - 00;31;26;28
Milu Franz
I'm interested to hear more about test driven development from others' experiences, honestly. I feel like it's I don't know, I wonder like I feel like you and I feel very similar about, you know, like we have had similar experiences working with prototypes. So maybe that's why or we have worked together in the past. So maybe we have a very similar culture and that's how we feel about it.

00;31;26;28 - 00;31;38;24
Milu Franz
But I am very curious to hear about others and how much testing they have done in the past. And if test driven development has been like their way to go, instead of getting

00;31;38;24 - 00;32;05;12
Ren Estep
Right. Yeah, well, I think I think that's it for today's show. So our next episode will cover chapters three and four, and as a point each episode this season will cover one to two chapters. So thanks for listening.

