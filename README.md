## Intro

Hi! I'm Sonya. I work for GitHub, with the support team. So you have some sense of what our support team is dealing with, we have 14 supportocats. GitHub has 3.5 million accounts (I even removed the spammy ones for ya), and we get about 250-300 support requests per day. I'm here to talk with you about supporting continuous deployment and some of the lessons we've learned at GitHub.

## You should give a fuck about what I'm about to talk about because

You may know, GitHub ships early and often*. We have lots of users, who do complicated technical things with GitHub. We have many support requests coming from users who understand our products nearly as well as we do. (BTW: this is amazing. Users debug stuff for us, offer solutions and are understanding when we have bugs.)

We ship little things all the time.* These are blips on our radar. We often don't know about them until they've shipped and we get a heads up.
We ship really big things too. When these happen, we are looped into the pull request, and have used the feature in staff-only mode.

So here's our secret to continuous deployment big and small, and supporting it happily: developers and support collaborate.

Support is inherently motivated to write excellent bug reports. Why? If we make it easy for the developer to see what's wrong, it lets them start to think about what needs to be fixed. They respect us for that, and in return take time to fix bugs and help us answer the tricky questions. They're grateful to not have to do the extra work. This means they're more likely to care about the bug (because we've shown we already care), and jump on fixing it. It takes more effort on our part to write up great bug reports, but less time overall when we help them find what's important and they fix things fast. That means happier users, and overall less work for us because it stems the flow of incoming reports of said bug.

A good bug report involves duplicating the bug to make sure it's not one of those things like a weird browser or user error (*we once were alerted to a unpressable button ... when we asked what browser, they told us: the Wii browser.) 

A good bug report involves taking the time to list the steps to recreate. It involves screenshots when it would otherwise require the developer to go check it themselves. It involves using analytical skills (or, as I prefer to think of it, spidey sense) to know when looking at two seemingly unrelated support requests, and seeing the connection. (Because bug symptoms can be weeeird.) 

Your support team can do this. They don't need access to the code, and they certainly don't need to have a technical background. They're looking at complaints all day. If they have a sense of pattern recognition, they'll pick up on it. Writing up bug reports well means they'll practice finding the bugs, and they'll get good at it.

So, like I said, GitHub developers and support collaborate. We communicate together in the Issues, and in our support system. Yes, everyone at GitHub has access to our support system. Transparency means we all can know what's going on.

I'm going to give you a sense of a "normal" support load for a new feature. 
When there's more than just a small splash, the support team will start amassing what we call an "incident report" - tldr, PR/issues already known, prp, canned responses.

Here's another secret: we really, really try to have low ego. To illustrate this, I'm going to tell you a little story. 

This is a story is an example of continuous deployment at GitHub, and something we figured out to do when we have a feature that was no small blip, but not a huge rollout either. Sometimes, you ship something that you think is going to go out with a whisper, and surprises you.

So, a few months ago, we shipped a UI change to GitHub Issues. 
This is what our Issues used to look like
(screenshot)
This is what we shipped
(screenshot of Shades of Grey) 
Within hours of the deployment, support was getting a steady of feedback from users.
Now, humans are known to hate change. When you change to something new, inevitably someone will say "I LOVED the old way, you should go back to the old way".
In all this feedback, there were reports of some straight-up bugs, a lot of general I-liked-it-the-way-it-was comments ... this is pretty standard ... but then there were also some concerns about the lack of readability.

The design team had worked HARD on this. They were proud of the aesthetic.

So, I looked at the queue of support requests with varying concerns, and I thought about the best way to present 
* a bunch of data
* from humans (our humans, our users)
* that was emotional
* and contained bugs
* and inflexible thinking
* and also totally reasonable concerns

in a way that wasn't going to overwhelm or give a knee-jerk reaction of inflexbility as well. I decided instead of immediately opening 8 different issues (which never goes over well), I wrote up one dossier. I presented the whole of it, in a way that wasn't overwhelming. 
(fuck yeah, "dossier", love that word. maybe define)



3 lessons: how we fixed it

First, compiled list of what I though were clearly bugs. This is the softball lob. How is it that I know what a legimitate bug is (as opposed to user's opinion, or unretestable)

Second, the biggest UI complaint: that the label colors were too pastel, and the background grey, which is all fine et dandy if you're on a giant retina display, but maybe not on a smaller, older screen. 

This has a big component to it, that I learned from the library world but is also A Thing in the UX world: stats and stories. Stats alone fall flat, especially with those who understand to be sketical about flashy stats. The other part is what I like to call "when it hits you in the feel" -- when a user's explanation of the problem is more eloquent than your own understanding of it. 

(show stats and quotes)

(label quoet)
We dogfood github, but we're not the majority.

Third, since I'd written up all this info so far, I figured they'd like to know about the long tail. (They would want to see everything everything)

I tl;dr'd the rest of the things, so they knew. There weren't THAT many, and they weren't that bad. Key: I summarized them.

I was super nervous about showing this to others. I spent most of a day on it, and I figured I could just keep it to myself, and it was still useful to get a sense of the landscape. But, I fuckin' shipped it. I made it available to the GitHub design team (our workflow is that we have a private repository called support/ which we use to spec out potential clusters of tickets that indicate a problem, and we can @mention a team (like @design) to send them all a notification of it). I thought this could be seen as a monkey wrench in what they rolled out, harmful and distracting rather than helpful, but ... 

Turns out, they loved it
(quote)

What came of all this? Having a low-angst dossier with lots of places to dig in and discuss how users were responding to the new UI meant that the design team were able to assess it with minimal ego, and make the best decisions. They fixed the bugs. They discussed the label colors, iterated on the design to benefit readibilty ... and ultimately decided to roll back the label color change.

Now, we don't often roll things back, so it's impressive. I'm proud of them. 

My job is to champion for the users, in ways that best make sense ot the developers. Emopathy going both directions. I'm motivated to write up excellent bug reports, because that makes the developers more likely to fix them sooner, which is good for the users! This can be an awesome, supportive cycle if you let it. 

## Reasons why I did this

1. helps you find true bugs
2. what's just people bitching, and will calm down in x days (where x is determined by your userbase)
3. Problems that warrant discussion, even if you don't change anything


## here's how you can apply this

(make punchier - more bullet points)

Your support may not have GH/ownership access. But you can do this.

* work with your support team to get those bug notes out of their heads and down in a report. Honestly, it's hard to want to write it up well when there are other requests piling up, but you can make them <3 you for it, by thanking them for the work, by fixing things fast or at least reporting why you can't. This makes support able to return to those users and either get to deliver good news (which is a job we love), or be able to manage the users' expectations better.

I'm not a developer, and I didn't need to understand the code to be able to make this dossier. Your support team, however they're working with you, or if you know your company has one?

I'm not a dev, just analytical. Your support people may already be like this.

Support's not told "just deal with it". We have power. We still deal with whatever is rolled out (yay, continuous deployment). We fully embrace the "ah, they'll get used to it" aspect. If the spike doesn't drop, that's when you have this kind of situation.

I have ownership access to github/github, I don't know other companies whose support people do. But I have access to read the PRs, to add issues directly to GH. I've read PRs from the designers, I know something about how they work. This made me understand what was important, and comfortable to share this.

(more here, show that we're way over on the side of +support+ from the company where no one communicates beyond support)

These situations can be stressful, which means we need to able to stay calm and pragmatic. Personally, whenever I start to realize I'm losing my cool, I turn to animated gifs. You have to find your own power gif., but I'll leave you with my favorite. 
