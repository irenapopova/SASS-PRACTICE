#### SASS INTRODUCTION notes

#### repo consists my notes and my sass/scss exercises
#### What is sass/ scss?

SASS stands for syntactically awesome stylesheets and does not run in the browser.

Instead it extends CSS during development only. 

#### SASS FEATURES

##### NESTED RULES
##### HELPER FUNCTIONS
##### INHERITANCE
##### MIXINS
##### PARTIALS
##### CONDITIONAL LOOPS
##### VARIABLES


what can be done in general with SASS is to nest CSS rules to shorten the code.
With use of helper functions certain things can be achieved like making a color a bit more brighter,
With mixins I can create reusable snippets of code.
The code can be easily split into multiple files with PARTIALS. 
Variables can be defined if a certain hex code of color gets used a couple of times on the page, instead of writing that hex code every time and changing it whenever change the color , I can simply store it in a variable. 
CONDITIONS  and LOOPS can also be used.

#### installing sass
In order to compile SASS it should be installed. 
SASS is a Ruby gem, a tool build with Ruby and therefore it requires the Ruby runtime to work.

BUT 

I can use node scripts 

#### Npm Scripts
Npm has a run command that can run scripts defined in the scripts property of a package.json file. If you’ve ever used a package that asked you to run a command like npm run test (or similar) then you have used npm scripts.

To use npm scripts as a build tool define a bunch of scripts in a package.json file, similar to defining the tasks i want to run in a config file in other build tools. The difference with npm scripts is that it is going to run the package CLI without any plugins, then chain the scripts together so to trigger a build with a single command. 

##### Compile Sass to CSS
##### Concatenate and minify CSS and JavaScript
##### Optimize images

 to compile our Sass file to CSS using the node-sass package. First we need to install it:
 #### npm install node-sass --save-dev

Note that the * --save-dev*  saves this package in the devDependencies section of the package.json file. This makes it easy for other developers to install the required packages in the future by simply running npm install.

#### Lifecycle Scripts
Node also allows you to run custom scripts for certain lifecycle events, like after npm install is run. 
```js
"scripts": {
    "postinstall": "electron-rebuild",
},
```




