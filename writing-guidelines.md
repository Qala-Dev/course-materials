# Writing Guidelines

## 1. Table of Contents


- [Writing Guidelines](#writing-guidelines)
  - [1. Table of Contents](#1-table-of-contents)
  - [2. Goals](#2-goals)
    - [2.1. Why you write](#21-why-you-write)
  - [3. Topic](#3-topic)
    - [3.1. Choosing a topic](#31-choosing-a-topic)
    - [3.2. Describing your own journey](#32-describing-your-own-journey)
    - [3.3. Diving deep into a very narrow topic](#33-diving-deep-into-a-very-narrow-topic)
    - [3.4. Tutorial for a small prototype application](#34-tutorial-for-a-small-prototype-application)
  - [4. Know your audience](#4-know-your-audience)
    - [4.1. Why your audience matters](#41-why-your-audience-matters)
    - [4.2. The Qala target audience](#42-the-qala-target-audience)
  - [5. Iterate](#5-iterate)
  - [6. Don't forget](#6-dont-forget)
    - [6.1. Grammar](#61-grammar)
    - [6.2. Plagiarism](#62-plagiarism)

Writing is one of the cornerstones of the Qala program. One benefit is that it can help make your learning process more effective by forcing you to think about the subject in more depth. Another benefit is that it contributes to your online portfolio. A good article is a valuable digital artifact that can help you get better exposure to employers, or to the industry in general. This guide contains information and tips on how to write better articles and get more out of your time spent on writing. This is largely based on observations from previous students, and will hopefully prove to apply to your situation too. 


In a nutshell, the process described here goes as follows:

> Define your goals. From your goals, choose a topic. Given a topic, what is the most appropriate audience? Identify what your audience already knows and what you want them to learn, and define the structure that will provide the most natural way of getting there. Start writing your content iteratively and keep optimizing for the goals you are trying to achieve. Run your article through a grammar-checking tool, and format it for the intended medium. Conscientiously proofread everything before publishing.


## 2. Goals

###  2.1. Why you write

The Qala program requires you to publish articles regularly, so naturally one of your goals will be to satisfy that requirement. If that is your *only* goal, however, your writing will usually come across as uninspired, and often unoriginal and uninteresting. This should not come as a surprise, since you explicitly weren't optimizing for anything but finishing an article.

Additional goals could be (but are not limited to):

- Learn something new and synthesize your learnings for your own reference
- Produce digital artifacts of things you've learned, researched, solved, ...
- Build an online reputation or following in one or multiple domains
- Help readers avoid going through the same struggles you did when studying or building something specific
- Promote a new tool you've built or a new insight you've found
- ...

These goals can vary based on your ambitions, your skill level, the stage of the program, ... You can have multiple goals when writing an article, but as in life generally - if you set too many goals, you may end up struggling to achieve any of them.

Once you understand the goal(s) of your article, make sure to remind yourself of them frequently. For example, if one of your goals is to help readers avoid going through the same struggle you did, ensure you're rigorous about describing the exact process they need to follow, and not just a high-level description.

Having clearly defined goals helps you:
- decide where to put priorities (e.g. completeness, original thought, simplicity, ...)
- decide which content is suitable and which content is interesting but would not sufficiently suit your goals and muddle the article
- increase your chances that the reader takes something away from the article


## 3. Topic

### 3.1. Choosing a topic

An important constraint we take into account is time. Writing requires research, and research takes time. Given the amount of time you have (or want to spend), you have to ensure that your choice of topic will allow you to always ensure that:

- all content is factually correct without [plagiarizing](#plagiarism) existing sources. Rephrasing or synthesizing information without having deep knowledge can lead to inaccuracies, e.g. through loss of nuance.
- the topic is sufficiently covered so that it does not leave out crucial components (simply referencing them can be enough)

However, satisfying these basic requirements just ensures that the article is publishable - not that it is compelling. To achieve that, the article should have as many as possible of these attributes:
  - add value in a way that no other existing article has
  - represent information in the most logical and concise way possible
  - contain original thought. This can be something simple, like a new analogy to simplify a difficult topic, your experience in using a library, difficulties you had understanding a topic, ...

It is usually best to avoid broad, generic topics. Because of their broadness, you typically won't be able to achieve the level of mastery needed to write content that is (at least in some ways) better than the existing literature. Instead of "Privacy in Bitcoin", why don't you focus on "How the shadow heuristic leaks privacy"? Or instead of "What is Bitcoin Script?", talk about "Bitcoin Script: some unexpected quirks I found while building a multisig wallet". Even though the topic is specific, you can (and oftentimes should) still introduce the more generic concepts, but now they'll have a purpose and won't be the focus of the article.

Good recipes for a solid topic - each described in more detail below - are:
  - [Describing your own journey](#describing-your-own-journey)
  - [Diving deep into a very narrow topic](#diving-deep-into-a-very-narrow-topic)
  - [Tutorial for a small prototype application](#tutorial-for-a-small-prototype-application)


### 3.2. Describing your own journey

If something was difficult for you, chances are it was for at least a few other people as well. One of the easiest sure-fire ways to find a good topic is to describe your journey of how you achieved something that took a bit of a struggle. This could be trying to understand a concept that was poorly (or not at all) explained in existing documentation or building an application that turned out to be difficult in areas you did not expect. Documenting your struggle will help people understand it more quickly.

> Hint: take quick notes/scribbles/links during your struggle to make it easier to write later on, and ensure you don't miss any steps that were vital to your understanding (but may seem obvious in hindsight)


### 3.3. Diving deep into a very narrow topic

When you're rigorous in keeping the scope narrow enough, you may be able to become enough of an expert to produce new insight (relationships with other topics, benefits and drawbacks, potential implementation problems, ...) or accurately summarize, simplify or explain the topic to a reader with a lesser understanding than you do.

A topic is narrow enough if you're able to confidently research *everything* there is to know about that topic and fully understand all the nuances, criticisms, ... It's okay to set boundaries and clearly state that a certain (underlying) principle or topic is outside of the scope of an article. 

### 3.4. Tutorial for a small prototype application

Your content is almost guaranteed to be both useful and original if you walk the user through the process of building a (small and/or prototype) application, ideally after something you've built yourself. Even if the application idea isn't new or original, it's very easy to make your article stand out, for example through the use of specific languages or libraries, or by having certain features that other tutorials don't yet have.

> Hint: when writing a tutorial, you have to be *really* careful that no crucial information is missing, and that every single step is correct. Ensure the prerequisites and dependencies are properly specified. Triple check all the commands or instructions you provide and try to be thoughtful about having code that is compatible across platforms (or specify when it doesn't).

> Hint: see https://developers.google.com/tech-writing for detailed documentation on how to improve your technical writing.

## 4. Know your audience

### 4.1. Why your audience matters

Say, after a year of dabbling in Bitcoin development you're interested in writing advanced Bitcoin Scripts and are excited to find a book called "The Bitcoin Script Expert". 3 hours and multiple chapters in, all you've read is how to switch on your computer and download a browser to visit the https://bitcoin.org website. Frustrated, you put the book away and leave a not very flattering 1-star review. Even though the book claimed to cater to advanced Bitcoin users, the author didn't properly anticipate the knowledge his targeted audience would already have and scared away exactly the kind of profile the book should have been written for.

It's important to have a well-defined understanding of who you think will be the main audience that can benefit from your writing. Be explicit (at least with yourself, but it can help to define this in the article too) about which knowledge you expect them to have, what you expect them to learn, and what you think could be the best way to do so.

If you define your audience too broadly, you will upset your actual audience as you would be when reading "The Bitcoin Script Expert". Conversely, if you define your audience too narrowly, you may lose some readers that otherwise would have benefited from your writing, but are lacking just a bit too much background knowledge to follow along.

Defining your audience and finding a good balance between assuming not too much and not too little pre-existing knowledge is a delicate exercise, but one that needs to be done anyway. It is often a good idea to link to other sources for prior reading to ensure your audience can fill in any gaps in assumed knowledge before diving into your article. 

### 4.2. The Qala target audience

The Qala program has a very clear technical focus. Most of your writing should reflect that. Even though articles catered to a general audience can be helpful (and are important for the Bitcoin ecosystem in general), these will often not be the best choice for two reasons:

- Writing for a general audience typically requires the subject matter to be significantly summarized and simplified. Perhaps paradoxically, it usually takes an expert to make a sound judgment on how that can be done without losing too much nuance or even being plain wrong. 
- Your goal should be to make yourself stand out for potential employers (and their technical recruiters) and show your level of technical understanding. This is much easier to do with an article catered toward a technical, educated audience.

Even though it's always a good idea to quickly rehash the fundamentals that underlie the article you're writing about, in general, you could assume that your audience already has a reasonable understanding of the basics of the Bitcoin and Lightning Network protocols, and has at least a basic understanding of the programming language you're using (if any).

## 5. Iterate

Everyone's writing process is different, and this guide does not prescribe how you should organize yours. However, especially for inexperienced writers, it's important to realize that your best writing often doesn't come from the first stroke of the pen. 

A good place to start is the outline. Which topics do you want to cover, and what is the most natural order for them to be in? Being explicit about the outline also helps the reader understand what to expect from your article. As you progress with the writing, you can keep reorganizing the outline based on new insights you've gained.

When writing down your thoughts, it helps to be critical throughout, but there's no need to get it perfect right away. You can write down a few sentences, reread them, and see if it makes sense. Is it accurate? Is it complete? Is this the most concise and clear way this could be written? Does it fit in the structure I have laid out? Switching to a different task and revisiting your writing later on can also help bring clarity.

The most important thing is to not be too content too quickly, and keep iterating until you feel like you're not changing much anymore and that you have achieved the kind of quality that you would like your name to be associated with. 

## 6. Don't forget

### 6.1. Grammar

Even though it has nothing to do with the content, having poor grammar is one of the easiest ways to make your article look bad. In general, the reasoning is that if you can't get something as simple as that right, what else is wrong with the article?

Agree with that reasoning or not, improving your grammar has become much easier nowadays thanks to the help of various tools. Many text editors already have this functionality built-in, and there are dedicated tools such as [grammarly](https://www.grammarly.com/) that offer such services for free.

If you're asking someone to review your article, make sure to grammar check your writing every time before submitting it as a draft to avoid wasting their time on easy-to-correct mistakes.

### 6.2. Plagiarism

> Plagiarism is presenting someone else’s work or ideas as your own, with or without their consent, by incorporating it into your work without full acknowledgement.
> 
> https://www.ox.ac.uk/students/academic/guidance/skills/plagiarism

When presenting an idea that is not yours, you'll have to choose between using your own wording or quoting/paraphrasing the original author. You should always strive to rephrase a topic in your own words (e.g. by phrasing from it an alternative perspective, or in simpler terms, or by combining it with other topics). Sometimes rephrasing is not possible or sensible. In that case, it is okay to quote or paraphrase, but you *always* need to clearly indicate which content is quoted/paraphrased and reference the source.

Even though plagiarism is often not illegal, it is almost guaranteed to blemish your reputation if and when it is discovered. Especially in an open-source community such as Bitcoin's, be generous with your references. It ensures the original author receives credit for their work where it is due. As an additional upside, ample linking to high-quality sources is a great way to make your own article more useful. Even if your writing is sufficiently original, it's usually a good idea to consistently reference the sources that inspired your thinking.
