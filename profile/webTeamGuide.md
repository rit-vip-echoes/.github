# **Web Team Guide**

### Important Documents

  - [Web - CI/CD](https://docs.google.com/document/d/1w3YIf5MbOnMSgP71NCYNCVwLVZvUfQISk5HgYp3n5Kk/edit?tab=t.0#heading=h.bz1o5140s4ge) - Explains the current CI/CD pipeline of the website.
  - [Website Outline & Info](https://docs.google.com/document/d/1tF_rkHCGwf7O9klohHy861KQmPCc39B_jhrhkuiZ63I/edit?tab=t.0#heading=h.vc3nlztxwuhi) - Details the content and flow of the website.
  - [RIT Official VIP Website Content](https://drive.google.com/drive/u/1/folders/1Y8HwBIynjNnL_ZfI1Sw9FjzOcf-dfs7f?ths=true) - Content for the website.

## Getting Started

1. Download and install VSCode + the [VSCode Extensions](https://docs.google.com/document/d/12TpMxFRPnAxTtqIhqanuayRmCgFmaLlivKxt0iqhiMU/edit?tab=t.po4cipcmytvq#heading=h.6262kmzc6qcc)
2. Install NodeJS
3. Clone the repo
4. [Node and NodeJS](https://docs.google.com/document/d/12TpMxFRPnAxTtqIhqanuayRmCgFmaLlivKxt0iqhiMU/edit?tab=t.po4cipcmytvq#heading=h.b4399690d2jn) to run local server

### Design Tooling

For the initial design of the website, [Figma](https://www.figma.com/) was used for mocking up page layouts. Given the limited mockup needs of this project, we left the design process rather loose, with each member using Figma independently rather than as a team. In the event future teams need more design work on this scale, there are a myriad of online resources and tutorials available via YouTube, paid courses, and more.

Use [this link](https://help.figma.com/hc/en-us/sections/4405269443991-Figma-for-beginners-4-parts) to see a 4-part Figma tutorial.

## VSCode Extensions

<img width="830" height="222" alt="image" src="https://github.com/user-attachments/assets/732cf32f-8210-4a96-8738-2769ac4bf72e" />

<img width="972" height="229" alt="image" src="https://github.com/user-attachments/assets/fb66d01b-d0a0-4eed-a028-7e01846199b1" />

<img width="874" height="241" alt="image" src="https://github.com/user-attachments/assets/01a013ee-0e39-4445-b6ff-7c9113ac9b56" />

<img width="1015" height="293" alt="image" src="https://github.com/user-attachments/assets/3cc4dae1-a992-43d5-b2de-a608acb66447" />


### Svelte/SvelteKit

Svelte is a compiler-based UI framework that uses familiar languages (HTML, CSS, and JavaScript) in a unique context. While React is battle-tested and well supported, it can be rather obtuse when it comes to simple projects. Meanwhile, Svelte is much simpler to set up, understand, and get working quickly.

At the beginning of Fall 2024, the latest major version of Svelte was Svelte 4. As a consequence, the website is currently written in Svelte 4. Since then, Svelte 5 has come out, deprecating, but not disabling, some Svelte 4 features. However, the [Svelte 4 Tutorial](https://v4.svelte.dev/tutorial/basics) still exists, and as such we will be following it. Team members should make it through the following within the first two weeks (finishing the rest as needed or if desired throughout the semester):

#### Basic Svelte
  -  Introduction
  -  Reactivity
  -  Props
  -  Logic
  -  Events
  -  Classes and styles
#### Basic SvelteKit
  -  Introduction
  -  Routing
  -  Shared modules
  -  Stores

Progress through the tutorials should be checked at each team meeting during standups. During these first two weeks, simple tasks will be provided to complete alongside the tutorials for early active immersion in the project.

Some additional materials:

[Svelte in 100 Seconds](https://www.youtube.com/watch?v=rv3Yq-B8qp4)

[SvelteKit Full Course](https://fireship.io/courses/sveltekit/) (don’t pay for this, just follow the first few modules)

### TailwindCSS

For a unique and simple project like echoes, a fleshed out UI Framework would have:

  -  Forced us into predefined styles and configs
  -  Added more overhead to onboarding new members

Instead, the website utilizes Tailwind for styling components. Tailwind works through simple utility classes added directly to your HTML, giving you perfect, active control over your styling without having to go back and forth between html and css files. Class names are more-or-less intuitively designed to respond to the vanilla css you learned previously.

The following resources should give you a good understanding of how Tailwind works:

  -  [Tailwind in 100 Seconds](https://www.youtube.com/watch?v=mr15Xzb1Ook) - Watch this.
  -  [Tailwind CSS is the worst…](https://www.youtube.com/watch?v=lHZwlzOUOZ4) - Watch this too.
  -  [The Tailwind Docs](https://tailwindcss.com/docs/installation) - Read through the “Core Concepts” and “Customization” sections. Then, refer to the rest of the documentation as needed when completing tasks. Use the search bar in the top left to look up specific styles or CSS concepts and their related documentation/examples.
  -  [Ultimate Tailwind CSS Tutorial // Build a Discord-inspired Animated Navbar](https://www.youtube.com/watch?v=pfaSUYaSgRo) - Watch this if you’d like a more in-depth example of how to use Tailwind.
  -  [SvelteKit & TailwindCSS Tutorial – Build & Deploy a Web Portfolio](https://www.youtube.com/watch?v=-2UjwQzxvBQ) - Skim through this after completing the Svelte tutorials and all other Tailwind resources to understand how Tailwind is used specifically in Svelte.

## Node and NodeJS

NodeJS is an open-source Javascript runtime environment. This means you can use NodeJS to run and test your code using the terminal/command line interface. Node commands can be entered using the terminal window or in VSCode’s terminal. To use NodeJS commands in the terminal, first make sure you are in the correct folder in the echoes Web repository.

<img width="1178" height="165" alt="image" src="https://github.com/user-attachments/assets/fc9b5714-e0b5-466d-8161-afb53a52cdc9" />

For the echoes website, we use the node command ‘npm run dev’ to launch a preview of your code on a local server. Once you are done testing, press CTRL + C twice to stop the server.

#### You will need to download and install NodeJS to use it.

[Introduction to Node.js](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs)

[Download Node.js](https://nodejs.org/en/download)

[Node.js Introduction - W3Schools](https://www.w3schools.com/nodejs/nodejs_intro.asp)

## Git and GitHub

### Project Board/Task Management

[The Web Project Board](https://github.com/users/EchoesVIP/projects/1/views/1) is organized into several columns: Ideas, Benched, Waiting, To-Do, In Progress, and Under Review. Each has a description you can refer to when determining where a card should go. Be sure to update these frequently to ensure the project board has the most up-to-date information.

Pull Requests

[How to create a pull request in 4 min | GitHub for Beginners 2024](https://www.youtube.com/watch?v=nCKdihvneS0)

A good pull request should generally include the following:

  -  What Issue is being referenced
  -  What was changed
  -  Why it was changed
  -  How it was changed 
  -  A screenshot, if necessary

Every team member should also be requested to review and approve changes before merging. 

#### (Optional) Command Line Interface

Accessing a branch: git checkout <branch name>

Accessing a new branch: git checkout -b <branch name>

[GitHub Basics Made Easy: A Fast Beginner's Tutorial!](https://www.youtube.com/watch?v=Oaj3RBIoGFc)

[Git Tutorial for Beginners: Command-Line Fundamentals](https://www.youtube.com/watch?v=HVsySz-h9r4)

### Accessing Vercel

Vercel is our current deployment platform for the website. When code is merged or pushed into the main branch of the repository, Vercel automatically redeploys to reflect those changes. To view the most recent deployment of the website, visit the [echoes website.](https://www.echoes-vip.org)

Vercel also goes through the trouble of producing private branch deployments. Unfortunately, these can only be accessed by Vercel collaborators. Collaborating with others on Vercel is costly (20$/seat/month). Fortunately, we can deploy private GitHub repositories with GitHub collaborators at no cost (see [Web - CI/CD](https://docs.google.com/document/d/1w3YIf5MbOnMSgP71NCYNCVwLVZvUfQISk5HgYp3n5Kk/edit?tab=t.0#heading=h.bz1o5140s4ge) for details on how that’s done); however, this means direct Vercel access will be limited to Erika and the web lead.

### References

  -  [Web - CI/CD](https://docs.google.com/document/d/1w3YIf5MbOnMSgP71NCYNCVwLVZvUfQISk5HgYp3n5Kk/edit?tab=t.0#heading=h.bz1o5140s4ge)
  -  [Website Outline & Info](https://docs.google.com/document/d/1tF_rkHCGwf7O9klohHy861KQmPCc39B_jhrhkuiZ63I/edit?tab=t.0#heading=h.vc3nlztxwuhi)
  -  [RIT Official VIP Website Content](https://drive.google.com/drive/u/1/folders/1Y8HwBIynjNnL_ZfI1Sw9FjzOcf-dfs7f?ths=true)
  -  [https://www.figma.com/](https://www.figma.com/)
  -  [https://help.figma.com/hc/en-us/sections/4405269443991-Figma-for-beginners-4-parts](https://help.figma.com/hc/en-us/sections/4405269443991-Figma-for-beginners-4-parts)
  -  [https://svelte.dev/tutorial/svelte/welcome-to-svelte](https://svelte.dev/tutorial/svelte/welcome-to-svelte)
  -  [Svelte in 100 Seconds](https://www.youtube.com/watch?v=rv3Yq-B8qp4)
  -  [https://fireship.io/courses/sveltekit/](https://fireship.io/courses/sveltekit/)
  -  [Tailwind in 100 Seconds](https://www.youtube.com/watch?v=mr15Xzb1Ook)
  -  [Tailwind CSS is the worst…](https://www.youtube.com/watch?v=lHZwlzOUOZ4)
  -  [https://tailwindcss.com/docs/installation](https://tailwindcss.com/docs/installation)
  -  [Ultimate Tailwind CSS Tutorial // Build a Discord-inspired Animated Navbar](https://www.youtube.com/watch?v=pfaSUYaSgRo)
  -  [SvelteKit & TailwindCSS Tutorial – Build & Deploy a Web Portfolio](https://www.youtube.com/watch?v=-2UjwQzxvBQ)
  -  [https://www.echoes-vip.org](https://www.echoes-vip.org)
  -  [How to create a pull request in 4 min | GitHub for Beginners 2024](https://www.youtube.com/watch?v=nCKdihvneS0)
  -  [GitHub Basics Made Easy: A Fast Beginner's Tutorial! ](https://www.youtube.com/watch?v=Oaj3RBIoGFc)
  -  [Git Tutorial for Beginners: Command-Line Fundamentals](https://www.youtube.com/watch?v=HVsySz-h9r4)
  -  [Introduction to Node.js](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs)
  -  [Download Node.js](https://nodejs.org/en/download)
  -  [Node.js Introduction - W3Schools](https://www.w3schools.com/nodejs/nodejs_intro.asp)
