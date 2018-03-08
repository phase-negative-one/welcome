# Empathetic Code Review

Quality, helpful code review suggests improvement to code **empathetically**. We will start with guidelines on giving empathetic code review and then talk about the technical side. 

## Why is empathy **so** important?

We are all aware of a particular archtypal programmer. Unconcerned with feelings, unconcerned with ego, bored by trivial niceities. They are engineers concerned *only* with making something work, and they only have time for the facts. 

The truth is, most programmers are not like this. When most of us take three days to engineer a solution we are proud of *do* get emotionally attached to that solution. Most of us are much more open to feedback that will improve our code when it is expressed with empathy. 

### What is empathy?

Empathy is feeling what someone else is feeling. It is putting yourself in their shoes. In code review this means acknoledging that the author of the code you are reviewing is human. It is acknoledging that they may have some insecurities or feelings of imposter syndrome. It is recognizing that no one likes being spoken to, or about, unkindly.

### Why some people come of as jerks when they give feedback

Sometimes when people sound like a jerk when they give feedback, they will defend themselves by saying "I'm just being honest." They will argue that it is on the other person to be tough, not on them to be kind. I have news for those people: It is both. It is everyone's job to be emotionally resilient, and it is everyone's job to be kind to eachother. This is true in *any* job. We all know writing software can be frustrating! It is everyone's job to make the human interactions as smooth as possible so we can all save our frustration for dealing with deprecated dependencies. 

But the "brutally honest" feedback style is only one way in which people can come off as unkind when giving feedback. The more common reason is due to people's own insecurities. When someone feels insecure when reviewing someone else's work, their feedback becomes less about helping someone else improve, and more about proving themselves and their own knowledge or intelligence. When this happens, empathy goes out the window. The review becomes a one sided argument about the "right" way of doing something. 

### Guidelines for conducting empathetic code review:

1. *No code is "wrong".* 

Some code is wonderful, some (probably most) code could be improved, and some code does not even run. But no code is wrong, and please don't ever tell someone that their code is wrong. Code review is not about who is right and who is wrong. It is about working together to improve. If you review code that makes you want to gag, take a moment and get over yourself. Remember when you were a beginner. Then write a kind suggestion for improvement. 

1. Don't tell people what to do, or even what they "should" do. 

Unless possibly if you are code reviewing someone who reports directly to you. Managers are the only person at work that can tell someone what to do. Anyone else can just make suggestions. That's what code review is. It is suggestions. When some people get told what to do by someone who isn't their manager, it puts them on the defensive. Say things like "it might be better if...". 

1. Don't automatically assume a rule, best practice, or pattern you read about in a blog is the best way to do something. 

The author of that blog has their opinion. It's up to you to form your own. If you don't understand why one way of doing something is better than another, don't pretend to. At the same time, its OK that you don't know the best way of doing everything! No one does. It's perfectly fine to say "I read that this pattern can lead to problems with scaling." This is much better than writing "This patterns will cause problems with scaling," without backing up that statement. We do *not* want to get into arguments about what is right and what is wrong, or about who knows more. That is the opposite of helpful. We want to share knowledge, which means being honest with eachother and ourselves about what we know, and being open to being wrong. 

1. You are a guest in the other persons code. Act like one. 

Be kind, respectful and gracious.

## The technical side

Of course empathy is just the packaging. Let's talk about the meat of code review: technical suggestions for improvement. 

## Three things you should look for when reviewing code: 

1. Does the code do what it is supposed to do? 
  - Are there bugs? 
  - Does it handle the edge cases properly?
  - Does the code solve the problem it is intended to?
  
2. Is it readable?
  - Is there a more human readable way to code this? 
  - Is the author of the code playing "code golf", and trading too much readability for brevity?
  - Are the function and variable names semantic? 

3. Is it efficient?
  - Does the code execute as efficiently as it can? 
  - Are we using nested for loops when one loop would work?
  - Are we making copies of our data when it could be changed in place?

4. Is it best practices?
  - Is the programmer following conventions and **agreed upon** best practices? 
  
5. Some other things to consider:
  - Sometimes code adhers to best practices, is reasonably efficient, fairly readable, and does what it is supposed to... but somehow could still be majorly improved. 
  - Is the author overcomplicating things? 
  - Are there more steps than necessary?
  - Could the control flow be simpler or better organized?
  - Are there large functions or classes that could be refactored into smaller functions or classes, leading to better organization?
  - Is the code too timid, relying on lots of fall backs and error handling rather than asserting itself properly? More info on writing [confident code here](https://www.youtube.com/watch?v=T8J0j2xJFgQ).
  - Code review is not the place for arguments on spaces vs tabs, or whether or not to put a space between a `)` and a `{`. That is what style guides are for. If the author is not following the styleguide, it should suffice to simple say "Please follow the style guide," rather than point out every place where they have not. That is their responsibility. 
  
## On recieving code review

**Even with these guidelines, not everyone is going to be great at giving empathetic code reviews.**

It is your job, as author of the code to set aside your ego and look at the review as what it is: suggestions to improve. It is your job to realize, even the harshest attack on your code is not an attack on **you**. You are not your code. If your code is deeply flawed, it doesn't mean you are deeply flawed as a human being. If someone hates your code, it does not mean that they hate you. We are all passionate about our craft. Don't let someone's passion and lack of practice at empathy threaten you. It is not your job to endure abuse, but it is your job to be emotionally mature and reasonably tough. Empathy does not mean "kid gloves." 

**Remember the bottom line**

Business is about money. Fortunately, it just so happens that engaging with people empathetically is good business. Remember that your feelings are secondary. A good manager will respect you for using empathy when giving feedback. They will also respect you for not demanding empathy at all times. When it comes to empathy, it goes much better to lead by example than to demand "better" empathy from others. 

**Treat your reviewer like you would treat a guest.**

When hosting a guest, we should be welcoming, warm and gracious. If someone's suggestion helps you, thank them! If they make their suggestions in an empathetic way, thank them for that! But this analogy only goes so far. If someone is taking advantage of your hospitality and being disrespectful of you in your actual home, you can tell them to leave. In code review at a place of business, it can be more complicated. Ask yourself, what is their motivation? If they seem to be meaning to help, give them credit for that, and practice empathy when you suggest to them how they might give better feedback. 

## An alternative outlook:

Some people will argue that the archtype at the beginning, the programmer who cares only for the right solution, and has no time for people's feelings, is **correct**. That all else is coddling and a mature human being should be able to completely set aside their own feelings and just deal with the facts. They might say that while most people may not be able to do this, everyone should **aim** to do this, and that worrying about empathy for things like code review just encourages emotional immaturity. To those people, I would point out that companies like Google disagree. But if you prefer a feelings-free company culture, you can probably find them. Just be prepared for the in-fighting, toxic politics and petty competition that seems to me go go hand in hand with this line of thinking. 

## Conclusion

Empathy is not just a touchy feely thing. It is a great starting point for sucessful communication. And for most people, empathic communication takes practice. 

Code review is about collaboration towards the betterment of the codebase. It should never be about ego, proving one's self, being right, or putting someone in their place. Code review is a terrible place to start an argument. Quality code review is empathetic: it takes into consideration that the author is only human. It looks for improvements that could be made, makes suggestions to do so, and leaves it at that. 

This does not mean you should hold back when doing code review! In fact, being empathetic sheilds you from the potential embarassment of a bad suggestion. If you are "just telling the facts" and are unconcerned for how your words might make someone feel, it sucks when you are wrong. But if you relate to someone as a human being, and you make a kind, but wrong suggestion, there is no reason to be embarassed. We are all humans and we all make mistakes. So don't hold back! Just be kind. 

Happy coding and happy code reviewing!
