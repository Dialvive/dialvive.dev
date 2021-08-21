---
title: About GitHub Copilot
tags: [Personal]
style: border
color: primary
description: Welcome to the future?
---

GitHub Copilot is no longer news, it has been around for a little while on developer preview, some hate the idea of a programming AI, while others love it. Is it really the
devil/angel people say it is? I have downloaded and did some tests on non work or school related programs. There are some serious ethical issues around it, I'll explore some
of them, and talk about it's usability and usefulness. 

![Space Odyssey 2001](/assets/img/hal.png "Space Odyssey 2001")
<p class="caption">
    Space Odyssey 2001: the tool overcoming the humans (?).
</p>

Many people are against the creation of self programming artificial intelligence, and while GitHub Copilot (Copilot from now on) is not quite there, it is a step forward.
The moment I heard about copilot, I instantly went and register to the beta. After a week or so, I was accepted and I installed it into VSCode. Long story short: I is so
intrusive that makes it so annoyng to use. I was constantly distracted by it's continuos guessing, not like in an old fashoned IDE way (with a little pop up guessing up 
to a line of code), no no, each guess occupied at least 3 or 4 lines of grey code in the same editor I was trying to write, and that happened almost randomly, making me
stop writing, looking at the suggestion, discarding it (being way off of what I was trying to do), and continue writing until the next ~~distraction~~ *suggestion* arrived, 
not pleasant at all.

But I've seen at the Copilot's Github issues a lot of developers that report almost magic being performed by it, some said *"Copilot knows quantum chemistry!!!"*, *"Copilot
predicts TSLA stock will remain flat..."*, etc. So it works for some people I guess, let's assume it works a 100% of the times: Then it is  a wonderful tool, I just have to
write a comment about what I want to do (not a whole program, but maybe a complete step like a for, switch, REST API connection, etc.) and it gives a correct suggestion that may 
need one or two tweaks. Well, that could help us avoid the "bloat" code and get right into the logic of the program, speed up the development process, and have a happier life...
right? 

Even if Copilot was -or were to become- that great, there are some questions that need to be asked, like: what data does Copilot uses to train itself? (It is trained with GitHub's
public repositories, surprise!), What happens if a suggestion is identical to a code block in its training set? (It somehow links the public repo and its license), Is it
compatible with open source licenses? (I'm not sufficently informed, but almost certainly not, see this [wonderful blog entry](https://zephyrtronium.github.io/articles/copilot.html) if 
you want to dive into it).

I firmly believe that Copilot is not a tool that will overcome human developers, nor enslave hummanity whatsoever. But I do think it is a really evil move from ~~Microsoft~~ 
GitHub. I'm sure most big projects stored in GitHub wouldn't consent to have their open source code used to train a for-profit programming AI. If they actually ASKED developers
if they would like to have their code analyzed and used to train and improve AI by GitHub itself, then they could have a solid ethical ground. Using user terms and conditions 
to manipulate users and use their assets and contributions is nothing but an evil move. I just had a realization, should we really trust code (open source or not) to a for-profit 
company that creates things like Copilot? It's obvious that respecting their users trust, and their repositories' licences is not a priority.
