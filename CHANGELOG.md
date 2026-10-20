# Changelog

> **Automated notice.** Entries here, and the release emails generated from them,
> are produced automatically on every push to `main`. Nobody types them
> individually and no reply is expected. If something needs discussion, contact
> Fatima directly.

Every change to the site, newest first. Each entry says what changed and
whether anything is needed at deploy time.

The site is a **single static file** — `index.html` — plus `og.jpg` and the
contents of `img/`. There is no build step, no dependencies and no server-side
code. Deploying is a straight file copy.

**Deploy = pull `main` and copy these to the web root:**

    index.html
    og.jpg
    img/            (whole folder)

`og-card.html`, `README.md`, `img/README.md` and this file are source/docs only
and do not need to be served (harmless if they are).

---

## Unreleased

### Saturday 1pm becomes "Selling to the Government", with Ian Quan
The 1:00 pm workshop is retitled **Selling to the Government: A Hands-On
Workshop** and its blurb replaced with the committee's wording, which names
**Apex Accelerator (Ian Quan)** alongside Hussain Ezzy, Fakhruddin Cutlerywala
and Huzaifa Hussain. Ian Quan joins the agenda row and the speaker grid, the
four cards now read "Selling to the Government" as their session, and the
hero's speaker count moves from 14 to 15.

### Raffles and Networking Bingo close both days
The 3:00 pm slot on Saturday and Sunday was "Programme to be announced"; the
committee confirmed raffles and the networking bingo run both days, so each
now carries that title and a one-line note.

### Five portraits, supplied by the committee
`img/speaker-saba-haider.jpg` and `img/speaker-ian-quan.jpg` &mdash; the markup
already pointed at these filenames, so the avatars pick them up with no other
change. Ian Quan's source is only 147px wide and renders soft in the 64px card
until a larger file arrives. The three guests of honour who were on initials
&mdash; Dr. M. Anand Prakash, Zaman Mehdi and John Curran &mdash; now have
`img/guest-*.jpg` portraits cropped to the same 369&times;420 frame as the two
House portraits. Saba Haider's cut-out arrived on solid black; the background
was flood-filled to a pale lavender so the circle has no dark corners.

### Sunday keynote badge
"Speaker announced soon" becomes **"Speaker to be announced"**.

Mirrors the same changes made to the event page on tr.chicagojamaat.org
(ASCChicago/tr-react-app PR #39, live 20 Oct 2026). Deploy: `index.html` plus
the five new files in `img/`.

### The Saturday keynote gets a promo band, and Abidali a portrait
The committee's own social card for the keynote now runs as a band straight
after the programme, so it lands on a reader who has just passed the 11:00 am
slot. It is the one place on the page with a direct **Register to attend** CTA
attached to a named draw.

The artwork already carries his name and title in its own typography, so the
copy beside it deliberately does **not** repeat them &mdash; it gives the slot,
the session and the action instead.

His face was cropped out of the same card for `img/speaker-abidali-neemuchwala.jpg`,
which the speaker card and his agenda avatar pick up automatically &mdash; the
first real photograph of any of the fourteen. The crop keeps the card's yellow
backing, which reads deliberately in a circle.

**Two naming notes from the artwork.** It gives his full name as **Abidali
Zainuddin Neemuchwala**, where the page says "Abidali Neemuchwala". And its
title line is **"Co-Founder and Director at Dallas Venture Capital"** with no
mention of Wipro &mdash; the "previously CEO and Managing Director, Wipro" half on
the page came from project notes, not from committee material. Both left as they
are for now; the committee should pick which is correct.

### Guests of honour get a section
The five public officials were one sentence &mdash; "Also expected to attend:" &mdash;
run together at the foot of the agenda. They now have a section of their own
with a card each, following the brochure's page 2 ("Distinguished Guests of
Honor"), which gives the two Congressmen a portrait and the honorific.

**Portrait rights are not a question here, for once.** Both are official US
House portraits &mdash; works of the federal government, so public domain. They
were pulled out of the brochure PDF with `pdfimages` and its gold frame cropped
off. New files: `img/guest-raja-krishnamoorthi.jpg`,
`img/guest-jonathan-jackson.jpg`.

The cards borrow the speaker card's shape but frame the portrait as a rounded
rectangle rather than a disc: a circular crop cuts the composition of a formal
portrait, and the different shape says "not a speaker" without a label. The
three guests with no photograph fall back to initials on a tint, exactly as the
speaker avatars do.

**Still outstanding, and more pointed now there are faces:** none of these
offices has been asked whether they are content to be named and pictured on a
public page.

### The schedule shares one time axis
The two days were independent stacks, so the hours did not line up. Saturday
10am is a one-line open slot; Sunday 10am carries a four-speaker panel &mdash; so
by 11am the two keynotes, the thing a reader most wants to compare, sat about
150px apart, and 1pm on one day was level with 2pm on the other. "11:00 am" was
printed fourteen times.

Both days run the identical seven hours, which makes a shared axis possible.
There is now **one grid**: an hour rail down the left, then that hour on each
day. Rows size to the taller card. The keynotes line up and read as a pair &mdash;
one named, one pending. "What is on at 1pm" is a glance. Fourteen time labels
become seven.

Open slots stretch to their row and centre their text, so a short card reads as
a deliberate block rather than floating in the gap left by a tall neighbour.

**Below 880px** there is no room for a rail plus two columns, so it collapses to
one column grouped **by hour**: the rail label becomes a full-width row heading
and each card names its own day. Grouping by day instead would need a different
DOM order than the desktop grid.

### Who attends, and why &mdash; rewritten from the 2026 brochure
Both sections now use the committee's own "Biz Connect Showcase &mdash; Event of
the Year 2026" brochure, which makes the case far better than the page did.

**Who attends** was twelve chips &mdash; Entrepreneurs, Business owners,
Professionals, Manufacturers &mdash; naming audiences without saying why any of
them was there. It is now **"Who you'll meet"**: six roles, each with the reason
that role is in the room (Executives, seeking partners and vendors; Founders,
ready to raise or launch; Investors, looking for vetted opportunities; and so
on). A motive is what makes a room legible &mdash; it tells a reader who they
want to find, and whether anyone wants to find them.

**New section: "Eight reasons to attend"** (brochure page 3, "What's in it for
you"), between Who attends and Programme. Fresh perspectives, sector pavilions,
brand visibility, real conversations, hands-on workshops, connections that last,
CEO stories, networking bingo. Nav gains a "Why Attend" entry and every section
below it flips tint to keep the alternation.

One correction carried in: the brochure titles its seventh reason
**"Manufacturing"** but the body reads "Learn from CEOs as they share their
journeys and insights", which describes **CEO Stories**, the Saturday keynote.
The body is unambiguous and matches a real session, so it is titled CEO Stories
here. If a manufacturing reason was intended, the Manufacturing Opportunities
session is the one to point at.

### Speakers become cards, and the keynote is featured
The portrait strip was fourteen identical 88px discs with a name and a session
under each. It had nowhere to put a title &mdash; so Abidali Neemuchwala's
credentials appeared once, buried in an agenda card &mdash; and fourteen across six
columns ended 6/6/2 with the last row stranded.

Each speaker is now a **card**: avatar, name, title where there is one, session.
The **keynote takes the full first row** with a gold border, a "Keynote" badge and
a larger avatar; he is the headline booking and was previously indistinguishable
from the other thirteen.

**Avatar tints.** Three shades from one hue family, assigned in list order rather
than hashed from the name. Fourteen identical discs read as a placeholder grid,
and two pairs collide on their initials &mdash; Abidali Neemuchwala / Abdeali
Nagarwala are both "AN", Mufaddal Khambaty / Mustaali Kanch are both "MK" &mdash;
so without this they are literally the same circle. The assignment guarantees no
two people sharing initials share a tint. All three carry white text above 5:1
(#6B2F9E 8.1:1, #4A2470 12.4:1, #8B4BBF 5.2:1); keep any replacement above 4.5:1,
since the initials are the only content in the disc.

**Photographs are still missing &mdash; all fourteen.** Nothing matches
`img/speaker-<first>-<last>.jpg` yet, so every card shows initials. Dropping a
file in is the whole change; no code edit.

### The full agenda moves under the two day cards
The timetable now sits inside the **Programme** section, directly beneath the 01
Discover / 02 Grow cards and the line that introduces it &mdash; "Confirmed
sessions and speakers are listed below." That sentence pointed at content two
sections away; it now points at the thing immediately under it.

**Speakers** keeps the portrait lineup and the "Also expected to attend" notice,
and its intro no longer says sessions are listed below, because they are not &mdash;
they are above. It describes the people instead, and the eyebrow drops "&amp;
sessions" to match.

### The agenda gets a real heading
"Full agenda, both days" was a 0.74rem uppercase label sitting between the lineup
strip and the timetable, where it read as a caption on the portraits above rather
than a title for the grid below. It is now **Biz Connect Chicago 2026 Speaker
Agenda** &mdash; a serif `<h3>` at display size with a gold rule under it, which
also puts the timetable under the section `<h2>` in the document outline instead
of leaving it as an unlabelled grid.

### Saturday's keynote is named, and the open slots are shown
**Abidali Neemuchwala** &mdash; Co-Founder and Director at Dallas Venture Capital,
previously CEO and Managing Director of Wipro &mdash; is published as the speaker
for the Saturday 11am keynote, **CEO Stories**. Confirmed by Mansoor Anjarwala on
16 October. Speaker count in the hero goes 13 &rarr; 14, and he leads the lineup
strip. A photograph drops in at `img/speaker-abidali-neemuchwala.jpg` if one is
supplied; until then the avatar shows his initials like everyone else's.

**The Sunday 11am slot was never a session.** The schedule reads "Keynote Open"
&mdash; an open keynote slot with no session and no speaker. This page had been
showing a "Closing keynote" with a description of what it would cover; both were
invented here, not taken from the schedule, and are now gone. The card reads
"Keynote" and carries the "Speaker announced soon" pill, nothing more.

**Both days now run 9am&ndash;3pm, as the schedule does.** The five hours it marks
"Open slot &mdash; Program to be announced" (9am, 10am and 3pm Saturday; 9am, 12pm
and 3pm Sunday) are published as dashed, muted cards rather than left out. Leaving
them out made a half-built programme look finished, and the page claims
8:30am&ndash;3:30pm days while showing nothing before 11am.

Two small CSS additions: `.sess.open` for those cards, and a keynote-card override
so a named speaker on the violet gradient is legible &mdash; the `--ink-3` title
colour and the violet avatar disc both vanish against it.

**`exhibitors.html` does not have any of this.** It still has no speakers section
at all, so this is not a three-line fix there; the whole section needs porting
across.

### Countdown replaced by the at-a-glance stats
The hero's days/hours/minutes/seconds counter is gone, along with its script and
CSS. A ticking clock seven weeks out is motion without information. The four
stats &mdash; 2 days, 13 speakers, 6 sessions, $5 entry &mdash; now sit in its place,
and the separate band below the hero is removed so the figures appear once.

Two CSS notes for whoever edits this next:
- `.glance-grid li` needs `min-width:0`, or grid cells refuse to shrink below
  their content and the hero clips them.
- The `.hero-stats` media query must sit **after** the base `.glance-grid` rule.
  It was written before it, so it was dead &mdash; `auto-fit` happened to give the
  right answer, which hid the mistake.

Verified at a real 375px viewport: two columns, zero clipped cells, no document
overflow. Headless screenshots below ~500px are misleading here (see Working
notes in CLAUDE.md) &mdash; measure with a DOM probe instead.

### Keynote cards, and an at-a-glance band
The two keynote slots were dashed outlines reading "to be announced" &mdash; they
looked like holes. They are now the strongest cards in the agenda: dark violet
gradient, gold keynote label, and a gold "Speaker announced soon" pill. Saturday
carries its real session theme from the schedule, **CEO Stories**, which is in the
source and is not a person's name, so it publishes safely while the speaker is
still marked TBD.

A dark **at-a-glance band** sits under the hero: 2 days, 13 speakers, 6 sessions,
$5 entry. Every figure is drawn from what the page already states. It breaks up a
long run of text and puts the scale of the event above the fold-ish.

Contrast checked on the new dark cards: 15.93:1 heading, 8.96:1 gold label and
badge, 7.72:1 body. No horizontal overflow at 1280 or 375px.

### Speakers section leads with the people &mdash; and a contrast fix
A lineup strip now opens the section: all thirteen named speakers as 88px
portraits with their name and session beneath, before the timetable. The section
asks "Who you will hear from" and previously answered with a schedule whose
speakers were 34px discs at the bottom of each card.

**Accessibility fix.** `.sess-time` and the audience-card icons used
`--hero-gold` (#E3BE63) on white: **1.78:1**, well under the 4.5:1 AA needs.
Both now use `--gold` (#7E5D12), the token the palette already carries for light
surfaces and which `.place-kind` was already using &mdash; **6.07:1**. This was a
regression introduced with those two components; the rest of the site was
unaffected because gold elsewhere sits on the dark hero and band.

Checked at 1280, 768 and 375px: no horizontal overflow, and portraits drop to
68px below 520px.

### Preferred hotel gets a block of its own
The hotel moved out of the venue facts list into its own card below the venue
photographs: exterior photograph, address, the group-rate note, and two links
&mdash; Google Maps directions and the Marriott page. On both versions.

`img/hotel-delta-willowbrook.jpg` is the hotel's own marketing photograph,
supplied by Fatima. **Permission to use it has not been confirmed** &mdash; hotels
normally welcome this from a partner event, but a line to the hotel would settle
it. The `onerror` handler hides the photo panel if the file is ever removed.

### Audience-specific reasons to attend
Five cards under the Who Attends chips, one each for manufacturers, service
providers and professionals, startups, retailers and wholesalers, and anyone
trying to sell more. Each points at a **real session on the agenda** rather than
making a generic promise &mdash; the page previously listed twelve audience types
and offered all of them the same thing.

### One ticket, either day
The ticket card now says one ticket covers both days and you may come to either,
and a new FAQ answers it directly with what each day leans toward. Two full days
read as a large ask; this lowers it without inventing a single-day price.

### Sessions updated from the 15 Oct speaker agenda
**Kristin Richards removed.** She had been published as "Director, Illinois Dept.
of Commerce &amp; Economic Opportunity" on the Manufacturing panel; the updated
agenda replaces her with "Illinois Manufacturing Association (TBD)". The live site
was naming a state official for a session she is no longer listed for. That card
now reads "Speakers to be announced".

Newer titles and descriptions throughout &mdash; "Sell Differently: the mindset
shift that changes everything", "Biz Lifecycle: from start to finish", "Community
and Public Leadership", and the AI panel's revenue framing. Saba Haider's card
describes the session rather than her candidacy, which the updated draft dropped
too.

**Keynote slots shown as pending.** Both 11am slots now appear as dashed-outline
cards reading "Keynote &mdash; speaker and session to be announced", so the agenda
shows the event has keynotes without naming anyone. No name goes on the page until
acceptance is confirmed.

**Keynotes still not published.** The 11am Saturday slot is marked "Keynote
Speaker (TBD)" in the source, above Abidali Neemuchwala (Co-Founder and Director
at Dallas Venture Capital, previously CEO and MD of Wipro). The Sunday keynote is
"Open". The source document is footed "This is a draft schedule. Please do not
distribute." Nothing goes on the public page until someone confirms acceptance.

### Around Chicago moved below the FAQ
The tourism and city-restaurant content took a lot of room for a mostly local
audience, so it is now the last section. Nav order follows the page and the
background tints were re-flipped to keep alternating.

### Speakers & sessions section &mdash; attendee page
New `#speakers` section after the programme, listing the six confirmed sessions
across both days with named speakers. Answers the main criticism of the page:
it asked people to give up a weekend without naming a single speaker or session.

Speaker photographs drop in as `img/speaker-<first>-<last>.jpg` &mdash; slugged from
the name, so `img/speaker-saba-haider.jpg`. Until a file exists, the avatar shows
the person's initials on a violet disc and the `<img>` removes itself, so missing
photos look deliberate. No code change needed to add one.

**Deliberately NOT published**, from the source schedule:
- The three keynote names. The source row reads "List is TBD" above them, so they
  are candidates, not confirmations. Announcing a sitting CEO who has not agreed
  would be a serious error.
- The "TR Coordinator" / "Expo Coordinator" assignments and the MC list &mdash;
  internal organising data.

The five public officials under "Notable Attendees" **are** published, as "Also
expected to attend", on Fatima's instruction. Worth confirming their offices are
content to be named.

### Preferred hotel &mdash; both versions
The venue block's "Hotel details will be shared with registered attendees" row is
replaced with Delta Hotels by Marriott Chicago Willowbrook, 7800 S Kingery
Highway, with a Maps link. Address corroborated from two independent listings;
Marriott's own site blocks automated requests so the link could not be checked,
and a Maps search link is used instead. No rate or booking code is stated &mdash;
if the committee negotiated one, it should be added.

### Attendee version is now a TWO-day event - 5&ndash;6 December
The attendee page describes a two-day event. Friday 4 December ("Orientation")
was removed from the programme entirely, and the remaining days renumbered: day
one is Saturday 5 December ("Discover"), day two is Sunday 6 December ("Grow").

Everything downstream of that changed with it: the seven date strings across the
meta tags, hero and footer; the countdown target (now `2026-12-05T09:00:00-06:00`
&mdash; the 09:00 start time is an assumption, since only Friday had a stated
time); "three days"/"three-day" copy throughout, including the pass inclusion;
and the programme intro, which described three days each having their own job.

Dropping Friday also removed the Business Reception Darees, so that pass inclusion
was deleted &mdash; it promised something no longer on the schedule.

**`exhibitors.html` still says 4&ndash;6 December and three days.** The event
dates are a fact about the event, not a per-audience presentation choice, so if
the event really is two days that file is now wrong and needs the same treatment.

**`og.jpg` is stale.** The social preview card still has "4&ndash;6 December" and
the Hijri date rendered into the image. It needs regenerating from `og-card.html`
(command in README.md), which itself still carries the old dates.

### Hijri dates removed from the attendee version
All five references gone: the hero block, the footer line and the three programme
day labels. `exhibitors.html` keeps them.

### Ticket card widened and trimmed
The single Attendee card now spans 58rem with the two lists side by side, since
one card in a three-column grid looked stranded. "Why attend" cut from six bullets
to four. A "Buy now" button was added &mdash; **its `href` is a placeholder `#`**
and needs the real ticket purchase URL before this page goes anywhere public.

### Two versions of the site — IMPORTANT FOR DEPLOY
The site is now two files. `index.html` is the **attendee version** and is the
only one published to `bizconnectchicago.org`. `exhibitors.html` is the previous
full version, byte-identical at the point of the split, and is what the Chicago
Jamaat portal should deploy.

`_config.yml` excludes `exhibitors.html` from the published GitHub Pages site, so
it is present in the repository but not reachable on the public domain. The same
exclude list also stops the internal docs being served — `CLAUDE.md` and the rest
were previously readable at the public URL.

**Deploy note for the portal:** deploy `exhibitors.html` (rename it to
`index.html` at the web root, or serve it directly). Deploying `index.html` from
this repository to the portal would publish the attendee version.

**Keeping them in step:** roughly two-thirds of the two files is shared — venue,
dates, programme, Around Chicago, halal dining, FAQ. A correction to any of that
has to be made twice. `diff index.html exhibitors.html` shows what is
intentionally different.

**What differs in the attendee version:** the whole vision section is gone,
taking the Mawaaiz quote with it (a direct quotation could not be reworded without
misquoting). `Mumineen`, `Bohra`, `Dawoodi`, `Aqa Moula`, `Dua Mubarak` and `TUS`
no longer appear anywhere on the page. The "Why exhibit" card, the Exhibitor and
Sponsor passes, the sponsorship band, the exhibitor FAQ answers and the "How do I
register?" FAQ are all removed, as is the `#register` section — it embedded a
*Vendor Interest Form* for exhibitors, which was the wrong form for this audience.
The "Why attend" bullets are merged into the single Attendee card alongside the
pass inclusions, under **$5 presale, $10 at the door**. The nav item reads Tickets
and the FAQ heading reads "Good to know". The presenting organisations stay.

Layout follow-ons: containers that lost children were switched to a single column,
and section `alt` classes were re-flipped twice so the background tint keeps
alternating after sections were removed.

**Not resolved — the attendee page has no registration path.** Removing the
vendor form also removed all five calls to action, so the only button left is a
scroll link. An attendee registration form does not exist yet; until one does, the
page cannot be published as-is. The FAQ is down to two items: the
"How do I register?" and single-day answers were removed, both having referred to
a form that is no longer on the page. The Attendee card deliberately ends on the
pass inclusions with no button, since every available target is either the wrong
form or a mailbox that bounces.

### Embedded mode for the Jamaat portal — IMPORTANT FOR DEPLOY
The page now adapts when it is hosted inside another site.

**The host template needs no changes at all.** On load the page checks whether
anything renders above its own nav. If so it switches to embedded mode and
measures the host header itself, setting `--parent-nav-h` automatically. That
value offsets the sticky bar and every in-page anchor so headings never land
behind the combined header. Re-measured on resize.

To force it either way: `<html class="embedded">` turns it on regardless.

**In embedded mode:** the Biz Connect wordmark and theme toggle are hidden (the
portal owns brand and theme), the bar slims from 70px to 52px, and the hero
padding tightens. Standalone rendering is unchanged.

**Also:** nav `z-index` dropped 60 → 40 so the portal's nav always wins a
collision. Added a skip-to-content link, a `<main>` landmark and
`aria-label="Showcase sections"` on the nav — with two navs on the page, keyboard
and screen-reader users previously had no way past ~15 links or to tell the two
navigations apart.

### Halal dining near the venue
Split the halal list into two groups: six sit-down restaurants within about
5&ndash;22 minutes of Compass Arena (Willowbrook and Naperville), and the
existing city options below them. Each near-venue card carries cuisine, drive
time, street address and a Google Maps link for directions and phone.

All entries are sourced from Zabihah, the community-verified halal directory,
and none is listed there as serving alcohol. Card layout switched to CSS grid
rows so titles and links align across a row regardless of address length.

### Around Chicago section
New `#chicago` section between the venue and sponsorship band: six things to see
and do with official booking links, plus a halal dining list.

**Deploy note:** adds six more image slots in `img/` —
`chicago-artinstitute.jpg`, `chicago-skydeck.jpg`, `chicago-rivercruise.jpg`,
`chicago-millennium.jpg`, `chicago-msi.jpg`, `chicago-navypier.jpg`. All show
patterned placeholders until supplied. Filenames and licensing guidance are in
`img/README.md`.

**Also in this change:** the nav gained an item and started wrapping at ~1024px,
so nav elements are now `white-space: nowrap`, the duplicate "Register" text link
was removed (the button covers it), and the mobile breakpoint moved from 900px to
1040px.


---

## 2026-08-24

### Venue photo gallery — `49ce659`
Replaced the single decorative panel in the venue section with three photo
slots: a large one beside the venue facts, and two smaller ones below.

**Deploy note:** this adds a new **`img/` folder**. Make sure it is copied to
the web root or the slots will 404. The folder currently contains only
`README.md` — no photos yet.

Until a photo exists, each slot shows a patterned placeholder reading
"Photograph to come". Dropping a correctly named file into `img/` makes it
appear automatically — no code change:

| File | Slot | Guidance |
| --- | --- | --- |
| `venue-exterior.jpg` | Large panel | Landscape 4:3, 1600px+ |
| `venue-floor.jpg` | Lower left | Landscape 3:2, 1200px+ |
| `venue-dining.jpg` | Lower right | Landscape 3:2, 1200px+ |

### Light theme by default, opt-in dark switch — `e8959e0`
Removed the `prefers-color-scheme` media query so the site no longer follows the
visitor's OS theme. Light is now always the default. Added a moon/sun button in
the nav that switches to dark and remembers the choice in `localStorage` under
the key `bcs-theme`.

**Deploy note:** a small inline script now runs in the document head *before*
the stylesheet, to stamp the theme before first paint. If your pipeline moves,
defers or minifies scripts, keep that one inline and in place — moving it causes
a white flash for anyone who has chosen dark.

### WhatsApp / social preview card — `04d4926`
Added `og.jpg` (1200×630, 133 KB) and the full set of `og:image` tags so links
preview properly when shared.

**Deploy note:** `og.jpg` must be served from the web root. The card is
regenerated from `og-card.html` — the command is in `README.md`.

**Action needed on domain change:** three tags hardcode the current host —
`og:url`, `og:image` and `og:image:secure_url`. When the site moves to its real
domain these must be updated or link previews will keep pointing at the old
address.

### Favicon, description and Open Graph tags — `6c9e371`
Added an inline SVG favicon (data URI, no file), a meta description, and
Open Graph / Twitter card tags.

### Initial site — `6b815ea`
First build. Sections: hero with countdown, vision, who attends, why attend /
why exhibit, three-day programme, passes, embedded registration form, venue,
sponsorship, FAQ, footer.

**Deploy notes:**
- The registration section embeds the JotForm at
  `https://form.jotform.com/261984324758066` in an iframe. The host must allow
  outbound framing of `form.jotform.com`; JotForm sends no `X-Frame-Options` or
  `frame-ancestors`, so it embeds fine.
- Fonts load from Google Fonts (`fonts.googleapis.com`, `fonts.gstatic.com`).
  Everything else is self-contained.
- The countdown targets `2026-12-04T09:00:00-06:00`, hardcoded in the script.

---

## Known placeholders

These are wrong on the page today and will change:

- **Contact email** — `info@bizconnectchicago.com` is a placeholder. The domain
  is unregistered, so mail bounces.
- **Pricing** — attendee and exhibitor cards both read "Rates announced soon".
- **Sponsorship tiers** — "Tiers on request".
- **Venue photos** — all three slots empty.
- **Logos** — the site has no organisation logos. The nav mark is a generic
  eight-point star drawn in SVG.
