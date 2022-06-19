00;00;05;02 - 00;00;17;25
Ren Estep
Hi and welcome to the Imagine Dat podcast where we explore software development concepts I'm Ren Estep, a software engineer who likes coding, drawing and running like a snail.

00;00;18;02 - 00;00;24;15
Milu Franz
I am Milu Franz also a software engineer who enjoys learning something new every single day.

00;00;25;11 - 00;00;48;19
Ren Estep
Our current season will take the format of a book club where we will be reading 99 Bottles of OOP by Sandy Metz, Katrina Owen and T.J. Sturgess. This book follows the 99 bottles problem where you build and transform your solution as you go with clean code and best practices in mind. There is a link in the show notes as to where you can buy the book.

00;00;54;01 - 00;01;08;09
Milu Franz
Today we will be discussing chapter five and six. These chapters take us farther down the rabbit hole of refactoring, exploring concepts in extracting classes and polymorphism.

00;01;08;09 - 00;01;37;28
Milu Franz
Right on. Right on. That is what we are doing. Chapter five entitled Separating Responsibilities is just a continuation of refactoring from Chapter four. Really. We had mentioned in chapter four before getting in there that like after analyzing where is a good place to like separate our code and that's kind of like takes us down that that path, right? So

00;01;37;28 - 00;01;41;01
Milu Franz
absolutely

00;01;41;01 - 00;01;49;10
Ren Estep
So going into this chapter, as I said, refactoring was already a big topic discussed in the previous chapters.

00;01;51;11 - 00;02;26;05
Ren Estep
Earlier, focusing on the flocking rules and the DRY principle. In this chapter, we begin the journey to making our code open for extension, and one of the first topics covered is getting better at identifying patterns in code by being better at identifying code smells. How would you rate or describe your abilities and identifying code smells.

00;02;27;25 - 00;02;58;19
Milu Franz
That is such an interesting question. And I guess I don't really have a good answer for you. I'm not sure, but I think I'm definitely in the lower range I guess before reading this chapter, I will. I think I would probably have chosen a higher number before reading this chapter But when we went through the questions to identify patterns, I realized I don't ask myself a lot of these questions.

00;03;00;04 - 00;03;25;03
Milu Franz
For instance, do arguments of the same name always mean the same thing? This question, which is seems so basic and it actually so powerful. I don't think I've ever asked myself that Then another question they mention was, do any methods have the same shape? I've never really paid attention to like the shape of the function. Looking at it or squinting looking at it.

00;03;26;15 - 00;03;41;10
Milu Franz
I just didn't know that was a thing. So, yeah, so this chapter made me realize that there is a long journey to get good at identifying code smells. What about you?

00;03;47;12 - 00;04;32;24
Ren Estep
If I were an honest person, which I am, I would definitely say that I need more experience finding code smells or even just knowledge around code smells because like, there's a few that I know, but if I. If I were to rate my knowledge on code smells from one to ten, one being the worst, ten being the best. Obviously I'm a solid three to four, eh three and a half.

00;04;35;14 - 00;04;58;16
Ren Estep
So as I need as I said, I need to be better acquainted with code smells. There are I mean, there are tools out there that can help for sure, like setting up a project on like Sonar Cube, right? When you run that out, you can go up there check to see how many code spells are in your project?

00;04;58;24 - 00;05;00;17
Ren Estep
In your code, right.

00;05;03;28 - 00;05;32;24
Ren Estep
And various other data I would say the questions that they gave us in the chapter are definitely something that I never considered Additionally, the the one that you had mentioned that do arguments of the same name always mean the same thing? I am probably like guilty of like hitting that code smell like all the time because I'm just like feed, feed, feed, feed, feed.

00;05;35;05 - 00;05;36;11
Milu Franz
Ah, me too.

00;05;37;06 - 00;06;15;12
Ren Estep
Right? I think like when when you are like building components out and you're not maybe using a state management system, when you're not using that and you're, you're feeding, you don't and that sometimes will just translate translate over into your other methods. You're just like, I'll just feed in this variable into this variable or into this function also and then blam.

00;06;16;22 - 00;06;22;11
Ren Estep
But yeah, I am likely very, very much a culprit of that.

00;06;22;11 - 00;06;27;15
Ren Estep
And you probably need some work.

00;06;27;15 - 00;06;47;06
Milu Franz
Agreed. And I feel like some words are so general for me, like input value data, all these things. And I feel like I reuse them a lot and they don't always be the same, I guess. I don't know. I feel like that came to my mind when I read that question, like, oh, like, oh dang.

00;06;49;01 - 00;06;53;23
Ren Estep
I totally get that. Oh, well, ok.

00;06;57;02 - 00;07;29;19
Ren Estep
I mean, if you're feeding in, but then you name the variable and the other method that you're feeding into. Like if you're getting something from an API call, like it's going to wind up being called data because you're getting the response object that's response dot data. All right. So up until this point, the solution work that has been described has not been in a object oriented programing pattern.

00;07;30;18 - 00;07;43;17
Ren Estep
Uh in this chapter, we see our code moving into the land of OOP. What surprised you most about our first steps into transitioning in the code example?

00;07;45;22 - 00;08;13;29
Milu Franz
Good question again. So for me, it was the discovery of the primitive obsession concept which occurs when you pass a building data type, such a string, a number or a boolean, and you supply behavior for it, such as in the case of the number of bottles which was a number passed as a parameter with multiple functions. And each function returns something based on the primitive parameter passed.

00;08;15;13 - 00;08;37;07
Milu Franz
So I don't think I've ever worried much about I haven't been able to identify this pattern in the past. I'm honest. So I was it was kind of surprising to see it and understanding it and I'm glad I did, I'm glad I read this chapter. What about you?

00;08;38;12 - 00;08;39;29
Ren Estep
So much learning going on.

00;08;40;11 - 00;08;40;23
Milu Franz
Yeah.

00;08;43;02 - 00;09;23;21
Ren Estep
So one of the methods in discovering patterns, I think you mentioned earlier which is something is being new, something that is being used to extract those common patterns into a new class, the abstraction class is called the squint test and this is where you literally squint at the screen until the code becomes just like lines in an object.

00;09;25;02 - 00;09;51;19
Ren Estep
And if the code has the same shape multiple times, you have found a pattern. This method is probably the thing that got me like really a squint well OK, but I tried it. It works. I don't know that I would ever do that in front of other people.

00;09;55;16 - 00;10;08;24
Ren Estep
But definitely the common shapes are there Additionally, most of those shapes have to do with conditionals.

00;10;08;24 - 00;10;10;22
Milu Franz
Yeah. Yeah, that's true.

00;10;12;08 - 00;10;27;04
Milu Franz
That is true. That was an interesting advice they gave I, I found that interesting as well. I, I've never. Yeah, I don't know. I feel like anybody here in this conversation will have the same reaction.

00;10;28;15 - 00;10;28;19
Ren Estep
...

00;10;32;14 - 00;10;51;29
Ren Estep
So also new concepts are popping up all over this chapter. As we move into OOP, the concept of Immutable Objects gets introduced in this chapter. What do you think about these unchanging objects?

00;10;53;27 - 00;11;16;21
Milu Franz
OK, so that part caught me off guard because I feel like I've learned since school like variables change. Change state like, I don't know, this was all right. I'm definitely one of the developers that has always believed that you should mutate and cache variables to improve performance. Like, I'm guessing that's what all my instructors have said. I don't know.

00;11;17;01 - 00;11;45;27
Milu Franz
It's like one of those things. I was in the back of my mind. Like, I, I just believe that to be true forever. The first iteration of the problem that was presented where we had a new instance of bottle number for each similar function made me cringe because it was like creating too many instances of it. However, I have to say this chapter shed light to immutability, especially when the author explains how much more complicated the code would get.

00;11;45;27 - 00;12;10;21
Milu Franz
If we make a decision to only have one model number instance and reuse it 900 times, that's too many times for sure. Definitely add some complexity to your code So what I took away from that section of the chapter was that there needs to be balance between optimizing for the ease of understanding and also maintaining performance. But yeah.

00;12;10;21 - 00;12;13;02
Milu Franz
What about you? What do you think about.

00;12;17;14 - 00;12;52;21
Ren Estep
So I took away that our immutable objects are in relation to caching and that was kind of interesting to me because caching it speed things up a little bit, especially when the object doesn't need to be mutated. Right. We will see this in server side rendered sites and frameworks that use that are examples NextJs and NuxtJs.

00;12;56;07 - 00;13;37;07
Ren Estep
And it. So in the instance of a server and those type of frameworks or just a server side rendered page with data coming in, is that when it sends up the data, the data is preloaded and will not change unless there is a interaction an interaction that would update the data. Right. So like in my mind, that's where I am on the immutability objects.

00;13;37;13 - 00;14;02;10
Ren Estep
So in the instance of the website example, if I have a whole lot of data that went up in my dashboard page and then I, I click and I leave to go look at something else, if I come back to that page and like data hasn't changed, then the data had had been cached and it just automatically loads.

00;14;02;10 - 00;14;27;05
Ren Estep
It's a lot faster. Right. So these objects that are unchanging and get cached when we return and get that cached data, it's much faster, faster than to pull data again, if you will, I think they're kind of useful.

00;14;28;14 - 00;14;54;18
Milu Franz
Yeah, for sure. Well, I mean, I like the perspective that you just use kind of using caching the data for a website. I feel like that's definitely a great example of using Cache. And I think the book also mentioned kind of clearing up cache. That's one of the things that is hard and it's interesting. But yeah, I agree.

00;14;54;18 - 00;15;23;07
Milu Franz
I do think there are useful. It was interesting to see how they manage the number of instances of a class that they were willing to handle and in their in their code. I mean, I found that also new I guess for some reason I expected them to create one instance of bottle number and just reset on all of that.

00;15;23;08 - 00;15;34;06
Milu Franz
Like, at least for me, it was like a little bit of a surprise to see them like analyzing like OK, how we can create multiple instances of these up to make it work.

00;15;35;29 - 00;15;56;16
Ren Estep
Yeah. Yeah. Like because they have, they have like they have the default bottle numbers class, but then you have the extended version of that for I think it was like bottle numbers one.

00;15;57;12 - 00;15;58;16
Milu Franz
Zero and one.

00;15;59;19 - 00;16;01;24
Ren Estep
01 and six, I think. Hmm.

00;16;02;11 - 00;16;04;15
Milu Franz
Yeah. So when they finished that.

00;16;05;22 - 00;16;27;15
Ren Estep
They made extensions of the bottle number to accommodate for those particular instances and then went with a factory to get around to them. Which may actually be in chapter six, but I can't remember.

00;16;28;06 - 00;16;29;14
Milu Franz
They're blending together.

00;16;29;22 - 00;16;42;02
Ren Estep
They're just all going in together. Everything's so exciting. Mentioning chapter six. Before we get there, what was the coolest thing that you learned or just in general in this chapter?

00;16;44;02 - 00;17;15;11
Milu Franz
I think that main lesson I took from this chapter is do not sacrifice readability in advance of performance. Like truly finding that balance between performance while keeping your code simple and readable. Just like the book said, assuming fast enough, just like good enough, the beginning assuming fast enough. If you face performance issues in the future, you can always adjust that in your code and troubleshoot that.

00;17;15;12 - 00;17;22;05
Milu Franz
So yeah, what about you? What was the best lesson or the coolest thing that you have learned

00;17;22;05 - 00;18;02;09
Milu Franz
So. OK, code smells like? So it was fun learning about code smells particularly the primitive obsession? In conjunction with building out the extraction class. So all of the methods that were about the number of bottles that took in the argument of number and that number argument meant the same thing in all of the methods. So I have now gathered all of my numbers up and put them in a basket or something.

00;18;02;17 - 00;18;06;03
Ren Estep
Right. But all of those things mean the same thing.

00;18;09;13 - 00;19;06;18
Ren Estep
So bottle numbers which extracts all those into the two separate little methods into its now own class away from the bottles class all share the same pattern. All that number means the same thing. And then like to get away from that primitive obsession all classes have constructors. So like you feed in your the the number that you need and then that is set within the class and you reference it with Dear Lord, the that this keyword I probably I probably haven't used that since.

00;19;06;18 - 00;19;13;16
Ren Estep
Like I switched from doing class components in React to functions.

00;19;14;14 - 00;19;22;15
Milu Franz
I know I felt like a long time and it was only a couple of years when we, when we changed. I think by some reason

00;19;22;15 - 00;19;24;02
Ren Estep
feels like forever.

00;19;24;02 - 00;19;26;13
Milu Franz
Yeah, it feels like another era.

00;19;27;04 - 00;19;59;24
Ren Estep
But yeah, that's probably that's probably the last time I used the this key keyword and quite because like I haven't used it very much I think maybe a that, that like spurred me to look up what it meant in conjunction to the class and like JavaScript in general. Like there's a lot more to it than I thought there was for sure.

00;20;00;26 - 00;20;04;06
Milu Franz
Yeah, I'll throw the word this , I can see that.

00;20;08;07 - 00;20;19;05
Ren Estep
But that's not that's enough about this. Let's move on to chapter six. Right. Oh, yeah. That was funny. You don't have to laugh. It's cool.

00;20;19;05 - 00;20;21;06
Milu Franz
You know. I laugh at all your jokes.

00;20;22;10 - 00;20;24;11
Ren Estep
Such like a dad joker.

00;20;27;25 - 00;20;32;02
Ren Estep
Um, so chapter six, it's entitled Achieving Openness.

00;20;33;13 - 00;20;34;01
Ren Estep
And I

00;20;34;01 - 00;20;34;27
Milu Franz
Finally

00;20;34;27 - 00;20;36;12
Ren Estep
right right.

00;20;37;00 - 00;21;03;16
Ren Estep
You think after this chapter, you'd just be done. Not. Not the case. Obviously, we have, like, three more chapters after this. Yeah. Yeah. So as we move into chapter six, we dig even deeper into our code, get get getting to be open to. And now we've travel. It's been so long, you probably forgot what we're trying to open it to.

00;21;03;28 - 00;21;33;20
Ren Estep
So essentially that's where that that's where that reference to bottle number six comes in is that they had put in a requirement that when you get to six bottles of beer on the wall, you switch it to a six pack of beer on the wall. So like we've been working all of this way.

00;21;34;13 - 00;21;35;25
Milu Franz
So just to get to this point.

00;21;36;09 - 00;21;37;16
Ren Estep
Just to get to this point.

00;21;39;23 - 00;21;41;23
Milu Franz
I know it hasn't gotten tons low.

00;21;43;17 - 00;22;41;11
Ren Estep
Like, dang, that's that's hard so we spend a lot of times with our conditionals. Oh, I just mentioned this so we spent a lot of time with our conditionals in this chapter and how to replace them in quotes. Replace yeah, pretty much. Ultimately the way to replace them. We wound up using the Martin Fowler's refactoring recipe of replace conditionals with polymorphism What are your initial opinions on this method and how did they change or grow as you read

00;22;41;11 - 00;23;09;06
Milu Franz
Well. The idea of implementing polymorphism to get rid of a bunch of conditionals kind of blew my mind. So I started polymorphism and inheritance and school. Java was my first coding language for context, but I guess we never really studied how to identify code smells that will lead to implementing polymorphism. It was kind of a given part of the problems requirements.

00;23;09;18 - 00;23;43;10
Milu Franz
For instance, an assignment would say, build an app that sells tickets. There are three types of tickets backstage, VIP or general, and following the assignment you know that there was a ticket class and three or smaller classes that extended ticket. And in my professional experience, I've mostly used React with JavaScript, which uses composition instead of inheritance. So I guess I haven't really explored OOP and Polymorphism the last few years, and I really enjoyed getting to these polymorphism solution.

00;23;43;17 - 00;24;02;02
Milu Franz
It makes sense how we got here and yeah, it makes sense when they explain how poorly polymorphism would fix all of these conditionals. I mean, I agree that was definitely a good recipe for it. What about you.

00;24;05;26 - 00;24;08;00
Ren Estep
It's a heavy subject and a heavy word.

00;24;09;13 - 00;24;10;18
Milu Franz
It's hard to pronounce.

00;24;11;04 - 00;24;14;29
Ren Estep
It is. I'm impressed at how well you did.

00;24;14;29 - 00;24;15;21
Milu Franz
Thank you.

00;24;15;21 - 00;24;34;03
Ren Estep
If it gets caught on my tongue quite a few times So. OK, so I had I had this concept of polymorphism in my head before we started this chapter.

00;24;36;13 - 00;24;46;01
Ren Estep
There's probably a bit of is likely on the wrong side, right? Or maybe like right on the cusp of being like, oh, yeah. I get it.

00;24;49;10 - 00;25;11;04
Ren Estep
So I always kind of equated it. And this is probably just my background I tend to equate things that I'm familiar with so that I, like, understand it. So I always equated polymorphism to like the clone stamp in Photoshop.

00;25;11;27 - 00;25;13;12
Milu Franz
I love that analogy.

00;25;15;13 - 00;25;42;15
Ren Estep
Like, in my mind, I'm like, it totally works. So long as you're using the exact instance, it's when you go in and you start like extending instances or like you can. The the fun thing about classes is that they have these inherent This is a getting off topic, just like a touch. But like classes have these inherent functions within them that are setters and getters.

00;25;42;15 - 00;25;54;04
Ren Estep
And like, you can you can change the you can change the different values with it, just crazy. So, like.

00;25;54;22 - 00;25;55;27
Milu Franz
Crazy things are here.

00;25;56;01 - 00;27;32;01
Ren Estep
Yeah, yeah, yeah. Classes are neat. However, so like my my thought on it, being close to a clone stamp as a metaphor is very close. So long as we keep it as an immutable object, but you can definitely change things there So I guess the bit that I had wrong, I think, was that in object oriented programing terms that ability to make making new but different object kind of from your class instance because you can technically set and get your values differently or you can feed feed in how to say this, you can you can feed in the instance of like the bottle numbers, you can feed in a different number and it gives you

00;27;32;01 - 00;27;43;15
Ren Estep
a different instance. So it's like, it's like it's a clone stamp, but like a real cheap one. So like something's just slightly off. Right.

00;27;44;25 - 00;28;13;27
Milu Franz
Well, I think it would be like I clone stamp like a perfect I'm not maybe not perfect analogy, but I can see like if when you're cloning, you also have settings and you could like apply all of those settings to your cloning. I think like that maybe it would be like a better match of polymorphism and how you or classes extend a larger class.

00;28;13;27 - 00;28;23;26
Milu Franz
So. So all of you are the same type. So all of you are like cloning stamps, but you all have different settings. Maybe

00;28;23;26 - 00;28;25;02
Ren Estep
Oh Man, let's

00;28;25;02 - 00;28;26;01
Milu Franz
brainstorm here.

00;28;26;01 - 00;28;38;02
Ren Estep
Let's get to Adobe's get lab right now and do like a feature request on the clone stamp. Like that clone stamp can use some settings just sayin'.

00;28;41;08 - 00;28;43;07
Milu Franz
Inspired by polymorphism.

00;28;43;23 - 00;28;53;15
Ren Estep
Right? Not clone stamp could have. Oh, what if you could set the clone stamp to have a gaussian blur.

00;28;56;11 - 00;29;01;17
Milu Franz
Well, that will be one of the settings, so it will still be an stamp. So it will be like child class

00;29;01;18 - 00;29;22;00
Ren Estep
And but then like you, you set to gaussian like, but I want my clone stamp to have a gaussian and blur. So like when you're doing the stamp, it's still copying the area that you're going over. But all of the stuff is blurred a little. So like, like it all, like if you wanted to go into a close edge.

00;29;25;16 - 00;29;27;09
Milu Franz
I feel like we are into something.

00;29;28;12 - 00;29;35;10
Ren Estep
Right Feature request Adobe, please. It probably already exists. I haven't like played around with Photoshop.

00;29;35;10 - 00;29;36;27
Milu Franz
Probably me either.

00;29;37;13 - 00;29;40;10
Ren Estep
And like a photo editing instance in a while.

00;29;41;12 - 00;29;55;26
Milu Franz
I don't have Adobe anymore, so I haven't played with it for all of them. I know. It's so sad. I feel like I've had it I have. I've had access to Adobe Product since I was in school and I'm really sad that I don't have access to it anymore.

00;29;56;27 - 00;29;58;23
Ren Estep
I can't give it up. I just pay for it.

00;29;59;25 - 00;30;01;24
Milu Franz
Yeah, I mean, that's the alternative.

00;30;03;08 - 00;30;36;17
Ren Estep
It's true So in this chapter, they hold off on fixing a Liskov violation until it becomes a problem. Obviously, this is on purpose, or at least I hope it is to teach a lesson. How did you feel that teaching technique from your own learning, do you feel how do you feel about that teaching technique from your for your learning yourself what did it accomplish?

00;30;36;17 - 00;30;41;16
Ren Estep
The desired result? Yeah. Did you yeah. You understood that we're good?

00;30;41;17 - 00;31;10;10
Milu Franz
I think so. To be honest, that one line change at a time technique that we have been using in this book drives me a bit crazy. It feels really low. Maybe because we're reading through it which has a lot more pauses than implementing these changes in your daily work would. However, I found their approach of showing how refactoring can make a small code smell more problematic as you go was definitely good.

00;31;10;22 - 00;31;34;22
Milu Franz
It was nice to see that. It was nice to see the progression of the problem and it felt very real. I think this is what usually happens when you refactor. You can create some side effects and they become it's like a snowball. They become bigger as you continue refactoring. So yeah, I appreciated how they analyzed the situation, step by step, it was easy to identified.

00;31;34;22 - 00;31;45;15
Milu Franz
It was, it was nice to see that it's not only you, you know, when these things happen but yeah, how do you feel about this technique?

00;31;46;09 - 00;31;50;27
Ren Estep
I had a similar thing. First I was like, Oh, I see what you did there.

00;31;53;09 - 00;32;51;07
Ren Estep
Mainly because like, learning, learning these things. Just reading about it and like working through things If you're given the exact instructions for every step it doesn't allow for a person to make mistakes and learn from them. So I think it was a good idea for them. To incorporate that, Oh, we've made a mistake. Now we have to work back to figure out and through problem solving and now an analysis of the code up until that point, of whether or not you you really have to make changes like huge changes if you need to walk things back or if you can kind of move forward.

00;32;51;07 - 00;32;58;21
Ren Estep
But also like do like a hop back but still move forward.

00;33;00;08 - 00;33;00;24
Milu Franz
Yeah. Yeah.

00;33;01;01 - 00;33;13;17
Ren Estep
I think I think it was a good, good thing that they did or added in because, you know, you you learn by making mistakes.

00;33;15;04 - 00;33;33;15
Milu Franz
I think so too. It was a good way to show it. How do you feel about like do you feel like it's going really slow? Like, I don't know why, but I'm bored or anything, but I'm just like, oh, my gosh, these like one change per line is like killing me a little bit.

00;33;35;28 - 00;34;18;24
Ren Estep
You're you're not wrong. But I think I think they're doing that for a specific reason. And I think they're doing that so that you see that there are different ways of going about refactoring because, you know, earlier in the book, they had mentioned, you know, you do this like even before refactoring, you're doing it one step at a time, but and not to like make big leaps forward because I mean, if you you know what they say about making people that assume things makes an ass out of you and me yeah.

00;34;19;06 - 00;34;30;01
Milu Franz
Yeah, I know. And that's like one of those things that I still need to work on. I feel like I'm still I'm not like small changes at the time. I'm a type of person, but just go to those goals until it works, which sucks.

00;34;30;08 - 00;35;21;18
Ren Estep
But yeah, I totally get that. So having been mostly self-taught in web development, I just I've been working in the industry for a little over five years, but I just started to learn how to do how to analyze my code and understand time complexity. So like giving your code a like rating of big O notation and like I had heard it places for your codes efficiency.

00;35;21;18 - 00;35;51;21
Ren Estep
Right? And I had heard it places. And I finally going through and being like, all right, I should probably really understand this it's not something that I should just like get by but the it's interesting to get these new old concepts coming through.

00;35;51;21 - 00;35;52;10
Milu Franz
For sure.

00;35;55;24 - 00;36;19;08
Milu Franz
Now, that's awesome. I love what you're learning that I feel like. Yeah, like more than once I've seen those iterations of arrays in iterations of an array, in another iteration of an array and you're like, it's like a big O notation pretty high. So yeah, love that you're learning that.

00;36;20;18 - 00;36;49;29
Ren Estep
Yeah, I had never really thought no one's ever brought it up like that nest. Those nested loops are not. Yeah, I heard that. I'm like, good point. That being said, the dot sort inherent method to the array, also a not a efficient form of code they're not.

00;36;50;00 - 00;36;54;02
Milu Franz
Yeah. I mean, they look good because you don't really see what it's under the hood.

00;36;54;25 - 00;37;26;18
Ren Estep
Because you're like, it's one line of code. It's fine because like so many times you get like those best practices nailed into one of them. And I'm not sure who came up with this best practice, but it's like to keep your lines of code under like 150 lines per file right now. Yeah. Dot Sort it's like one, it's like one line that's off topic.

00;37;27;07 - 00;37;36;18
Milu Franz
Things like that. Filter all of those, all of those handy dandy functions. Definitely they have some cost for sure.

00;37;37;01 - 00;37;38;21
Ren Estep
I'll never give up dot filter.

00;37;39;21 - 00;37;40;23
Milu Franz
I know, me either.

00;37;40;24 - 00;37;41;09
Ren Estep
It's just.

00;37;41;14 - 00;37;42;12
Milu Franz
It's just so nice.

00;37;43;20 - 00;37;56;15
Ren Estep
Granted. Granted. If I were being smart, if I were being a smart person, I would do my dot filters on an API call Yeah.

00;37;56;18 - 00;38;01;05
Milu Franz
Backend is definitely faster than the front end for a lot of things.

00;38;01;21 - 00;38;01;24
Ren Estep
Yeah.

00;38;04;09 - 00;38;15;17
Ren Estep
Words, words. Let's, let's move on. Like, see, the coolest thing that you learned in this chapter All right.

00;38;16;00 - 00;38;33;13
Milu Franz
The coolest thing about this chapter for me at least, was identifying recipes to solve the many conditionals and finally achieving openness throughout the six pack change. Finally, I kind of forgot about these new requirements.

00;38;33;15 - 00;38;33;24
Ren Estep
And.

00;38;34;08 - 00;38;38;01
Milu Franz
When they mentioned it again, I was like, Oh yeah, that's what we were doing.

00;38;40;05 - 00;39;05;21
Milu Franz
We have talked about creating code that is open for change without altering its existing behavior. And even though I understood the concept it was nice to see it in action. It was nice to see how we got to that point. We're just adding a new class that extends the bottle numbers class easily, these new requirement without modifying anything else about the code.

00;39;06;03 - 00;39;08;27
Milu Franz
I was I was really cool to see. What about you?

00;39;10;21 - 00;39;43;19
Ren Estep
So learning so much more about polymorphism was a huge help in this chapter, at least understanding the problem, because I definitely had him. I had an knowledge gap in that, like I understood the base bit of polymorphism, but like this went in so much further and it was a so big help was a big help.

00;39;43;19 - 00;39;49;17
Milu Franz
It's a good book. I'm glad we're reading this I feel like we're learning a lot along the way.

00;39;50;09 - 00;40;00;22
Ren Estep
I am glad that we are reading this also. There's also like so many references to other resources within this book, so that's.

00;40;00;22 - 00;40;01;07
Milu Franz
Yeah, I feel.

00;40;01;07 - 00;40;02;01
Ren Estep
Like nice.

00;40;02;17 - 00;40;06;14
Milu Franz
Our journey has just started. We're going to read all these other books.

00;40;07;12 - 00;40;20;25
Ren Estep
We are so next time we'll be covering chapter seven and eight and I guess Thanks for listening.

00;40;21;20 - 00;40;25;03
Milu Franz
Yeah, thank you for listening. Listening, to us ramble.

