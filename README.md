# PrintYourDay for wedding planners

A site for Adam, who runs PrintYourDay, a studio in Mount Vernon, NY that prints
photos at 40 by 60 inches on foam board for events. This site is for wedding
planners, and the one thing it has to do is get them to call him.

Who opens this, and what do they need in the first five seconds: a wedding planner
on a phone, between two other vendors, who needs to see that these people do big
photo boards for events and find the number to call.

Live site: https://zayd123455.github.io/printyourday-business/

Files: `PROPOSAL.md` is the client brief from my conversation with Adam. `sketch.jpg`
is the layout I drew before any code. `PRD.md` is what the agent wrote from the
proposal, corrected by me. `AGENTS.md` is the rules the agent follows on every
request. `css/styles.css` is the one stylesheet, built on the six values in the
PRD's `:root` block.

## The required question

**Pick one piece of AI output you did not accept as-is. What did it give you,
what did you change, and how did you know it needed changing?**

The gallery page in commit `72897ea`. The agent built it from PRD.md as one grid
of six photos, and it captioned two of them "The Five, in the studio before
delivery" and "The easel stand, $25 each". Those are true captions, but check 3
in PRD.md says every photo in the gallery has a caption naming the event, and a
studio shot and a close-up of a stand are not events. I only noticed because I
ran the checks one by one instead of looking at whether the page seemed fine,
which it did.

The fix is in the next commit. The four event photos stay under "Boards at real
events" with captions that name the event. The two product shots moved into their
own section, "The boards and the stand", so the page still shows all six photos
without pretending a studio photo is a wedding. In the same commit I took
`loading="lazy"` off the first two gallery images, because they are above the
fold on a phone and lazy loading only delays images the visitor is already
looking at.

What I did to verify the rest of the first build: opened every page at 320 and
390 pixels wide in DevTools and read `document.documentElement.scrollWidth` to
confirm there is no horizontal scroll (check 5); tapped the phone link in the
header on each page (check 1); found the price of The Five on the home page in
one scroll (check 2); and searched every file for the name of Adam's other
company, which must not appear (check 4).

## Client feedback

Adam has the live link. His feedback, and what changed because of it, goes here.
