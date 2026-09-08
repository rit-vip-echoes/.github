# **echoes Web Development Standards**

## JS & HTML

Ensure all JavaScript and HTML is structured semantically, i.e., with respect to meaning, named clearly, and commented effectively.

### JS

  -  Group related variables and code-blocks close together to keep context consistent for future readers (which could include yourself).
  -  Keep your variable and function names clear and concise. The clearer these are, the less commenting you’ll likely need to do.
  -  Comment large blocks of code and complex lines to communicate their functions.

### HTML

  -  Use the appropriate semantic elements where applicable ([Resource](https://www.w3schools.com/html/html5_semantic_elements.asp)) ([Resource](https://www.freecodecamp.org/news/html-best-practices/)). This improves accessibility for those using screen readers.
  -  Comment your HTML to enhance readability and structural clarity for future devs.

### Svelte

#### Components

  -  Break UI elements into reusable components [componentName.svelte].
  -  Comment your component files using the following format at the top of the file:

<!-- @component
    This is a Svelte component comment that will show up on hover.
-->

  -  Limit use of complex functions in components. Instead, give each of these functions their own JS file inside of a “utils” folder, which goes in the “lib” folder.

#### Stores

Limit how much data you’re putting in a single Svelte store, as these data structures inform Svelte on when to re-render components. Keep in mind the [Single Responsibility Principle](https://stackify.com/solid-design-principles/).

#### SvelteKit

If you recall from the tutorial, Svelte is just a component framework. SvelteKit, an app framework, is what helps us with the project’s structure. To keep everything clean and organized, the following section will act as our project structure guideline. Maintaining this structure is key to keeping the website scalable, maintainable, and easily navigable for future onboarding.

## Project Structure

/src

The src directory is where the meat of our app resides. Most of our code and markup will go in here.

/lib

The lib directory is used to contain shared modules used by multiple pages or components. It can be accessed from any client file with the “$lib” alias. For a refresher, refer to [this page](https://learn.svelte.dev/tutorial/lib) in the tutorial. Example modules in this folder include:

  -  /classes - contains all [className].js files (controls interactive web applications)
  -  /components - contains all [componentName].svelte files
  -  /stores - contains all [storeName].js files
  -  /utils - contains all [utilName].js files
  -  /data - contains all [dataName].json files
  -  /hooks - contains all [useDataPipelineName].js files (parses .json files)

/routes

The routes directory contains all of the app’s subdirectories. It is important to note the [layout] and [error] files apply to subdirectories as well as the directory they live in. ([Resource](https://svelte.dev/docs/kit/routing))

It is currently organized as follows:
  -  routes
      -  production
          -  [page]
      -  themes
          -  interactive chapbooks
              -  [game]
                  -  [page]
      -  [layout]
      -  [page]

/static

The static directory contains all of our static assets like images, fonts, and videos. It will be organized as follows:

  -  images
      -  site
          -  [page]
      -  games
          -  [game]
  -  videos
      -  site
          -  [page]
      -  games
          -  [game]
  -  favicon.png

### Images

All game hero images need to be 1280px by 720px
