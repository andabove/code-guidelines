# Coding Guidelines

> The style guidelines and best practices for our engineering team.

# Javascript Styles

> These are some general coding styles that should be adhered to

## Formatters

Using formatters when developing saves time and keeps a consistent style throughout the entire codebase.

We use Prettier with specific eslint configs - this is generally already setup when using either of the templates.

## Code Editor

By default we use [VSCode](https://code.visualstudio.com/) as our code editor, this is to take advantage of every developer using the same extension setup. See the .vscode folder in this repo for the essential extensions that we use, if you clone this repo VSCode will offer to install all the recommended extensions for you.

There is also a settings.json file in the folder, this allows everyone to have the base prettier setup and some other specific settings to our repos.

# HTML/CSS Styles

## Alternative text

> Alternative text, or alt text, is read out by screen readers or displayed if an image does not load or if images have been switched off.

All images, except decorative images, must have alt text that:

- tells people what information the image provides
- describes the content and function of the image
- is specific, meaningful and concise

Use normal punctuation, like commas and full stops, so the text is easy to read and understand.

Do not:

- include the name of the photographer or person who created the image
- start with ‘Image of’, ‘Graphic of’ or ‘Photo of’
- repeat information from the page
- include extra information not on the page

# Git Commits

> Git commits must be used effectively for auto-changelog

When making git commits, using the correct prefix before writing what has changed in the document is essential. Commit messages also can have an optional scope, this scope helps to see what the commit was focused on, if the scope is not entered then the message must contain information on where the fix is located. Lowercase for the entire commit is recommended.

There are currently 5 main commit prefixes with only 3 being daily uses.

### fix: \${string}

---

_fix_ is a commit type that is used for either patching a bug in code or tweaking existing code

    $ git commit -m "fix: dates not being disabled correctly on the filter calendars

    $ git commit -m "fix(calendars): dates not being disabled correctly

### feat: \${string}

---

_feat_ is used when you are implementing a new feature to the codebase

    $ git commit -m "feat: added disabled end date depending on start date

    $ git commit -m "feat(calendars): added disabled end date depending on start date

### chore: \${string}

---

_chore_ is used for anything that doesn't directly affect the codebase. Some examples are; adding/removing/updating dependencies, assets or documentation

    $ git commit -m "chore: added documentation on the calendar functions

    $ git commit -m "chore(nuxt-analytics): removed package

### rel: bumping version to \${version}

---

_rel_ should only be used when increasing the version number of the project - the version number must be the same as the one in package.json

    $ git commit -m "rel: bumping version to 1.1.0

### init: \${string}

---

Init should only be used once when creating the project

    $ git commit -m "init: inital project commit

# Branch Naming

Branch naming must follow the same prefixes that are outlined in the '_git commits_' section but instead of the prefix being followed by a scope, the prefix must be hyphenated and the overall area afterwards. Below are some examples of acceptable branch names;

    $ fix-filtering-dates

    $ feat-disable-previous-dates

    $ chore-update-analytics

# Pull requests

When creating a pull request, the title must follow the same as the git commit conventions but must always have a scope attached and then the description to be an overall review of what has changed
