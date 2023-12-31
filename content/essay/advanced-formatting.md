---
section: Write Your Essay
nav_order: 4
title: Formatting with Markdown
---

---

**Goals**: Edit the essay's table of contents; Add footnotes

**Estimated Time to Complete**: 15 minutes

---

## Step 1. Navigate to Your Project Repository

1. Log in to GitHub (<https://github.com>{:target="_blank" rel="noopener"}).
2. Once you're logged in, select the dropdown arrow in the very top-right corner of your browser window. Once you select this, a dropdown list should appear that starts with the words "Signed in as [your username]." On the dropdown, locate the link titled "Your repositories" and click on it. This will take you to your GitHub account and a list of all the repositories you've ever created.
3. Locate the name of the repository you created for this project, and click on it. This will bring you to your project repository and website, where you can continue editing files following the steps below.

---

## Step 2. Open Your Website in a New Browser Tab or Window

1. In the "About" section of your repository homepage (the section to the right of the green "Code" button), locate the URL for your project site. Right click this URL and select either "Open link in new tab" or "Open link in new window."
2. Now you should have two tabs/windows open: **one with your GitHub repository** (the "*back end*" of your site) and **one with your website** (the "*front end*" of your site). You'll need both of these tabs/windows open for the duration of this Lab, and you'll work with both of them open in future Labs.

---

## Step 3. Essay Sections

1. In your GitHub repository, locate and click on the "pages" folder.  
2. Inside the "pages" folder, click on the file titled "essay.md." Then select the pencil button in the top right corner of the `essay.md` file to open editing mode. 

To break your essay into sections (example: Introduction, Conclusion, etc.), you can title each of those sections using headings.

You can have multiple headings of the same type throughout your essay, and nest headings hierarchically just as you would an outline, like this: 

```
# First Heading 1

## First Heading 2

# Second Heading 1

## Second Heading 2
```

...which looks like this on the front end:

# First Heading 1

## First Heading 2

# Second Heading 1

## Second Heading 2

<br>

Remember, always separate a heading from the text below it with a blank line.

---

## Step 4. Edit the Table of Contents

To further organize your essay, you'll probably find it convenient to make use of the table of contents box at the top of the essay.

The table of contents is generated by the line of code near the top (probably on or around line 7) of your `essay.md` file that looks like this:

`{% raw %}{% include feature/nav-menu.html sections="Introduction;Conclusion;Notes" %}{% endraw %}`

Look closely at this line of text. 
This is called the "Table of Contents Include."

See the word "sections"?

"sections" is followed by an equals sign (`=`) and three words separated by semicolons and encased with quotation marks: `"Introduction;Conclusion;Notes"`.

The three words inside the quotation marks correspond to headings in the default `essay.md` file:

`## Introduction`

`## Conclusion`

`## Notes`

As long as these headings exist both on the page *and* in the Table of Contents Include, users of your website will be able to click on a Table of Contents link to scroll to the related section of your essay.

To see this in action, take a look at the front end of your essay web page.
Immediately underneath the navigation bar, there's a box that contains the word "Contents" followed by the links "Introduction," "Conclusion," and "Notes."
Click on any of these links and your page will automatically scroll down to the specified section.

**In order for the contents box to work correctly, the word in the Table of Contents Include needs to match a heading somewhere in your essay.**
Your heading just needs to be preceded by one or more pound signs (`#`) in order for this feature to work (it doesn't matter how many pound signs). 

### Now try it yourself

1. In editing mode for your `essay.md` file, add a new heading by copying the following: `### My First Subheading`, and pasting it into the `essay.md` file somewhere after the `## Introduction` heading but before the `## Conclusion` heading.

2. Locate the Table of Contents Include: `{% raw %}{% include feature/nav-menu.html sections="Introduction;Conclusion;Notes" %}{% endraw %}`

3. In the Table of Contents Include, add your new heading and a semicolon between the words "Introduction" and "Conclusion," like this: `"Introduction;My First Subheading;Conclusion;Note"`

4. Scroll down to the bottom of the file and type a commit message into the "Commit changes" text box.

5. Click the green "Commit changes" button to save your changes.

6. Head over to where you opened your "Essay" page in a different tab or window.

7. Wait a minute or two, then refresh the "Essay" page.

8. Once you refresh your site, you should see your changes.

9. The updates may take a few seconds to a few minutes to appear, so hold tight and keep refreshing if you don't see them right away.

You can add, edit, and delete as many headings in your Table of Contents Include as you'd like!

---

## Step 4. Add Footnotes to Your Essay

You'll need to cite the sources for your multimedia essay just as you would for any academic essay.
You'll be using [Turabian Style](https://www.chicagomanualofstyle.org/turabian/turabian-notes-and-bibliography-citation-quick-guide.html){:target="_blank" rel="noopener"} to add your essay citations as footnotes.

To add a footnote in Markdown, use this formula:

`Example text to be cited.[^1]`

`Yet more text to cite.[^2]`

Then, at the very bottom of the page, create a section with the heading `## Notes`, and add corresponding bracketed footnote numbers (i.e. `[^1]`, `[^2]`, `[^3]`, etc.), followed by a colon (`:`) and citation, like this:

`[^1]: Rowlandson, Mary. "The Narrative of My Captivity." In *The Making of the American Essay*, edited by John D’Agata, 19–56. Minneapolis: Graywolf Press, 2016.`

`[^2]: Sharon Sassler and Amanda Jayne Miller, *Cohabitation Nation: Gender, Class, and the Remaking of Relationships* (Oakland: University of California Press, 2017), 114.`

On the front end of your essay page, your footnote number will automatically link down to the proper citation, which will reside at the "foot" of your essay.
To see this in action, look at the cited text below, and click on the blue `1` and `2` footnotes at the end of each line.
When you click on them, you'll be taken to the `Example Notes` section at the bottom of this page.

Example text to be cited.[^1]

Yet more text to cite.[^2]

### Now try it yourself

1. In your GitHub repository, select the pencil button in the top right corner of the `essay.md` file to open editing mode. 

2. At the end of one of the sentences in your `essay.md` file (doesn't matter which sentence, this is just for practice), add `[^1]`.

3. Scroll to the `## Notes` section at the bottom of the `essay.md` file.

4. Leaving an empty line underneath the `## Notes` heading, paste this citation: `[^1]: John D’Agata, ed., *The Making of the American Essay* (Minneapolis: Graywolf Press, 2016), 19–20.`

5. Notice the asterisks in the middle of that citation? Remember, they make the text look italicized on the front end of your webpage. You'll probably use asterisks quite a bit in your citations, for book titles and journal titles!

6. Scroll down to the bottom of the file and type a commit message into the "Commit changes" text box.

7. Click the green "Commit changes" button to save your changes.

8. Head over to where you opened your "Essay" page in a different tab or window.

9. Wait a minute or two, then refresh the "Essay" page.

10. Once you refresh your site, you should see your changes.

11. The updates may take a few seconds to a few minutes to appear, so hold tight and keep refreshing if you don't see them right away.

---

## Step 5. Write Your Essay

You're now ready to start generating essay content!

Begin utilizing your GitHub Markdown skills to write and format your essay.
When you're ready to incorporate primary source documents and images into your essay, proceed to the next step.

---

## Example Notes

[^1]: Rowlandson, Mary. "The Narrative of My Captivity." In *The Making of the American Essay*, edited by John D’Agata, 19–56. Minneapolis: Graywolf Press, 2016.

[^2]: Sharon Sassler and Amanda Jayne Miller, *Cohabitation Nation: Gender, Class, and the Remaking of Relationships* (Oakland: University of California Press, 2017), 114.

