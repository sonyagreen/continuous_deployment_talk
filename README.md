# Intro

I'm Sonya. I work for GitHub, answering support requests. My team has 14 people on it. GitHub has xmillion accounts, and we get about y support requests per day. I'm here to talk with you about supporting continuous deployment and some of the lessons we've learned at GitHub.

You should give a fuck about what I'm about to talk about because

Our developers see that we're doing the best we can to help them: duplicate/validate bugs, pull in screenshots, do the legwork to make it easy for them to understand and want to fix the problems. They respect us for that, and take time to make our lives easier too. It takes more effort on our part to write up, but less time overall when we help them find what's important and they fix things fast.

We collaborate. And have low ego. To help explain this, I'm going to tell you a story. 

This is a story is an example of continuous deployment at GitHub, and something we figured out to do when there's a lot of resistance to a change we make to the site.
https://github.com/github/support/issues/23

You may know, we ship early and often. 
We ship little things all the time.
  (note of someone saying "I did this thing, no one should notice, let us know if you see anything weird")
We ship big things too. 
Here's what the average user-noticable but fairly routine/well tested feature 
Use graphs more to show the dropoff feeling. Find an example (something the audience may be aware of) as a normal graph, then show this one.


One time, we shipped a UI change to our Issues feature. 
This change happened in the beginning of April. 
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

My job is to champion for the users, in ways that best make sense ot the developers. I'm motivated to write up excellent bug reports, because that makes the developers more likely to fix them sooner, which is good for the users! This can be an awesome, supportive cycle if you let it. 

## Reasons why I did this

1. helps you find true bugs
2. what's just people bitching, and will calm down in x days (where x is determined by your userbase)
3. Problems that warrant discussion, even if you don't change anything


## here's how you can apply this

You may not have GH/ownership access. But you can do this.


I'm not a developer, and I didn't need to understand the code to be able to make this dossier. Your support team, however they're working with you, or if you know your company has one?

I'm not a dev, just analytical. Your support people may already be like this.

Support's not told "just deal with it". We have power. We still deal with whatever is rolled out (yay, continuous deployment). We fully embrace the "ah, they'll get used to it" aspect. If the spike doesn't drop, that's when you have this kind of situation.

I have ownership access to github/github, I don't know other companies whose support people do. But I have access to read the PRs, to add issues directly to GH. I've read PRs from the designers, I know something about how they work. This made me understand what was important, and comfortable to share this.

(more here, show that we're way over on the side of +support+ from the company where no one communicates beyond support)

These situations can be stressful, which means we need to able to stay calm and pragmatic. Personally, whenever I start to realize I'm losing my cool, I turn to animated gifs. You have to find your own power gif., but I'll leave you with my favorite. 







