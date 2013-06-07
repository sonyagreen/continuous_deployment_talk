## Intro

Hi! I'm Sonya. I work on the GitHub support team. So you have some sense of what our support team does, we answer support requests (by email, no phone or chat), mostly from GitHub users, and some potential users. There are 4 million accounts on GitHub, and we get something like 300 new support requests per day, and we reply on average to 550 times. We have 14 supportocats (on any one day, there are about 10 answering support requests). I'm here to talk with you about GitHub's continuous deployment workflow, how support fits into it, and a couple of interesting things we've learned.

## You should give a fuck about what I'm about to talk about because

GitHub ships early and often*. We have lots of users, who do complicated technical things with GitHub. We have many support requests coming from users, who understand our products nearly as well as we do. (BTW: this is amazing. Because our userbase is developers, they debug stuff for us, and even suggest solutions. They're understanding about the bugs, like "hey, we get bugs too!")

At GitHub, the support team is part of the continuous deployment workflow.
* ship something, +support chat room
* async - always someone around in chat to help even if you've signed off
* pace can be fast

But here's our secret to continuous deployment big and small, and to supporting it happily: developers and support collaborate.

We ship little things all the time.* These are blips on our graph. We often don't know about them until they've shipped and we get a heads up. We don't need to know about them beforehand, because they don't generate a lot of support requests.

We ship really big features too (a recent example is the contributions graph*). When these happen, we are looped into the pull request before it's done, and get to experience it in staff-only mode before it's released to everyone.

Another way we collaborate is that the support team has access to all the code and issues. From what I know of other companies, this is unique: we have access to PRs, so even if we don't read code, we can read the associated comments and discussion, which gives HUGE context when figuring out what's going on, and what to tell the user.

GitHub support often writes up bug reports (at GitHub, we use our Issues feature for bug tracking).

Support is inherently motivated to track down bugs and write really good bug reports. Why? 
* we start seeing bugs reported from users
* users give us valuable clues in how they describe what's wrong (well, from our users we get annotated screenshots and terminal outputs)
* support wants to fix bugs fast (stop the flow of reports of the same problem from many people; get to reply to users who reported the bug, get to say "it should be fixed now")

So we make it easy for the developer to see what's wrong and fix it fast. 
 * duplicate & recreate steps bug
 * make sure it's not user error or something like an unsupported browser (*we once had a user report a site bug ... when we asked what browser, they told us: the Wii browser ... which technically is Opera, which isn't one of our supported browsers.)

Support people have analytical skills (or, as I prefer to think of it, spidey sense) We know when looking at two seemingly unrelated support requests, and seeing the connection. (Because bug symptoms can be weeeird.) Unless YOU'RE looking at the support requests, you wouldn't necessarily see this. (Props to all of you who are developing a project where you're also supporting it.) 

As a developer, if you have this great bug report in front of you:
* you can start to see what needs to be fixed
* you may feel relief to not have to reproduce or document it
* more likely to care about the bug (because we've shown we already care by writing it up carefully, and by showing what there is to care about)

It takes effort on our part to write up great bug reports, but less time overall when we help the developers find what's important and they fix things fast. That means happier users, and overall less work for us because it stems the flow of incoming reports of said bug.

Your support team can do this. They don't need access to the code, and they certainly don't need to have a technical background. They're looking at user-reported problems all day. If they have a sense of pattern recognition, they'll pick up on it. Writing up bug reports well means they'll get to understand the difference between a true bug (when what you meant the code to do and what users are experiencing are two different things), and when a user wants something different than what you made. In either case, support needs to know the difference. 

So, like I said, GitHub developers and support collaborate. We communicate together in the Issues, and in our support system. Everyone at GitHub has access to our support system. Transparency means we all can know what's going on.

Back to that continuous deployment, I'm going to give you a sense of a "normal" support load for a new feature. Say it's a big feature*. 
* figure out legit bugs, get on those
* people can really hate when things change. When you update to something new, inevitably someone will say "I LOVED the old way, you need to go back to the old way".
* long tail of complicated bugs, workflows that were affected, people on vacation/casual users

Here's another secret: we really, really try to have low ego about bugs. In fact, GitHub hires for low ego. People need to be able to talk pragmatically about what's going on. It can be really hard to scrutinize hard work you've done -- like calling your baby ugly. To illustrate this point, I'm going to tell you a little story. 

This story is an example of continuous deployment at GitHub, and something we figured out to do when we have a feature that surprised us with the amount of support responses. Sometimes, you ship something that you think is going to be easy to support,  you get surprised by the depth and breadth of bugs and functionality.

So, a few months ago, we rolled out a UI update to GitHub Issues.* This was mostly driven by the design team, but I want to mention that most of our designers are developers, so through this story, I'm talking about this team.

Within hours of the deployment, support was getting a steady stream of feedback from users. The design team had worked HARD on this. They were proud of the design aesthetic, as well as the functionality changes that were part of the update.

Sorting through the feedback, there were the usual reports of straight-up bugs, a LOT of general I-liked-it-the-way-it-was comments ... again, this is pretty standard ... but mixed in were also concerns about the lack of readability. This wasn't a bug -- the site was displaying as intended, but the things the users were saying was cause for thought.

Looking at the queue of support requests with varying concerns, we needed a way to look at:
* a bunch of data
* from humans (our humans, our users)
* that was emotional
* and contained bugs
* and inflexible thinking
* and also totally reasonable concerns

in a way that wasn't going to overwhelm or give a knee-jerk reaction of inflexbility as well. They didn't need to read things like this.* Digestible. Instead of immediately opening 8 different issues (which never goes over well), we condensed into one document. I've taken to calling this a dossier*. 

So, here's how we fixed it

First, we compiled list of what seemed to clearly be bugs. This is the softball lob for the developers, there are easily identifiable actions to take to fix this.

Second, we complied information about the biggest UI complaint: that the label colors were too pastel, and the background grey, which is all fine et dandy if you're on a giant retina display, but maybe not on a smaller, older screen. 

There's something to know here. To convey a problem in a way that is gripping, use stats and stories. Stats are important*, but fall flat on their own. (side note: these are links to our support system, called Halp)

The other part is what is called "when it hits you right in the feel"* -- when a user's explanation of the problem is more eloquent than what you could describe. It means more, coming from an actual user, an actual person out there.

We dogfood github, but we're not the majority. None of us are, which is a reason to find a way to keep your finger on the pulse of your actual users.

This dossier was written up so support could summarize everything, get a sense of the landscape. I was super nervous about showing this to the design team. I figured we could just keep it to ourselves, and it was still useful. But, I fuckin' shipped it. I made it available to the GitHub design team (our workflow is that we have a private repository called support/ which we use to spec out potential clusters of tickets that may be a problem, and we can @mention a team (like @design) to send them all a notification of it). I was worried that the design team loved their work so much, that this would feel like a hit over the head, harmful and distracting rather than helpful, but ... 

Turns out, they loved it * *

They jumped on bug fixes right away, and started a conversation about how to address the readability problems.

What came of all this? Having a low-angst dossier with lots of places to dig in and discuss how users were responding to the new UI update meant that the design team were able to assess it with minimal ego, and make the best decisions. They fixed the bugs. They discussed the label colors, iterated on the design to benefit readability ... and ultimately, days later, decided to roll back the label color change. * aaaand *

Now, we don't often roll back big visible UI changes, so it's impressive. They did what was right for users, not what they wanted. I'm proud of them. 

Support's job is to champion for the users, in ways that best make sense ot the developers. Empathy goes both directions - to our users, and to our developers. We're motivated to write up excellent bug reports, because that makes the developers happy, and more likely to fix them sooner, which is good for the users! It is an awesome, supportive cycle.

## Reasons why I did this

So, if you have a support team, consider how you can work together. The incoming skill level for support varies widely, but any good support person can learn the analytical skills to become a bug hunter. You can leverage their inherent knowledge of your users. Get that knowledge about your bugs out of their heads.

From the perspective of support, honestly, it's hard to want to write up a good bug report when there are other support requests piling up, but you can make love you <3 you for it, by thanking them for the help, by fixing things fast or at least letting them know why you can't. This makes support able to return to those users and either get to deliver good news (which is something we love), or be able to manage the users' expectations in the reply.

I want you to know, I don't know how to code, and I didn't need to understand GitHub's code to be able to do my job well. Your support team, however they're working with you, however technical their knowledge, can work with you.

Together, you can then fix bugs faster and get on to the next adventure.

On fixing those sticky problems like our UI change, remember that when you can check your ego, you can talk pragmatically. This means you can discuss problems well. If you can stay open-minded about what needs to happen next, and not get distracted about saving your baby, you can look a problem and feel like it was worth discussing, even if you don't change a thing.

Situations like a the story I told can be stressful, which means we need to able to stay calm and pragmatic. 

So here's my Pro Tip™: whenever I start to realize I'm losing my cool, I turn to animated gifs. Now, you have to find your own power gif., but I'll leave you with my favorite.
