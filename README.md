# Getting Started with Tailwind

- Download (or clone) this repository and unzip it.
- Open the folder in VS Code.
  - You should see this is exactly the same as the example we looked at in the last session.
- Open index.html in a web browser
  - At the moment it has no styling, we are going to style this page using Tailwind

# Installing Nodejs

# Installing Tailwind

- Using the shell/terminal navigate to the intro-to-tailwind directory.

- To make sure you are in the right place enter the followinf

```
dir
```

- You should see the index.html file listed along with the js and css folder.
- Next install tailwind

```
npm install -D tailwindcss
```

- Initialise tailwind

```
npx tailwindcss init
```

- This will create a tailwind.config.js file.
- Open this file
- Modify it so it points to 'index.html'

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./index.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

- Under content we are specfying which files tailwind should look at for references to its CSS rules.

- Add tailwind directives to css/input.css
  - This simple loads some basic CSS rules that tailwind uses.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

In your terminal/shell enter

```
npx tailwindcss -i ./css/input.css -o ./css/style.css --watch
```

- Open in a browser, you should find that tailwind has applied its default base styles to your web page.

## Using Tailwind

- To use tailwind, we don't write our own CSS instead we simply use classes from the tailwind framework.
- In index.html add a class attribute to the body tag i.e.

```
<body class="text-sky-950 text-lg">
```

- Note the terminal gives you some feedback that the CSS has been rebuilt.
- Reload the page see the change.
  To understand what these classes are doing see:

  - colours - https://tailwindcss.com/docs/customizing-colors
  - changing the text colour https://tailwindcss.com/docs/text-color#basic-usage
  - changing the font-size https://tailwindcss.com/docs/font-size#basic-usage

- Open style.css, find the `text-sky-950` class (do a ctrl+f).
  - See how Tailwind has generated the CSS rule.

## Styling the Navigation Bar

Previously we styled the navigation bar using the following CSS

```css
/* CSS rules for the header*/
.header {
  background-color: rgb(8, 47, 73);
  color: white;
}
.header-wrapper {
  display: flex;
  justify-content: space-between;
  padding: 0.75em;
}
.nav-list {
  margin: 0;
}
.nav-opt {
  border-top: 1px solid white;
}
.nav-link {
  color: white;
  display: block;
}
.nav-link:hover {
  background-color: rgba(255, 255, 255, 0.25);
}
.menu-icon {
  cursor: pointer;
}
```

- Try and re-create this using Tailwind. For most properties you should be able to
  search on the Tailwind website to find the equivalent Tailwind class and then add these classes in _index.html_.

For example we need to set a background colour and text colour for the `header` element. So we'd add a class attribute to the header tag and use the `bg-sky-950` and `text-white` classes.

```html
<header class="bg-sky-950 text-white"></header>
```

- You don't need to make any changes to the CSS files! You only need to edit _index.html_

- If you get stuck here's a final working version:

```

```

- There are already `onclick` event handlers for the menu icons.

the navigation will work, we had to change the class name in the js to use the tailwind classname

## Styling the Main Content of the Page

again, here is the css we applied previously

try and find the equivalent tailwind css classes and apply them

your design won't be an exact match e.g. the headings, try and find additional tailwind properties to get the headings looking correct.

## Making This Responsive

media queries are done with a modifier

demo the header example

### Adding a Two Columned Layout

- Here's the css fro making a two columned layout at 640px

```css
.main-content {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.content-list-holder {
  width: 50%;
}
.content-list {
  margin: 0.25em;
}
.poster {
  float: right;
}
```

have a go at doing this yourself

### Limiting the Final Page Size

do this yourself

## Testing Your Understanding

like the example earlier this week, the design will need tweaking
