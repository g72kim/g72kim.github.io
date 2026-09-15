# Grace Kim’s portfolio

A simple portfolio built with HTML and CSS. Open `index.html` in your browser to preview it. After editing, save your files and refresh the browser.

## Edit the experience and education timeline

In `index.html`, find `<section id="experience"`. Education appears above a horizontal year axis; the four co-op cards sit below their corresponding years. Dates inside each card give the exact work term. The card widths do not represent duration.

Edit the dates, job title, company, and location directly in each `<li class="timeline-card">` block. To add a role in an existing year, copy a complete card into that year's `<ol class="timeline-jobs ...">` list. Education is in the `timeline-school` blocks above the axis.

The year columns and positions are controlled in `styles.css` (`jobs-2024`, `jobs-2025`, and `jobs-2026`). Keep detailed project descriptions in the Projects section. On smaller screens, swipe the timeline sideways, or focus it and use the arrow keys.

## Add attachments to a project

Click any project card on the homepage to open its page. Each project has an HTML page in `projects/` and a matching folder in `assets/projects/` for its files.

| Project | Page to edit | Attachment folder |
| --- | --- | --- |
| Robotic hand | `projects/robotic-hand.html` | `assets/projects/robotic-hand/` |
| Multi-robot workbench | `projects/multi-robot-workbench.html` | `assets/projects/multi-robot-workbench/` |
| DAB converter | `projects/dab-converter.html` | `assets/projects/dab-converter/` |
| Cochlear implant | `projects/cochlear-implant.html` | `assets/projects/cochlear-implant/` |
| Gait prediction | `projects/gait-prediction.html` | `assets/projects/gait-prediction/` |
| Microphone amplifier | `projects/microphone-amplifier.html` | `assets/projects/microphone-amplifier/` |
| Financial planner | `projects/financial-planner.html` | `assets/projects/financial-planner/` |

### Example: add microphone amplifier materials

1. Copy your files into `assets/projects/microphone-amplifier/` using VS Code or File Explorer.
2. Open `projects/microphone-amplifier.html` in VS Code.
3. Find `<!-- ADD ATTACHMENTS HERE`. Paste one or more examples below **above that comment**, inside the attachments section.
4. Match the filenames to your actual files, including capitalization. Remove the paragraph saying `Project materials coming soon.` once you add materials.
5. Save, then refresh that project page in your browser.

Files do not appear automatically: each needs an image, video, or link in the HTML. The `../` at the beginning of a path means “go up one folder” from `projects/` to the main website folder.

**Photo or circuit diagram:**

```html
<figure>
  <img src="../assets/projects/microphone-amplifier/circuit.jpg"
       alt="Microphone amplifier circuit on a breadboard" loading="lazy">
  <figcaption>The amplifier circuit and test setup.</figcaption>
</figure>
```

**PDF report:**

```html
<ul class="attachment-links">
  <li><a href="../assets/projects/microphone-amplifier/report.pdf">Read the circuit report (PDF)</a></li>
</ul>
```

**Video file:**

```html
<figure>
  <video controls preload="metadata" aria-label="Microphone amplifier demonstration">
    <source src="../assets/projects/microphone-amplifier/demo.mp4" type="video/mp4">
    <a href="../assets/projects/microphone-amplifier/demo.mp4">Download the demo video</a>
  </video>
  <figcaption>Describe what the demonstration shows.</figcaption>
</figure>
```

For a hosted video or code repository, paste its full URL into a link:

```html
<a class="text-link" href="https://github.com/g72kim/your-repository">View source code</a>
```

**Excel workbook** (paste in `projects/financial-planner.html`):

```html
<a class="text-link" href="../assets/projects/financial-planner/planner.xlsm" download>Download the financial planner (.xlsm)</a>
```

Use your actual file extension, such as `.xlsx` or `.xlsm`. These links open or download files; Excel workbooks do not run inside the webpage.

## Add a new project

1. Copy a complete `<article class="project-card">...</article>` block inside the homepage's `project-grid`.
2. Update its title, category, summary, and tags. Change the title link to `projects/your-project.html`. Keep one link per card because it covers the whole card.
3. Copy an existing page in `projects/` to `projects/your-project.html`. Update its browser title, heading, description, and attachment paths.
4. Create `assets/projects/your-project/` and add your files there using the examples above.

### Add your résumé

Put `resume.pdf` in `assets`. In the header of `index.html`, find the résumé link and remove the surrounding `<!-- ... -->` comment, including the explanatory sentence, to display the link.

## Change the appearance

`styles.css` controls the layout, spacing, and colors. The color variables are at the top. No build step or package installation is needed.

## Publish updates

Commit and push your changes to the branch configured for GitHub Pages. This edit does not publish the site automatically from your local computer.
