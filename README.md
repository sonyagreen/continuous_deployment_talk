magmaconftalk
=============

Magmaconf talk

# Intro

I'm Sonya
I'm not a developer.
I'm a librarian (amongst many other things)
(slide of that?)
Part of why I'm good at my job is because I know how to respond to a question. Just like a reference librarian, I don't need to know the answers, I just need to know how to put the user and the answer together. I also need to know what the user is actually asking, and the best way to deliver the information.
(slide of vague question, slide of awkward-to-answer question)


# Let me tell you a story. This is a story is an example of continuous deployment at GitHub, and what we figured out to do when there's a lot of resistance to a change.
https://github.com/github/support/issues/23

You should konw, we ship early and often. 
We ship little things all the time.
(note of someone saying "I did this thing, no one should notice, let us know if you see anything weird")
We ship big things too. 
One time, we shipped a UI change to our Issues feature. 
This change happened in the beginning of April. 
This is what our Issues used to look like
(screenshot)
This is what we shipped
(screenshot) https://a248.e.akamai.net/camo.github.com/cfb16f5192be91b1ff2b8cd87eb7457d715e40ef/687474703a2f2f692e696d6775722e636f6d2f643231776a30622e706e67
Within hours of the deployment, we were getting support requests from users.
Now, people are known to hate change. When you change to something new, inevitably someone will say "I LOVED the old way, you should go back to the old way".
In all this feedback, there were reports of some straight-up bugs, a lot of general I-liked-it-the-way-it-was comments ... this is pretty standard ... but then there were also some concerns about the lack of readability.

The design team had worked HARD on this. They were proud of the aesthetic.

So, I looked at the queue of support requests with varying concerns, and I thought abou the best way to present 
* a bunch of data
* from humans (our humans, our users)
* that was emotional
* and contained bugs
* and inflexible thinking
* and also totally reasonable concerns

in a way that wasn't going to overwhelm or give a knee-jerk reaction of inflexbility as well. I decided instead of immediately opening 8 different issues (which never goes over well), I wrote up one dossier. I presented the whole of it, in a way that wasn't overwhelming.
(fuck yeah, "dossier", love that word. maybe define)

3 lessons: how we fixed it

First, compiled list of what I though were clearly bugs. This is the softball lob. 

Second, the biggest UI complaint: that the label colors were too pastel, and the background grey, which is all fine et dandy if you're on a giant retina display, but maybe not on a smaller, older screen. This has a big component to it, that I learned from the library world but is also A Thing in the UX world: stats and stories. Stats alone fall flat, especially with those who understand to be sketical about flashy stats. The other part is what I like to call "when it hits you in the feel" -- when a user's explanation of the problem is more eloquent than your own. 

(show stats and quotes)

Third, since I'd written up all this info so far, I figured they'd like to know about the long tail. I tl;dr'd the rest of the things, so they knew. There weren't THAT many, and they weren't that bad. Key: I summarized them.

I was super nervous about showing this to others. I spent most of a day on it, and I figured I could just keep it to myself, and it was still useful to get a sense of the landscape. But, I fuckin' shipped it. I made it available to the GitHub design team (our workflow is that we have a private repository called support/ which we use to spec out potential clusters of tickets that indicate a problem, and we can @mention a team (like @design) to send them all a notification of it).

Turns out, they loved it
(quote)

What came of all this? Having a low-angst dossier with lots of places to dig in and discuss how users were responding to the new UI meant that the design team were able to assess it with minimal ego, and make the best decisions. They fixed the bugs, they discussed the label colors, and ultimately decided to revert them to full opacity.

Now, we don't tend to revert things, and I don't expect us to do this frequently, but it's impressive. I'm proud of them. My job is to champion for the users, in ways that best make sense ot the developers. I'm motivated to write up excellent bug reports, because that makes the developers more likely to fix them sooner, which is good for the users! This can be an awesome, supportive cycle if you let it. 

Remember that I'm not a developer, and I didn't need to understand the code to be able to make this dossier. 

## Long-term benefits

Developers see that we're doing the best we can to duplicate/validate bugs, pull in screenshots, do the legwork to make it easy for them to understand and want to fix the problems. They respect us for that, and take time to make our lives easier too. It takes more effort on our part, but 

These situations can be stressful, which means being able to stay calm and pragmatic. Personally, whenever I start to realize I'm losing my cool, I turn to animated gifs. You have to find your own power gif., but I'll leave you with my favorite. 
