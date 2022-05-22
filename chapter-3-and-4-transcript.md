00;00;05;02 - 00;00;17;25
Ren Estep
Hi and welcome to the Imagine Dat podcast where we explore software development concepts I'm Ren Estep, a software engineer who likes coding, drawing and running like a snail.

00;00;18;02 - 00;00;24;15
Milu Franz
I am Milu Franz also a software engineer who enjoys learning something new every single day.

00;00;25;11 - 00;00;57;14
Ren Estep
Our current season will take the format of a book club where we will be reading 99 Bottles of OOP by Sandy Metz, Katrina Owen and T.J. Sturgess. This book follows the 99 bottles problem where you build and transform your solution as you go with clean code and best practices in mind. There is a link in the show notes as to where you can buy the book. Today we'll be discussing chapters three and four.

00;00;57;27 - 00;01;45;15
Ren Estep
These chapters guide us on how to implement a new requirement and our existing code by refactoring using the flocking rules. I'm going to start with chapter three, which is titled Unearthing Concepts. Hi Milu. So we both have experienced frequent changes in requirements. What do you think the idea of getting your code in an open closed The solid design principles state before adding the new requirement So let me let me just let me just preface this.

00;01;46;13 - 00;01;47;03
Milu Franz
Yeah, go for it.

00;01;47;09 - 00;02;31;26
Ren Estep
The open close friend principle is the O in the SOLID acronym. It's considered... SOLID is considered a collection of well known principles in the world of object oriented design. And the open close essentially means that your code lives in a state that can be expanded open. But shouldn't it be manipulated closed, right? Mm hmm. And, well, I'm not going to lie.

00;02;32;11 - 00;02;38;03
Ren Estep
I kind of really like this principle It's really clean and straightforward.

00;02;41;26 - 00;03;04;28
Ren Estep
So you write your code in a way that you can add to rather than change. Right. Did Now, do I actually do this? Um I try. I definitely try, but I'm definitely not always successful. What about you, Milu?

00;03;06;18 - 00;03;32;08
Milu Franz
Well, I really like this idea as well. Open for extensions and close for modifications. That's how I kind of remember it. And I actually think you and I probably have been intuitively doing this when refactoring some of our code already. However, this chapter kind of shine some light into this concept that I just never really pay attention to.

00;03;33;10 - 00;03;54;01
Milu Franz
So I feel like I'm more aware of it now, and I want to purposely apply it every time I need to refactor my code. But yeah, I do. I actually do it right now. Sure. Maybe some. But I love that we touch these in this chapter. Like I feel like it's going to make me a better developer after applying these for sure.

00;03;57;07 - 00;04;10;29
Milu Franz
So I actually really, really enjoy this chapter in both of these chapters. How do you feel about refactoring code using the flocking rules? Have you heard of these rules before or have you used them in your workflow?

00;04;13;13 - 00;04;59;13
Ren Estep
So I like how simple the rules are, right? They are a very linear, linear cycle, kind of like lather, rinse, repeat. But in this case, we find What's it like? Then we find the smallest difference in those items that are alike. Then we make the simplest change to remove said difference. And then test and then repeat. If you didn't get it on the first try right which let's be honest, probably won't get our first try.

00;05;01;05 - 00;05;36;23
Ren Estep
That means then I really hadn't heard about these rules before. And I also tend to use the word refactor for like every little change that you make right after learning about the solid principles and the flocking in rules. I think I'm going to try a little harder in writing my codes and my code and stepping through four factors.

00;05;38;08 - 00;06;10;22
Milu Franz
Yeah, honestly, this is this was also my first time learning the flocking rules, and I truly love the concept repeating three simple steps to achieve refactoring your code, but also discovering what is the best way to add your new changes. As you do so. Kind of genius. I think this concept also helps whenever you feel a bit over overwhelmed with new requirements.

00;06;11;01 - 00;06;35;03
Milu Franz
I'm not sure about you, but I sometimes get that feeling when the changes are dramatically different. Where I don't even know where to start. Like I really have to analyze the situation and really kind of think about the problem. I feel like this is a great method to kind of jump in and chip away at the problem instead of kind of getting overwhelmed with it.

00;06;40;11 - 00;07;30;22
Ren Estep
I agree on that. That being said, chapter three let's let's culminate on what lessons you grabbed from this chapter the most Let me so hilariously, I don't know if this is a lesson learned, but at least the coolest thing I learned from this chapter is why they call this locking rules, blocking rules. It comes from bird flying patterns like the the swallow murmuration.

00;07;30;29 - 00;08;14;23
Ren Estep
Right. So essentially the flock is guided by small decisions by each participant in the flock. This leads to the goal of the flock in rules Complex behavior emerges from repeated simple rules. That that's probably the coolest thing that I learned and it'll probably go live in my useless knowledge bank ever. That comes up in the land of trivia.

00;08;15;18 - 00;08;17;25
Ren Estep
What about you?

00;08;18;17 - 00;08;48;16
Milu Franz
Yeah, I definitely thought the background on this naming was interesting and cool. And, yeah, I really agree with. Does it? I feel like that was a good lesson for sure. I think something that stayed in my mind about this chapter is how we usually think solutions are crafted by intention as whenever you get a problem to solve, you look at the code, understand abstraction, and jump to implement the solution.

00;08;49;05 - 00;09;28;06
Milu Franz
And I think that is how I've always looked at how to solve a problem. However, this book offers an alternative, but it takes many small, iterative steps and results in a solution that is discovered by refactoring. But you don't have the solution. You discover it by following these rules. So I definitely want to change my mentality and start applying the rules in my day to day Also, I think I borrowed a few a few pointers, but I that I wrote down on my notes while reading this chapter.

00;09;28;27 - 00;09;49;03
Milu Franz
One of them was change only one line at a time. I thought it was important because sometimes whenever I get feedback or click on an M.R. or I get like an extra task, I kind of take all of them and I do everything. And then when something fails, it's like. And so I feel like that was a good line.

00;09;50;12 - 00;10;08;00
Milu Franz
The second point there was wrong the tasks after every change. So I think it's a good, good advice. And if you go ahead and do and make a better change, I feel like that was a simple advice. Nevertheless, very good All right.

00;10;08;27 - 00;10;45;27
Ren Estep
So since we've mentioned our lessons in chapter three and this was jump into chapter four, which is titled Practicing Horizontal Refactoring So did you find the guidelines to find or create a name for an elusive concept? Helpful would what are your thoughts?

00;10;47;21 - 00;11;13;25
Milu Franz
So the struggle to come up with a good name for an abstraction is a real problem for me. So I really appreciate that they touched on this issue. I like that the author gave us pointers such as grouping what you are going to refactoring a table and ask the question, what would the column header be? I feel like this technique is simple but definitely useful.

00;11;14;23 - 00;11;39;08
Milu Franz
I also liked how they gave these guidelines whenever you don't know what to name your abstraction. They said you could think about it for 10 minutes, and if you can't think of anything in 10 minutes, give it a placeholder name and move on. Once you know more about what you're solving you are more likely or it's going to be easier to name it, which I think is true.

00;11;39;26 - 00;11;54;20
Milu Franz
And then if you can't come up with anything, ask someone in the team who is better with names, which I laughed a little bit because I feel like you always there's always one person in your team who is good with words. So definitely not about advice.

00;11;58;02 - 00;11;58;27
Milu Franz
What about you, Ron?

00;12;00;18 - 00;12;35;08
Ren Estep
So, so far in this book, of all the concepts we've learned, this is the one that was probably easiest for me to grasp I guess I would be that person on your team. That's good with words. I've always I've always had a knack for naming things. But I did like the thinking around using the responsibility of the element to help in naming rather than the.

00;12;37;02 - 00;13;08;15
Ren Estep
They offered up a guideline around thinking about the like the pronoun of it. But you know that that can make you jump to different conclusions before. So like having that there. But also considering the responsibility was I feel like a good guideline to kind of follow or at least help in creating your names. The placeholder also is always nice I'm trying to think of like the common placeholder.

00;13;08;15 - 00;13;16;08
Ren Estep
If I can't get it like right away. I think my common placeholder is usually like, come back to me.

00;13;18;02 - 00;13;18;11
Milu Franz
Yeah.

00;13;18;12 - 00;13;22;18
Ren Estep
So like I just search that and then like immediately pop back.

00;13;23;25 - 00;13;50;10
Milu Franz
That is a great advice. Kind of using the same placeholder. So you so you have like a rule for yourself because or before you make a merge request, you just look for that make sure there's nothing that has a name. That's what I do with like whenever I log things in my code, I put bracket debug in capital letters and close bracket and that's like my rule before and my I always look for that and I always find the logs.

00;13;51;28 - 00;14;09;15
Milu Franz
But anyways, what did you understand about the list of substitution principle and how to apply it when refactoring? Also, have you ever committed a list of violations OK.

00;14;10;12 - 00;15;05;08
Ren Estep
First off, the acronym for the list Gas Substitution Principle is LSP, which is one of my fave characters from Adventure Time. I don't know if you've seen that show, but she is she is on point That was my first thought in learning about list substitution principle. But then as I read more and more about a list LSP the concept of having H, so like the it came up in the reading, the concept of having trustworthy return information so that you didn't have to like test your return information to make sure you know how it functions or how it how it should function.

00;15;05;26 - 00;15;25;17
Ren Estep
Reminded me a lot of TypeScript. So well, like in TypeScript you shouldn't because you define your return type. You shouldn't have to test on what's being returned to continue in your functionality. Right.

00;15;28;09 - 00;16;09;09
Ren Estep
But JavaScript is inherently a dynamic language and variable variable values have the ability to change all willy nilly and LSP is like, if this object is promising it's a string, then it should be a string. And I get that I totally get that and I totally get TypeScript, right? Like, don't say you're a dog when you're clearly a duck.

00;16;14;02 - 00;17;01;15
Ren Estep
But so the concepts there, I think that my understand doing in the weirdest way possible. But in my case, I have because I work in TypeScript, I rarely run into the use of Lisp in refactoring or initially writing because you know, I should be, I should be writing in the correct type case anyways. But you know how we like to do and just throw in is anywhere and just as you go in and come back to it fix it don't do that.

00;17;01;16 - 00;17;06;00
Ren Estep
Obviously if you're listening at home, don't do that.

00;17;09;28 - 00;17;40;01
Ren Estep
So but the thing is, is like when I go and I play around with regular old JavaScript, I generally mess typing up or LSP. Right or like because I work in TypeScript, I'll also just start writing JavaScript in like in like a code pen or something. I'll start writing just regular JavaScript and then like try to type something.

00;17;40;20 - 00;17;41;14
Milu Franz
Really. Yeah.

00;17;41;15 - 00;18;20;29
Ren Estep
Oh, right. I'm not writing TypeScript, but also I know for I know for a fact that when I started to learn JavaScript, I definitely committed violations because like, I thought it was the coolest thing, that JavaScript is a dynamic language So like the fact that my variable could be a string or a boolean was like so neat So yeah, I still think it's neat.

00;18;21;11 - 00;18;50;01
Ren Estep
I like that. I like that JavaScript is a dynamic language however, I understand that LSP TypeScript, which I imagine TypeScript is based off of this LSP principle. So I would definitely say principle I understand that it's much cleaner and there's less of a likeliness that your code is going to break.

00;18;50;28 - 00;18;52;18
Milu Franz
If not definitely more reliable.

00;18;53;21 - 00;19;08;04
Ren Estep
So now that I've ranted on about all kinds of fun stuff about LSP, what about you How are you feeling about Lisp?

00;19;09;05 - 00;19;47;16
Milu Franz
Well, I thought you had great points. So I'm currently using TypeScript as well. But also go and they're both a strongly typed languages so that LSP roles and apply as much as what dealing with JavaScript, like you mentioned, However, I've come across instances where I've declare a parameter as a number or a string, which I'm not sure if that's like got was probably like a super small, but depending on what I had to do with the return data data, I will have to identify which type it is to continue with whatever action I'm going to take.

00;19;47;28 - 00;20;14;06
Milu Franz
So after reading this chapter and they pointed out this code smell I, I don't know, it just kind of like opened my eyes and I'm like, why have I done that? Why am I doing that? Maybe I need to like pay close attention to the clearing, you know, parameters that could be multiple types. So yeah, these are this part of the chapter definitely opened my eyes.

00;20;15;04 - 00;20;25;22
Ren Estep
That's when you build your own interface, the type interface or your own type Yeah, just joking. Don't do that.

00;20;30;08 - 00;21;25;05
Ren Estep
So while there were lots of concepts that we got to learn in chapter three and four, we were still learning those through examining the shameless green solution. So I guess my question is how do you feel about the final abstracted solution versus the original? Good enough. Shameless. Green solution. My thoughts I was thinking that it was very interesting to walk through the refactoring process using less locking rules and going from the switch statement to the one very dynamic phrase.

00;21;25;20 - 00;21;46;29
Ren Estep
So I thought that was pretty cool. And being able to see there are naming process in play was like super readable and understandable. What about how are you feeling about it?

00;21;47;29 - 00;22;33;21
Milu Franz
I agree I think seeing the changes and step by step was definitely helpful. The final abstraction or like that dynamic phrase that you're calling, it definitely feels like a more robust solution with a lot less code repetition. I compare it to the shameless green solution, right? And like you said, that abstraction names the words that were chosen made the code so readable So I feel like the obstruction solution they offered with these two chapters, what was really good was better than what I way better than what I put together before we started reading the book.

00;22;33;22 - 00;22;45;27
Milu Franz
Like, I, I kind of love seeing that transition Yeah, for sure. So what are the lessons you got from reading chapter four?

00;22;48;29 - 00;23;27;01
Ren Estep
Oh, honestly, and I think you mentioned this about in the previous chapter because it's like it's kind of like a weird iteration is running the tests between each change in the refactor. And I have the tendency to wait till the end of whatever I'm doing which if anything is broken, it's a whole mess of walking backwards. Right.

00;23;30;24 - 00;23;31;11
Milu Franz
For sure.

00;23;31;19 - 00;24;10;01
Ren Estep
Yeah. That the whole concept of testing after you make a change reminds me, it's and I don't know if you ever had to experience this, but because of my background in Fine Arts when I was learning how to use Photoshop was in like 2,001st learning how to use Photoshop is probably like 2006. And did you know that autosave was not a thing Yeah.

00;24;10;18 - 00;24;13;17
Milu Franz
I did not know yeah.

00;24;13;18 - 00;24;32;10
Ren Estep
So like when I finally got to teaching is studio digital studio classes like at that point autosave was a thing, but like in all of my instructions, it was like every after every step in the instruction, it was like save.

00;24;34;27 - 00;24;56;07
Milu Franz
Well, actually, I thought you were going to say that you did not say stop or you did not separate changes in layers because I know when I've used Photoshop in the past, like I for some reason, like I started doing layers and I kind of forgot and I made all these changes and then I did something that it was like, Oh no, that doesn't look right.

00;24;56;24 - 00;25;06;17
Milu Franz
But then I can now go back because I don't know when with that change in like the history of changes and I don't have my stuff in layers. I thought about example you were going to game, but I feel like they're both they're broken.

00;25;08;19 - 00;25;29;10
Ren Estep
No, no, I had a lot of detail work, right? But that's, that's besides the point. But it just, it reminded me of that having to, like, go and like save like every couple of steps because if you didn't, then, like, it's, everything's broken Well.

00;25;29;10 - 00;25;31;15
Milu Franz
Yeah, that's a good analogy. Yeah.

00;25;34;20 - 00;25;51;23
Ren Estep
Like, I know you had a lot of commentary about these being, like, awesome chapters. So, like, I'm curious as to see what your roundup is for chapter four.

00;25;52;27 - 00;26;30;08
Milu Franz
OK, so like, there were a lot of good lessons, but I wrote some quotes from the book to remember, I don't know, they kind of and compares everything I like about these chapters, but I think there are definitely good things to remember. So one of them was best to stay horizontal and concentrate on the current goal. And I believe this was mentioned when the refactoring was happening and they were kind of looking ahead and they were kind of thinking like, oh, what happens?

00;26;30;16 - 00;26;54;02
Milu Franz
Like this is going to happen. We can like we should do these changes anticipating that change. But then they said, no, it's the horizontal concentrator the current task, whatever is coming next, is going to be revealed. And I really like that and I want to focus on that as well. And then the other quote I wrote down was Code is read many more times than it is written.

00;26;54;27 - 00;27;26;04
Milu Franz
So anything that increases and there's a really underneath you not say that word, anything that increases the way you understand this problem will lower costs. So I don't know. I feel like that's crucial. Crucial for any business, crucial for assets developers But yeah, those were like the lessons I wrote down. And I hope to remember So that's all for today's chapter.

00;27;27;05 - 00;27;36;12
Milu Franz
Thank you so much for joining us. Next week, we will be covering chapter five and six. Thank you so much for listening. I.

