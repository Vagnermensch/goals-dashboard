# 2026 Goals — personal dashboard

A single HTML file to track your goals and weekly wins, and to share a clean
progress report (or PDF) with your manager. Everything is saved **in your own
browser** — no account, no server, nothing leaves your machine.

**▶️ Live demo:** https://vagnermensch.github.io/goals-dashboard/

## Get your own copy

- **Download:** click **Code → Download ZIP**, or just save
  [`index.html`](index.html).
- **Or fork** this repo and enable Pages to host your own live version.

## Use it in 3 steps

1. **Open `index.html`** in your browser (double-click it). It works straight
   away with example goals.

2. **Make it yours.** Open the file in any text editor (VS Code, Notepad,
   TextEdit…) and edit the `CONFIG` block near the top — it's the first thing
   inside `<script>`:

   ```js
   const CONFIG = {
     owner: 'Your Name',      // shown in the header and the shared report
     year: '2026',
     password: '',            // leave '' for none, or set a word to lock the page
     goals: [
       {
         tag: 'Growth',                        // small label
         title: 'Skills & Learning',           // objective name
         statement: 'One line describing it.',
         topics: [                             // the things you check off
           'First key result',
           'Second key result',
         ],
       },
       // add as many objectives as you like…
     ],
   };
   ```

   Save the file and refresh the page.

3. **Use it.**
   - **Objectives** tab → click a card to open it. Check topics off, drag the
     slider to set progress manually, and add **Updates** and **Next steps**.
   - **Weekly Wins** tab → log wins and browse previous weeks.
   - **Share update** (top right) → choose *Goals progress* or *Weekly wins*,
     then **Copy as text** or **Print / PDF** to send to your manager. In the
     print dialog keep **“Background graphics”** on for the styled version.

## Good to know

- **Where's my data?** In this browser only (localStorage). Using the same file
  on another computer starts fresh. Clearing browser data erases it.
- **Password:** setting `CONFIG.password` is light privacy for a shared file —
  it's not real security (the file is readable). Leave it `''` for no lock.
- **Fonts:** the display font loads from the internet; offline it falls back to
  a system font — everything still works.

## License

MIT — see [LICENSE](LICENSE).
