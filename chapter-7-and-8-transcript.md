00;00;05;03 - 00;00;17;26
Ren Estep
Hi and welcome to the Imagine Dat podcast where we explore software development concepts I'm Ren Estep, a software engineer who likes coding, drawing and running like a snail.

00;00;18;03 - 00;00;24;17
Milu Franz
I am Milu Franz also a software engineer who enjoys learning something new every single day.

00;00;25;13 - 00;00;48;20
Ren Estep
Our current season will take the format of a book club where we will be reading 99 Bottles of OOP by Sandy Metz, Katrina Owen and T.J. Sturgess. This book follows the 99 bottles problem where you build and transform your solution as you go with clean code and best practices in mind. There is a link in the show notes as to where you can buy the book.

00;00;54;20 - 00;01;23;24
Milu Franz
Hello, everybody. Today we will be discussing chapters seven and eight. These chapters discuss in depth the final steps to finish refactoring the 99 bottles song we have working on so far. So let's start with chapter seven. The title is Manufacturing Intelligence. As we dive into Chapter seven, we learn more about using polymorphism and explore their various forms of a factory called take.

00;01;24;12 - 00;01;43;22
Milu Franz
And also we are considering the trade, the trade offs involved. So it's a pretty interesting chapter. So Ren just to get us started. In your own words, could you explain their relationship between message senders and factories and why they play an important role in polymorphism?

00;01;46;11 - 00;02;29;10
Ren Estep
Sure. So early in the book, the authors tell us about the preference for the saying message senders, Right? You, I remember like keying in on this quite a bit. You like this phrasing also over calling a function. So in that, it gives us a better description of what's happening, right? So now in this chapter, we see a message senders as collaborators that work well with polymorphism and view the polymorphic objects as elements that are interchangeable but are highly collaborative.

00;02;29;10 - 00;03;02;26
Ren Estep
Message sender lacks some really important knowledge like in the classes that we're working with. There's a bottle number variant and it's a class But also they don't know so that the message sender that are within that class, they don't know how to choose between an... OK, not I've a class class. So it's a class, but it's like a like a selector almost.

00;03;03;06 - 00;03;38;05
Ren Estep
So but the message sender doesn't know how to choose between the different functions, right? That is where our factories come in and our factories are like the stage manager of a production and it makes sure that our right variant class or objects goes into the correct role. So essentially it's like a symbiotic relationship. They, they need each other.

00;03;39;11 - 00;03;42;26
Ren Estep
So I guess not a difference. Right. But like I.

00;03;42;26 - 00;03;54;15
Milu Franz
Love that I love your definition of factories they are like a stage managers of the production. Yeah. That's such a good way to put it. Absolutely.

00;03;57;13 - 00;04;24;04
Milu Franz
I can also describe it in my own words. So as you said, this book uses a term sending a message instead of calling a function. And like you said, I love that because the reason behind this choice is to leave some mental space between the sender's intention and their receiver's actions. And they play an important, an important role in polymorphism because they use role.

00;04;24;15 - 00;04;49;00
Milu Franz
The book calls them role playing objects, which are your classes basically exposed APIs without knowing the internal implementations. So you don't know what's going on in them. And the ignorance makes these role playing objects interchangeable, which makes them more flexible for change. And since message senders are ignorant of what role playing object they're using, this knowledge has to live somewhere.

00;04;49;09 - 00;05;10;13
Milu Franz
And that's like you said, where factory becomes, super useful. They are the place where the logic necessary to choose the correct type of role playing object is chosen. AKA a bunch of conditionals to select the correct type. And as the book stated, factories are where conditionals go to die. I also love that definition.

00;05;11;24 - 00;05;28;01
Ren Estep
I forgot about that phrase. That phrase is really is factories are where the conditionals go to die. That so like it's like so disheartening, but also like. So true. Yeah, that's so true.

00;05;30;05 - 00;05;41;15
Milu Franz
Yeah. Cool. I'm glad we both kind of, like, understood how they're, like, the language they're using and how we're definitely on the same page with them.

00;05;44;02 - 00;06;05;05
Milu Franz
So, Ren, if you had to choose between the first three factory recipes for one of your projects, and I think those three were simple conditional made up programs, class lookup, key value lookup, which one will you choose and why

00;06;05;05 - 00;06;49;23
Ren Estep
Well. You know, so even if I hadn't read the chapter I would probably try to make the key value pairs work for me primarily because it's familiar to me. But also it seems like it would be more open to manipulations Also, I think it would fall into the good enough idea, which I really like and now I'm like, All right, well, when I take on a GitLab issue, I need to make sure that it's good enough for this specific issue and stop thinking about the future.

00;06;50;11 - 00;07;06;21
Ren Estep
Not that like thinking about the future is bad necessarily, but sometimes that leads down to terrible and horrible things. Or good things, depending on how you have figured it. What about you? What are your thoughts on this?

00;07;08;05 - 00;07;35;20
Milu Franz
Well, I think for me, the simple conditional option is just to ugly to look at what all those if statements, It just doesn't look good The key value option was definitely very intuitive. But personally, I like the Meta-program class lookup option. I like how this option dynamically identifies the correct bottle number class instead of adding them on a list as the other options.

00;07;37;01 - 00;08;15;18
Milu Franz
So I feel I can look cleaner and addition. I like how this factory is open to extension without changing its implementation. Like you could just add a new class model number seven and you won't have to change anything in this factory to get it to work. However, there were a few issues with this implementation that the books stated, such as the fact that it would ignore any bottle number class that did not follow the name convention and that the bottle number classes are no longer explicitly, explicitly referenced in the source code.

00;08;15;26 - 00;08;38;27
Milu Franz
So it would make the code a little harder to understand and the 99 so hard to follow, which would make the code more expensive. Right? Like if you're not working on it, someone else will work on it and it will take a little longer to figure out what's going on. So, yeah, so maybe it's not the best option, but to my eyes, when I saw that, I was like, Oh, so clean, so beautiful.

00;08;40;17 - 00;08;48;26
Ren Estep
I mean, it did look like a good option. I just, I went for it for familiarity because I've rocked that key value pair.

00;08;49;21 - 00;08;53;29
Milu Franz
Oh, yeah, yeah. That was my second favorite for sure.

00;08;57;26 - 00;09;17;13
Milu Franz
This chapter introduces us to the registry pattern, which gives classes the responsibility to put themselves on the list, explicitly asks their factory to call them. What did you think about this pattern in comparison to the others, which are a bit more similar among each other?

00;09;19;08 - 00;09;52;05
Ren Estep
So all of the solutions were a bit slimmer. Similar, right? And I will say that after learning about the registries pattern, I think I would change my answer that I gave before about key value pairs to trying to implement this particular pattern. The registry approach because it is definitely easier to read rather than the key value pairs. Also seems a lot cleaner.

00;09;54;24 - 00;10;25;21
Milu Franz
I completely agree. Yeah, the self registration pattern was definitely interesting. I will argue that it was the most interesting pattern that the most interesting pattern that we review in this chapter. I actually had a conversation with someone from work about this pattern and he highlighted a great point. This implementation could lead to some bugs if the classes are not registered in order.

00;10;25;25 - 00;10;52;22
Milu Franz
And I feel like that's putting a lot of responsibility onto the next developer. Kind of like you are assuming that this person is going to know that the order matters. And so we kind of like had a little bit of a we chatted about it and I guess my suggestion for this solution because I still feel like it's a very strong recipe, it will be to improve upon this solution.

00;10;53;01 - 00;11;31;15
Milu Franz
Using a map instead of an array for the registry so we could keep the order. So the keys would be like the order that you have to keep it and the value, the class that you're going to create. But yeah, I don't know that that's that really interesting and interesting conversation. And I, I, I, I haven't applied this pattern anywhere but I want to Yeah.

00;11;34;05 - 00;12;20;14
Ren Estep
Sorry, sorry. It just, it reminded me of a different object that would also probably work because it has to do with how it, how it intrinsically moves through the iteration. And I think I want to say it's, it's like a list collection. So like that you know, how you can kind of move wibbly nimbly through arrays but the I think, I think it's the list like you have to literally move from one to the next.

00;12;20;14 - 00;12;29;25
Ren Estep
It's like, it's like you're moving through a hallway with of rooms that you can only get to the next room by going through the door.

00;12;30;16 - 00;12;31;20
Milu Franz
A linked list.

00;12;32;01 - 00;12;34;05
Ren Estep
Linked list, yes. Yeah, that's it.

00;12;34;18 - 00;12;52;11
Milu Franz
Oh, my gosh. I haven't used that term in a year now. Like data structures and algorithms from college. But yeah, let's start with well, go hand me with the solution. I agree. Is there any math in JavaScript?

00;12;52;24 - 00;12;54;12
Ren Estep
I believe there is.

00;12;56;07 - 00;13;03;20
Milu Franz
Interesting. Learning something new or here Yeah.

00;13;07;18 - 00;13;12;20
Ren Estep
Yeah. Where you enter into the head and like, you can only move from one to the next one.

00;13;18;27 - 00;13;24;20
Ren Estep
Visually speaking, it just looks like a really hilariously nested object.

00;13;27;14 - 00;13;43;26
Milu Franz
Yeah, for sure. I've only used linked lists in Java. I've never used that in JavaScript. But it does look just like a nested object. So maybe it's not like I need to.

00;13;44;01 - 00;13;46;07
Ren Estep
Not like a true linked list, but like.

00;13;46;29 - 00;13;48;02
Milu Franz
Someone building it.

00;13;48;18 - 00;14;03;21
Ren Estep
Yeah. The times that I've I've I've looked at, I've there been a few instances where I had to hit up the knowledge on linked lists for like a weird JavaScript question. Was like.

00;14;03;21 - 00;14;04;26
Milu Franz
Very cool.

00;14;05;29 - 00;14;12;03
Ren Estep
Like do they have linked lists? And that's how I figured that that one out, it was like, well, awesome.

00;14;12;03 - 00;14;12;14
Milu Franz
Yeah.

00;14;13;13 - 00;15;02;21
Ren Estep
Doing these challenges makes a, makes your brain work a little bit more. But you know, outside from other random topics, we also have chapter eight to cover the developing a program programing esthetic. Right. So naturally, after chapter seven, we lead into chapter eight where we see the responsibilities of our bottles glass get further spread out and with that more refactoring that so So, so far this book has been amazing, right?

00;15;03;16 - 00;15;31;21
Ren Estep
And I've learned a ton. You've learned a ton. And Chapter eight definitely lives in the realm of things to learn. Right. But this chapter was extremely difficult to get through, at least on my from my perspective, Why do you think that is or isn't the case?

00;15;32;19 - 00;15;53;21
Milu Franz
You know, you're not alone. You are not alone. This one was the heart. Like, I care. It was hard to get through it. There were a lot of concepts to unpack in this chapter. I wish the authors divided into two chapters, actually. I was thinking about it after I finished. It would have been a bit better to digest.

00;15;53;22 - 00;16;08;27
Milu Franz
I can see the programing esthetic concept to have its own chapter, and they could have expanded a bit more on it instead of sprinkling it through this chapter. What do you think So.

00;16;09;11 - 00;16;45;17
Ren Estep
Okay, I really I really wanted to say to to that to this question. I really wanted to say that it was hard to get through because it was a really long chapter, but that wasn't necessarily true for me. I think what was hard for me was reevaluating the lessons we had learned before in iteration and then adding the instance of jumping to conclusions.

00;16;45;26 - 00;17;32;21
Ren Estep
Right. So, like you, you know where you are now familiar you know where you are now. You're familiar so you can skip a few steps. And my brain was just like but why? I basically had to read reread portions of the chapter so that I could get past the stuck feeling of being like, why am I abandoning my friend iteration to skip a few steps ahead I know but I feel like I did learn a lot from the difficulties.

00;17;35;00 - 00;17;44;15
Milu Franz
It was a good chapter for sure. So yeah, I totally get that. Yeah, I'm Bonnie, where I want to power through.

00;17;45;21 - 00;18;22;06
Ren Estep
Pretty the, the the temptation to just go straight to the summary and be like, Yeah, I read it. That's a really strong So I mentioned that jumped to conclusions. This brings out my next question, which the concept of coding by wishful thinking was brought up in this chapter. Do you ever use this concept with your coding practice, or is this something you have trouble understanding?

00;18;22;19 - 00;18;24;27
Ren Estep
I mean, what are you what are your thoughts?

00;18;25;09 - 00;18;55;12
Milu Franz
I will say coding by wishful thinking feels a bit too familiar to me. Isn't that what we all know already? You of think about your solution and start crafting it even though it's not fully baked, then edit in multiple places to make it fit I guess I struggle a little bit with these concepts. I got what they were doing, but it didn't feel that much different.

00;18;55;16 - 00;18;59;28
Milu Franz
From, like, what we already do. What do you think?

00;19;00;29 - 00;19;39;25
Ren Estep
Okay. Okay. Well, just for for some context. So there's a wee definition. So the book says Coding by wishful thinking allows you to sketch software designs, ideas economically with a low level of commitment. So with that, the concept that I was talking about earlier that I had a difficult time grasping, was this right, that jumping to conclusions or like perceiving what is there right?

00;19;41;27 - 00;20;09;11
Ren Estep
Making intuitive leaps on the basis of knowing the problem. And the only reason I had difficult grasping this concept, as I said earlier, is that early in the book, we had made all these steps and we learned all of these steps to get to a certain point. And then just kind of like we're like, well, it was nice to know you and now you're going to sit over here.

00;20;10;00 - 00;20;11;14
Ren Estep
You'd be good over there.

00;20;11;14 - 00;20;12;20
Milu Franz
And, you know, not anymore.

00;20;13;02 - 00;20;34;23
Ren Estep
You matter anymore. I'm out of out of sight, out of mind. And I just disregarded that at this point, which it was just weird to me in granted Now that I have read the chapter, I do understand especially after reading it probably more than once.

00;20;37;25 - 00;20;55;20
Ren Estep
I can probably say that I do do some bit of code coding by wishful thinking in my practice, but I'm probably not doing it correctly.

00;20;57;07 - 00;21;23;25
Milu Franz
Yeah, I think this is still like a muddy concept to me because it felt I mean, I'm sure there is something there's more to it if they are mentioning it and they're trying to explain it. But yeah, I don't know. It felt to me, I mean it was very different from following recipes. Like you said, it was kind of just like analyzing the problem and be like, oh, these just make it work, right?

00;21;23;25 - 00;21;24;19
Milu Franz
Isn't that what we do?

00;21;26;20 - 00;21;33;28
Milu Franz
But I get that it was a muddy concept for me to um.

00;21;34;23 - 00;21;47;08
Ren Estep
So we are nearly done with the book we have after to go at this point. Do you feel like you're coding practice has improved?

00;21;48;12 - 00;22;38;22
Milu Franz
Heck yeah. A couple of weeks ago I had the chance to refactor a few of the implementations I've been putting together work and I have to say this book was immensely helpful. My code source has been written using Golang, which is post object oriented programing or lightweight object oriented. So it doesn't use classes, it uses structs, but you can definitely use polymorphism patterns with these and I was able to apply, I was able to apply a few of the things that I learned So yeah, I think this money, this money this book was worth the money was, was a good investment for sure.

00;22;38;23 - 00;22;39;14
Milu Franz
What about you?

00;22;40;26 - 00;23;12;16
Ren Estep
So I truly want to say yes that it has improved and in some aspects it prob it definitely has For instance, I understand the basic code smells and how to recognize them now. But in a lot of concepts I think I need to go back and reread them and start finding ways to incorporate them into my coding practice.

00;23;12;29 - 00;23;24;08
Ren Estep
And then into my mentoring practice as well. So, uh, yeah, well, that was that was, that was chapter eight.

00;23;25;21 - 00;23;34;00
Milu Franz
Yeah. Thank you for sticking with us until this point. We have, we are so close to finishing this book now.

00;23;34;01 - 00;23;39;20
Ren Estep
Next time, chapter nine and we'll see you later. Bye.

