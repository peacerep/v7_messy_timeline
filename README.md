# Messy Timeline

## Update

1. Replace 1 csv file inside data with updates:  
   `pax_all_agreements_v[new_version].csv`

2. Update file names in `index.html` on line 126:
```js
Promise.all([
    d3.csv("data/pax_all_agreements_v[new_version].csv"),
]).then(d => init(d))
```

3. Run the vis locally to check if ok before pushing changes:
`python -m http.server`

Then open in browser: http://localhost:8000

(or open the html file locally)


4. If happy, deploy using:
```bash
git add .
git commit -m "message"
git push
```

This should auto update both:
https://peacerep.github.io/v7_messy_timeline/ 
https://pax-messy-timeline.onrender.com [the link on the pax website]


## Important reminders for when updating

- Update the **info panel text** to reflect the latest date range and data version (e.g. "version 10")
- Check that the **timeline date range** reflects the latest data (change the year end). Ideal line may need adjusted once more years added.

## Updates with v10 data (NH)
1. added hyperlinks to agreements on PA-X on click
2. adjusted ideal line to plateau 
3. improved tooltip positioning as some were getting cut off
4. changed x axis scale to fit the new years better - comments in code
5. changed how links are styled
6. added Tom and Tobias website for credits

## Further updates:
1. Implementing zoom of x axis
2. Zoom control buttons
3. Wrap long titles
4. Container for top bar added so no overlap

