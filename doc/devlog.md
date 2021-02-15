## Initial evaluation

**Received problem at 4PM 02/12/2021**

Reading the PDF reveals some information:

* I am to design a dashboard
* User Story: "As an executive, I want to understand how salespeople are performing at a glance"
* There is a "starter" HTML file
  * I may modify the HTML file (assumption: only the single file?)
  * No CSS or JS frameworks (Is jquery or lodash a framework?  assume yes)
  * Also, above implies `<script>` tags for CSS, etc.
* Estimated time is 3-4 hrs, but I can spend as long as I want (extra credit?)
* Modified HTML is to be returned by 3PM Mon (3PM per I-Shien's email)

HTML has:
* sections
  * leaderboard
  * sales employee list (table)
  * overview
* problems
  * no `title`
  * no `alt` text for images
  * overview `div` is in the middle of employee `table`

## Returned questions to InfoTech

_Unfortunately, this went out at 4:30.  Did not get a response, and Monday I have to work, so that will be late to react to new input.  "The Customer Is Always Right" so not waiting for response and will proceed based on assumptions documented amongst questions.  If they want to give me till Tuesday, I can address feedback Monday night_

1. Based on the instructions, I should return a single, static HTML page, is this correct?
   * If that is correct, then I assume CSS and Javascript in `<script>` tags is OK.
   * I also assume that it is fine to have embedded mock data and the only api I should use is the randomuser.me assets that are already there.
1. Is the evaluator interested in any ancillary materials (README, plan, tests, etc.), or am I limited to only the single file?
1. Are the metrics in the existing HTML in the order of importance for the user from top to bottom?
1. Are there specific browsers that I should target?
1. Are there specific mobile browsers that I should target?
1. Do you want it to be responsive to multiple device sizes?  If so, are there any specific sizes?
1. Will this be tested on a screen reader? Are there any specific accessibility criteria I should target?
1. Are there any branding assets (colors, typefaces, images) that I should be using?
1. Are there performance metrics other than what are in the existing HTML that are of interest?

## Detailed evaluation of HTML

* There is a "leaderboard"
  * Select/Option with three time ranges (not hooked up)
  * Three employee images (assuming first, second, third and not one for each option in the select - ask?)
* There is an employee listing
  * Name, Headshot, closed deals
  * Two links: view profile, and "message"
* There is a "sidebar" div
  * float right
  * Overview with closed deals and cumulative value (since when?)
  * "Feed" (ticker?) with I assume the latest sales info
* PROBLEMS
  * `div` inside `table` but outside `td`
  * No HTML5 `table` markup
  * Repetitive inline styles
  * No `alt` text for `img` tags
  * No title



