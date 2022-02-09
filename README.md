# Markdown Website
Sometimes just getting some information online doesn't need to be that hard. Doesn't even come with a build tool, don't need it.

### Cheatsheet
Not familiar with markdown? It's pretty easy. Here's a [Markdown Cheetsheet](https://www.markdownguide.org/cheat-sheet/) to get you started. The markdown you write in `.md` files will be converted to HTML and become your website.

### How It Works
`index.html` references and downloads `./src/main.md`, converts the downloaded markdown to html, and then injects it into the body.

### Images 
Put these types of things in the `/public` folder. Access them in your markdown like `/public/your-image-name.png`.

### Dev Server
I didn't include any sort of dev server with this repo, but the following should provide a pretty decent development environment. 
1. [Download NodeJS (Current)](https://nodejs.org/en/)
2. Start Dev Server: `npx nodemon --watch . -e md,css,html,js --exec 'npx sirv-cli --dev'`
3. Open `http://localhost:8080` in your browser.

Now you can make a change to the website, go back to the browser, refresh, and see your changes.

### Deploy
It should just work.

**Recommended Optimizations**
You should definitely prerender the page if you care about SEO since the `.md` file is fetched and parsed at runtime.

### Maybe Someday
- Routes and multiple pages.
- Imports inside .md files to allow for partials.
- Auto compile SCSS out of the box....might need that built tool.....
