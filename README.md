# caffeinate — the pet

A terminal Tamagotchi that runs on real wall-clock time. It drains whether or not the tab is open, and it holds a grudge. Keep it awake by typing `caffeinate`. Leave it too long and it crashes. Abuse it and it does worse.

One self-contained HTML file. No build step, no dependencies.

Access it here: https://j0jk.github.io/caffeinate-pet/

## Play

Type commands into the prompt. The one that matters is `caffeinate`. You find the rest by poking.

- The mug drains about 4% a minute in real time and remembers across sessions. Close the tab, come back an hour later, and it will have crashed and tell you how long it was out.
- The face changes with the level. Steam and wide eyes when wired, drooping when it runs low, tipped over with floating z's when it crashes.
- The first two minutes drain at half rate. It never says so. Early play stays survivable, then it gets needier as you get attached.
- There are 27 discoveries. The counter sits in the stats row (`◆ N/27`). Click it or type `discoveries` for the gallery. Found ones show their flavor. Locked ones stay redacted with a hint.
- `reveal` opens the whole gallery, no penalty. Good for a quick demo.
- `man` lists the basics. It does not list everything.

A few things worth knowing and not worth spoiling: coffee is not the only drink, past full is not better, and the one death caffeine can't fix has another way back.

## Themes

Type `theme` to cycle the terminal color, or `theme <name>` to pick one. Four to choose from: amber, green, ice, plasma. Your choice sticks across sessions.

## Mobile

It works on a phone. Tap the screen to raise the keyboard, then type. Typing commands on a phone keyboard is the only real friction. Everything renders and persists the same.

## Notes

Scores and timings are illustrative and self-contained. Apart from optional logging, everything lives in the visitor's browser. Respects reduced-motion.


## Forking

Fork it, deploy your own, rename the pet, repaint it, do whatever.

One thing to know: the committed `index.html` logs anonymous input to the original author's database, so a fresh fork would send its visitors' typing there. To turn that off, open the script near the top and set `SUPA_KEY` to an empty string (`""`). The pet plays exactly the same with logging off. To point it at your own instead, set `SUPA_URL` and `SUPA_KEY` to your own Supabase project's URL and publishable key.

### Deploy to GitHub Pages

The file is static, so hosting is a copy and a push.

1. Create an empty repo on github.com. Don't initialize it with a README or license.
2. From the folder holding your files:

   ```bash
   git init
   git add index.html README.md
   git commit -m "caffeinate: the pet"
   git branch -M main
   git remote add origin https://github.com/YOUR-USER/YOUR-REPO.git
   git push -u origin main
   ```

4. Repo → Settings → Pages. Set Source to the `main` branch, root folder. Save.
5. Give it a minute. It's live at `https://YOUR-USER.github.io/YOUR-REPO/`.

Persistence uses the browser, so the wall-clock state works on Pages with no changes.


## License

MIT. See [LICENSE](LICENSE). Use it, change it, ship it.
