# Shiny Rock Games website

Static site for Shiny Rock Games, hosted on GitHub Pages. Plain HTML and CSS, no build step, no framework, no JavaScript needed so far. Keep it that way unless there's a real reason.

Nieve reviews and commits everything in GitHub Desktop. **Do not commit or push.** Make the edits, then summarise what changed so she can review the diff.

## Files

- `index.html`: home page (hero, our games, "What does this mean?" series teaser, about, Discord band)
- `scrunge.html`: Scrunge game page (hero + trailer, how it plays, pogs, tiddlywinks glossary, demo CTA)
- `style.css`: all shared styles; design tokens are CSS variables at the top
- `images/logo.png`: gnome sticker logo with transparent background (also used as favicon and og:image for now)
- `videos/scrunge-demo-announcement.mp4`: 9s "Demo coming soon" teaser (1080p, no audio), shown in the Scrunge hero
- `images/scrunge-trailer-poster.jpg`: last frame of the teaser, used as the video poster
- `images/scrunge-screenshot.webp`, `images/creature-castle-screenshot.webp`: 1200x675 game card images on the home page
- `images/scrunge-share.jpg`: 1200x630 share image for `scrunge.html` (`og:image`)
- `videos/scrunge-flick.mp4`, `videos/scrunge-smash.mp4`, `videos/scrunge-pot.mp4` (+ `.jpg` posters): silent looping "How it plays" clips, cut from the B-roll at 960px wide. Use looping MP4s like these rather than real GIFs (far smaller and sharper)
- `app-ads.txt`: AdMob verification for Creature Castle. **Must stay at the site root. Never delete or edit it.**

Preview by opening `index.html` in a browser. Check at phone width too.

## Brand

Taken from the official banners (X/Bluesky header, Discord banner, Story cover).

- **Colours:** dark ink background `#131217` with sunburst rays `#1B1A20`, true panel black `#0B0B0C`, cream text `#F0ECE2`. The four brand colours always appear in this order: green `#2BD67E`, purple `#8A4FD8`, coral `#FF6B57`, amber `#E8A84B`.
- **Type:** Archivo Black, uppercase, with a hard black offset shadow for big headings. Space Mono, uppercase and widely letter-spaced, for the tagline and small labels. DM Sans for body text.
- **Motifs:** sunburst background, outlined gem shards scattered around, the four-colour bar under big headings, a black box holding mono text (e.g. "SMALL GAMES, BIG SHINE"), the gnome sticker with its cream border.
- **Tagline:** "Small games, big shine".
- **Buttons** press down into their black shadow on hover. They never fade.

## Design rules: avoid looking "vibecoded"

Do not introduce any of these:

1. Purple-to-blue gradients
2. Gradient hero text
3. Emoji in headings (or anywhere in the UI)
4. Inter font
5. Coloured border cards
6. Glassmorphism cards
7. Low-contrast dark mode (keep text at 4.5:1 or better)
8. 3 icon boxes in a row
9. Badges or eyebrow labels above headlines (labels go *below* the heading, like the tagline under the colour bar)
10. Lucide icons
11. Untouched shadcn UI
12. Fade-in on scroll
13. Cursor-following effects
14. Buttons that fade on hover
15. Inconsistent spacing (use `--section-y` and the existing gap scale: 12 / 16 / 20 / 40 / 56 / 72px)
16. Em dashes. **Never use em dashes**, in copy or comments.
17. Generic buzzword copy ("reimagined", "next-level", "seamless", "unleash" etc.)
18. Serif italic accents
19. Space Grotesk or Instrument Serif
20. Grain over a gradient

The sunburst and gem shards are part of the brand, not decoration to remove.

## Writing

UK English. Plain, warm, a bit daft, specific to tiddlywinks. Short sentences. Write "wink" in lowercase, never "Wink". Real tiddlywinks terms are welcome (squidger, pot out), but Scrunge is single-player: no squopping, opponents or "your mates". Don't invent facts about the game or the team: leave a bracketed placeholder instead.

## Content status

- **Scrunge:** "a chaotic tiddlywinks roguelike" (that's the pitch; use it consistently). Single-player: flick, smash, stack up perks, pot it before your rack runs out, beat each level's target score. In development, demo coming soon on itch.io. Perks are presented as pogs (90s milkcap style, risograph look, deliberately scrappy). The mascot Mr Scrunge appears only occasionally.
- **Creature Castle:** spooky match-3 game, out now on Google Play (Android): https://play.google.com/store/apps/details?id=com.shinyrockgames.monstercastle
- **Support email:** shinyrockgames@gmail.com (shown in full in the footer, not hidden behind a "Contact" link, because mailto does nothing for people with no email app set up; Google Play needs a support contact, so keep it).
- **"What does this mean?"** video series: lives on TikTok, so its sections link there (plus Discord). Not ready yet, shown as "coming soon" everywhere. Don't add episode cards until there are real episodes. Episode one is about the word "scrunge" itself (a wink that bounces back out of the pot). It's the first card in the "Learn the lingo" glossary on `scrunge.html`.
- **Discord:** https://discord.gg/f2EysadzFF (real, working link). It's the main way to follow the studio: there is no mailing list, so don't add an email sign-up.
- **TikTok:** https://www.tiktok.com/@shiny.rock.games (real; use this clean URL, not the share link with tracking parameters).
- **No other socials yet.** Instagram and Threads are being set up. There is no X, Bluesky, itch.io page or press kit, so don't link to them.

## TODO

Search the files for `TODO` and `[` placeholders. Outstanding:

- [ ] itch.io page: when it exists, switch the two "Follow on TikTok" buttons on `scrunge.html` back to itch.io and add it to the footer
- [ ] Instagram and Threads: add to both footers once the accounts exist
- [ ] Press kit: none yet; add a footer link if one is made
- [ ] Gameplay trailer: the hero currently shows the demo announcement teaser; swap it when real gameplay footage exists
- [ ] Pog artwork: the four pogs on `scrunge.html` show Wide Pot, Hot Hands, Last Chance and Encore as text on the face until art exists
- [ ] A proper share image (1200x630) for `index.html` (`scrunge.html` already has one)
- [ ] Before launch: hide or remove any section still full of placeholders rather than shipping it half-finished
