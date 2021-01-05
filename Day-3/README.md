# Week-13 -- Day-3

## Getting Started with the Restaurant Page


 The Odin project has an assignment to test your newly acquired module knowledge. Feel free to change it from a restaurant to whatever you want! I mean that. It is important to practice your creativity along with your logic skills.

Whatever you choose here is how you can get started:

run `npm init -y`
run `npm install webpack webpack-cli --save-dev`
run `touch .gitignore` and add the following line to the newly created file
> node_module

run `npm install`
Create `src` and `dist` directories
Create an `index.js` in `src` directory. Feel free to use the touch command again.
Create an `index.html` in `dist` directory
Open up index.html in your editor and link a javascript file called main.js. Here is an example:

    <!DOCTYPE html>
    <html lang="en" dir="ltr">
      <head>
        <meta charset="utf-8">
        <title></title>
      </head>
      <body>
        <script src="main.js" charset="utf-8"></script>
      </body>
    </html>
Create a `webpack.config.js` file with the following content:

```javascript
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```
Let's test it out. Add a console log statement or alert statement inside src/index.js
run `npx webpack --watch` in the root directory
Open up index.html in a browser and see if your console log or alert statement showed up without error messages.

Here is full Odin instruction page:

https://www.theodinproject.com/courses/javascript/lessons/restaurant-page

Feel free to also use the official webpack getting started page:

https://webpack.js.org/guides/getting-started/
