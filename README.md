# Bar Ready

A study game for Starbucks drinks: standard recipes plus the shots, pumps and scoops for every size. It is a single `index.html` with no build step. It is an unofficial study aid, not a Starbucks product.

## How it plays

- **Map**: a training path of 9 levels, from Latte & Cappuccino to the Rush Hour Boss. Each level is a shift of 6 orders and earns 1 to 3 stars.
- **Bar Shift**: a ticket prints, a customer waits, and you build the drink at the stations. Espresso drinks use Espresso, Milk, Syrup and Toppings. Frappuccinos use Milk, Sauce, Blender and Toppings. The glass fills as you go. A wrong drink comes back as a REMAKE. The yellow button shows the recipe card.
- **Tickets**: `✓ STANDARD RECIPE` means make the drink exactly as the recipe says. A yellow `CUSTOMER ADDS` line means the customer asked for something extra (for example a syrup): add it using the bar-card pumps. Lattes, Cappuccinos, Flat Whites, Americanos, Misto, Cold Brew, Iced Tea and Refreshers have no syrup in their standard recipe.
- **Learn with help**: every level and every recipe can be played with help first. The right buttons glow and each counter shows its goal. Help runs earn no level stars and don't count as mistakes.
- **Recipes**: every drink laid out like the Starbucks app, with only the standard recipe (no customer changes). "Quiz me" hides the answers.
- **Rush**: 60 seconds of quick questions, plus "Fix my mistakes".
- **Cards**: the bar cards, the recipe tables and memory tricks.

Anything you miss comes back more often. Progress is saved only in that browser.

## Use it on an iPad or phone

Open the site in Safari, tap **Share → Add to Home Screen**. It opens full screen like an app. The layout adapts to phones, iPad portrait (one large column) and iPad landscape (scene on the left, stations on the right).

## Publish with GitHub Pages

In the repository: **Settings → Pages → Deploy from a branch → `main` / `(root)` → Save**. After a minute the game is live at `https://<user>.github.io/<repo>/`.

## Files

- `index.html`: the whole game.
- `logo.svg`, `icon-*.png`, `manifest.webmanifest`: logo, home-screen icons and app settings.

## Where the data lives

In the `<script>` of `index.html`:

- `TAB`: counts from the bar cards (card row → hot/iced → size).
- `REC`: standard recipes from the Starbucks app. Espresso drinks: roast, shot type, milk, steamed or cold, foam, whipped cream, syrup. Frappuccinos: milk, sauce, whipped cream, drizzle, topping. Pumps and scoops per size come from `TAB`.
- `D`: every drink and which `TAB` rows it uses.
- `LEVELS`: the map.
- `TEST_DAY`: the test date.

Known gap: Frappuccino Chips are only known for the Grande (3 scoops), so the Mocha Cookie Crumble is Grande only. Add the Tall and Venti values to `CHIPG` in `TAB` and remove `sizes:['G']` from that drink in `D`.
