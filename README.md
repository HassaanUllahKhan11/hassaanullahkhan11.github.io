# Hassaan Ullah Khan: portfolio

A one-page static site: selected work, services, process, about and contact. No build step; open `index.html` or serve the folder.

```bash
python -m http.server 5050
```

## After deploying the demos

Edit the `LINKS` object at the bottom of `index.html`. Each "Try the live demo" or "Book a call" button appears only once its URL is set:

```js
var LINKS = {
  assistant: "https://your-assistant.vercel.app/demo/sunmarke-school",
  dashboard: "https://your-dashboard.vercel.app",
  booking: "https://cal.com/your-name/15min"
};
```

## Files

- `index.html`: the page
- `style.css`: design tokens (light and dark) and layout
- `img/`: WebP screenshots of the two demos, light and dark variants
