---
layout: post
title: Coursework vs. Production code
tags: []
status: publish
type: post
published: true
meta:
  dsq_thread_id: '808770976'
  _edit_last: '1'
  _yoast_wpseo_linkdex: '0'
---
I've been speaking to a number of first-time technical entrepreneurs recently who are starting businesses for the first time. One question I often get is regarding the difficulty involved in writing production code. Given that probably a lot of them (you) have similar experience to what I did, I thought I'd share some reflections I had about the differences between academic work and production coding.

<em>Programming at a startup is, in general, much easier than the work you've already done in school.</em>

I'm assuming a lot of things when I say this. Naturally, I'm assuming that you challenged yourself while you were in school. You took some of the hard classes and didn't just coast through the easy ones [1]. You completed all of your assignments (likely taking multiple late days, but hey, finishing is finishing :P).

In school you work on problems that get progressively harder. By the time you reach the upper division classes, you working out non-trivial proofs about algorithms that took you multiple lectures to understand. Even if you're not in a theory track, you'll be expected to grok papers about the newest research in the field. Not to mention, (since you're a CS major) you're probably taking 3-4 of these classes at the same time. [2]

In my opinion, this kind of pencil pushing is way harder than coding! It is very difficult to implement, say, a non-trivial variation on a maximal matching algorithm for bipartite graphs from your brain, with nothing but pencil and paper, on an exam. You don't even know if you can do the problem or not, let alone write anything down on the paper! If you fudge a "clever hack", that's zero credit. Because it's not clever, it's just plain wrong.

The real world is not quite so unforgiving. For one, you will almost never a problem in software that you can do nothing about. If you're stumped on a tough architecture decision, just look up standard practice on Wikipedia. Phone a friend. Take a walk around the neighborhood and then decide that it's not really a problem that you have to do anything about. It's software so there has to be a way to get it done.

<em>Unlike the code you write in school, everything you write in production has TONS of bugs in it.</em>

When I was in college, we had unit tests given to us for everything we wrote. For CS140 - Operating Systems (by the way, this was perhaps my favorite class at Stanford, every CS major should take it), our team would have gotten absolutely destroyed if those unit tests did not exist. But because they did, we had a notion of progress. We'd make the tests pass, turn the project in, and call it a night (or early morning). I'd generally know if I did a good job on the programming or not before I had turned in my assignment. Once I'd turned it in, I'd never have to look at it again.

My analogy for unit tests is that they're like monkey cages. Programmers (myself definitely included) are the monkeys. If left to their own devices, they'll chaotically bang on their keyboards, and create a total mess for themselves and all of the other monkeys. Sooner or later it'll be Planet of the Apes. The cages provide structure and prevent the monkeys from making a total mess of things.

In the code I write now, I assume that nothing works unless I've tested it and it works. Even then, it still probably doesn't work, because I probably wrote the test incorrectly. If I find what looks like a JVM error - hold your horses, it's not a JVM error, you screwed up - I'll assume that there's something wrong in my own code. If I didn't think like this I would probably not find any bugs.

<em>You spend almost as much time getting the requirements correct as you spend building the damn thing.</em>

One of my favorite classes (other than Operating Systems) that I took at Stanford was CS155 - Computer and Network Security taught by John Mitchell and Dan Boneh. When I took it, the class had the Operating Systems class (CS140) was a prerequisite. Since I was just a sophomore at the time, I hadn't taken Operating Systems, but after sitting in the first lecture found the class so interesting that I signed up for it anyway. [3]

I strongly remember the second project, because that project just about killed me and my partner. In the project, we were asked to implement traceroute, in C. Implementing traceroute itself is challenging enough for a class of students who haven't taken networking. But we were additionally asked to implement <em>highly non-trivial</em> variants of traceroute. These included firewalking traceroute (if you don't know what that is don't worry, it burns just about as hard as it sounds) and ghost traceroute (this was actually illegal, so we were only allowed to test in a small lab provided to us on campus).

If this weren't hard enough, the documentation left basically the entire assignment ambiguous. To figure out basic information, such as which ICMP headers to send under which circumstances, you'd have to pore through the newsgroup, which contained tons of other confused students and very few actual answers. By the time we had finished the assignment, the newsgroup had something like 3000 posts in it.

My partner (another sophomore) and I read them all. We finished the assignment. Actually, I think we were one of the only teams to finish the assignment because the average score on that assignment was 24/100. By the way, I want to tell you that I attribute our score on that project<em> completely</em> to my partner, who is the best networking engineer that I know. Some people are just that good.

The funny thing about that assignment was that it was actually more spec'd out that anything I have ever written since graduating. Traceroute has an RFC. Also, once the description of the problem had been cemented, we knew exactly what to write. We never had to delete all of our code because the specification changed. No one ever said: "Wait, are you really building traceroute? wtf, actually what I want is a program that draws a bunch of unicorns on the screen!"

<em>Some final thoughts (as usual):</em>

My undergraduate advisor was Mendel Rosenblum. I went to visit him recently, and asked if he had any advice about creating software for the real world. He just told me that he had no advice for me and that I really ought to just figure it out myself. But actually, after thinking about it that is pretty good advice.

&nbsp;

[1] You can actually do this now, and it infuriates me! From my point of view as an employer I don't even know if someone really even knows CS, based on the fact that they have a CS degree alone. I'll save the rant for some other day, though.

[2] There's one CS major that know who took 7 classes at the same time. I lived in the same dorm with him and never saw him eat a meal outside of his room (however, he did shower - the whole thing about CS majors never showering is just total BS). Some people are just that good. I mean, it's Stanford, who am I kidding?

[3] The CS program at Stanford doesn't really enforce prerequisites, so you can take whatever you want if you can handle it. When I was an undergrad, I tended to do this a lot when I was first getting into CS. However, I would definitely not recommend it even if you think that you can. The gist of my point is that taking classes early is hard because you won't (in general, myself excepted) have good partners. Also, it means that you'll have to take the lame easy classes later, because they're required anyway. Trust my co-founder, you don't want to be learning about induction in CS103 (Mathematical Foundations of Computing) when you've already done it in CS161 (Design and Analysis of Algorithms).
