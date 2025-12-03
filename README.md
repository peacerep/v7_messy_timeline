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

3. Deploy
```bash
git add .
git commit -m "message"
git push
```