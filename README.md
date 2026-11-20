# Who has to pay to close the gap?

An interactive tax simulator. Students set a yearly wealth tax on billionaires and the wealthiest households, and raise or cut the federal tax rate for six income groups, then watch how much of the $2.0 trillion federal deficit their plan closes and who ends up paying for it. It shows why plans that focus only on billionaires fall short, and where the rest of the money would have to come from. By Gwen Sharp.

**Live site:** https://gsharpokie.github.io/taxgap/

## What it does

- **A meter at the top** stays on screen and shows how much the plan raises, how much of the goal is left, and which groups the money comes from.
- **Your goal:** close the 2026 deficit, cut it in half, or leave it as is. Students can also add a new program or tax cut, either from a menu of common proposals with sourced cost estimates or by typing their own cost. The cost is added on top of the deficit goal.
- **Wealth tax sliders** for billionaires and the rest of the wealthiest 0.1% of households, with an avoidance setting (none, 15%, 45%, or 70%) based on published estimates of Senator Elizabeth Warren’s wealth tax.
- **Income tax sliders** for six groups, from the top 0.1% to the bottom half. Each shows the group’s current average federal tax rate and what the change would cost each family.
- **Starting plans:** “Billionaires only,” “Top 1% only,” and “Broad base.”
- **Who pays in your plan,** a summary of each group’s share, and a button that copies the plan as text.
- **Discussion questions** and a section on how the tool works and its limits.

Nothing a student enters is saved or sent anywhere.

## For instructors

- The math is simple on purpose: revenue equals a group’s income or wealth times the rate students set. Treat every number as a rough illustration, not a forecast.
- Students can paste their plan into an assignment with the **Copy my plan as text** button.
- It works well in pairs or small groups: have each group find a plan that closes the gap, then compare who pays.

## Updating the numbers

Open `index.html` on GitHub, select the pencil icon, and look in the `<script>` section:

- `var DEFICIT = 2000;` and the goal buttons near the top of the page hold the deficit, in billions.
- `var WEALTH = [` holds the two wealth groups: `base` is total wealth in billions and `n` is the number of people or households.
- `var INCOME = [` holds the six income groups: `base` is total income in billions, `n` is the number of families, and `cur` is the current average federal tax rate.
- `var PROGRAMS = [` holds the proposal menu. Each entry has a name, a yearly `cost` in billions, a `note`, and a source link.

If you change a figure, also update the matching note in “How this tool works and its limits.”

## Turning on the site (one time)

Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, and select **Save**. Keep Issues turned on so the accessibility link below works.

## Sources

Congressional Budget Office. 2026. *Monthly Budget Review: Summary for Fiscal Year 2026*. U.S. Department of the Treasury, Office of Tax Analysis. 2024. *Distribution Table 2025-001*. Board of Governors of the Federal Reserve System. 2026. *Distributional Financial Accounts*. Saez, Emmanuel, and Gabriel Zucman. 2019. “Progressive Wealth Taxation.” *Brookings Papers on Economic Activity*, Fall: 437–511. Penn Wharton Budget Model. 2019. “Senator Elizabeth Warren’s Wealth Tax: Budgetary and Economic Effects.” Zidar, Owen, and Eric Zwick. 2026. *The Everywhere Millionaire*. Henry Holt. Sources for the proposal costs are linked on the page.

## Accessibility

This site aims to meet [WCAG 2.1](https://www.w3.org/TR/WCAG21/) Level AA, so it works for people who use screen readers, keyboards, or screen magnification.

- All buttons, sliders, menus, and links can be reached and used with a keyboard, and show a visible outline when selected.
- Every slider has a label, and its current setting and the money it raises are shown as text.
- The colored bar at the top has a text equivalent: the amount raised and the share of the goal are shown above it, and each group’s amount is shown beside its slider. Groups left out of a starting plan are labeled “Not in this plan,” not marked by color alone.
- Text meets WCAG AA color contrast standards in both light and dark mode.
- Pages fit narrow phone screens without sideways scrolling.

I checked it in November 2026 with automated accessibility testing (axe-core) plus keyboard and small-screen checks. It hasn’t yet been tested by people who use screen readers every day, so there may be problems I haven’t caught. If something doesn’t work for you, please [let me know](https://github.com/gsharpokie/taxgap/issues/new).

## Author

Created by Gwen Sharp ([@gsharpokie](https://x.com/gsharpokie)).

## License

© 2026 Gwen Sharp. Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): you may share and adapt it for noncommercial purposes with credit. See [LICENSE](LICENSE).
