# ⭐ Daily Features – Your Daily Recipe Inspiration

> Every time you open Cookwise Pro, five random recipes are highlighted at the top of the screen.

This section is designed for you, the cook, to jump straight into something new without digging through filters or collections.

---

## 🧠 Why it’s useful

- **Fresh ideas instantly.** If you’re not sure what to cook, the Daily Features section gives you five possibilities with one glance.
- **No setup required.** You don’t have to tweak filters or enter keywords – the app does the work for you.
- **Keeps things interesting.** The set stays the same while you’re using the app, so you can open recipes and come back without surprises; close and reopen for a new selection.
- **Complemented by Random Recipe.** Once you’ve explored the five featured items, hit the Random Recipe shortcut (Ctrl/Cmd + R) for a one‑off surprise drawn from your entire library.

## 🚀 How to use it

1. Launch Cookwise Pro (or refresh the page).
2. Look at the horizontal row labelled **Daily Features** (with a calendar icon :fa-calendar-day:).
3. Click any recipe card to open it and start cooking. The other cards remain until you close the app.
4. When you reopen tomorrow, the row will show five new recipes.

> Tip: you can still use search, filters and collections below the Daily Features section – it won’t interfere with them.

## 🛠 Technical details (for power users)

- The app chooses recipes on first load only. A `useRef` flag prevents the list from recalculating during your session.
- Recipes with certain courses (e.g. marinades, seasonings, condiments) are excluded so you get full meals.
- The feature is implemented in `App` and stored in state as `dailyFeatures`.
- Styling uses a scrollable flex row so the cards fit on desktop and mobile.

## 📌 Notes

- Since this is a user‑centric feature, you cannot edit or disable it – it’s always there to spark ideas.
- If you add or remove recipes from your library and refresh, the next set may include the updated list.
- Treat it like a mini “recipe of the day” board – perfect for morning browsing with coffee.
- Don’t forget the **Random Recipe** command (Ctrl/Cmd + R) if you want a spontaneous single suggestion outside of the daily set.
  Happy cooking! 🧑‍🍳
