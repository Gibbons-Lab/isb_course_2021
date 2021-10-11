![GitHub release](https://img.shields.io/github/tag/Gibbons-Lab/isb_course_2021.svg)
![QIIME 2 version](https://img.shields.io/badge/Qiime%202%20version-2021.8-blue.svg)
[![part 1](https://img.shields.io/website?up_color=green&up_message=up&label=part%201&url=https%3A%2F%2Fgibbons-lab.github.io%2Fisb_course_2021%2F16S)](https://gibbons-lab.github.io/isb_course_2021/16S)
[![part 2](https://img.shields.io/website?up_color=green&up_message=up&label=part%202&url=https%3A%2F%2Fgibbons-lab.github.io%2Fisb_course_2021%2Fmodels)](https://gibbons-lab.github.io/isb_course_2021/models)

# Materials for the 2021 ISB Virtual Microbiome Series

## Output

All output generated during the walkthrough can be found in the
[treasure chest](treasure_chest). The easiest way to get all of that
is to [download the entire repository](https://github.com/Gibbons-Lab/isb_course_2021/archive/main.zip).

## Part 1: Amplicon Sequencing Data Analysis with QIIME 2

Presentation: [![part 1](https://img.shields.io/website?up_color=green&up_message=up&label=part%201&url=https%3A%2F%2Fgibbons-lab.github.io%2Fisb_course_2021%2F16S)](https://gibbons-lab.github.io/isb_course_2021/16S)
Notebook: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gibbons-Lab/isb_course_2021/blob/main/16S.ipynb)

You can see the actual workshop walkthrough at
https://gibbons-lab.github.io/isb_course_2021/16S. Press `?` to get a list
of available live options such as slide overviews and speaker mode. Note that
some slides are grouped vertically, you can navigate the presentation using
the directional buttons on your keyboard.
A [PDF version](part1.pdf) (lacks the output previews) is also available.


## Part 2: Metabolic Modeling of Bacterial Isolates

Presentation: [![part 2](https://img.shields.io/website?up_color=green&up_message=up&label=part%202&url=https%3A%2F%2Fgibbons-lab.github.io%2Fisb_course_2021%2Fmodels)](https://gibbons-lab.github.io/isb_course_2021/models)
Notebook: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gibbons-Lab/isb_course_2021/blob/main/models.ipynb)

You can see the actual workshop walkthrough at
https://gibbons-lab.github.io/isb_course_2021/models. Press `?` to get a list
of available live options such as slide overviews and speaker mode. Note that
some slides are grouped vertically, you can navigate the presentation using
the directional buttons on your keyboard.
A [PDF version](part2.pdf) (lacks the output previews) is also available.

# Licensing

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)<br>
All source code is licensed under the Apache License 2.0. This includes the notebooks deployed via Google Colaboratory.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a><br />Content and artwork is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License. 

This covers:

- Text content of the presentations.
- Illustrations and derived renders in the `illustrations` folder.
- Top level images in `docs/*/assets`.

The following content is not publically available and is *not* covered under the CC license above:

- Everything in the `docs/*/assets/isb` folders.<br>
  Those are images relating to the Institute for Systems Biology identity like backgrounds and logos
  that are licensed exclusively to the Institute for Systems Biology, Seattle, WA, USA.

# FAQ

### How do the presentation slides work?

The presentation itself is a webpage hosted on GitHub. Basically, it
renders dynamically from a [markdown file that includes the course](docs/16S/talk.md).
Editing the markdown file is sufficient to change the content of the presentation.

See the [reveal docs](https://github.com/hakimel/reveal.js/#markdown) for more info.

### Preview locally

Open a terminal in the `docs` folder in the repo and use:

```bash
python -m http.server
```

This will preview the talks at `localhost:8000/16S` and `localhost:8000/models` in a browser. Editing the
markdown and reloading the page should be enough.

### PDF output

To generate a PDF of the course, open up the website in chromium or chrome and
append `?print-pdf` to the address. For instance, if you ran it locally as
described above, open `localhost:8000/16S?print-pdf` in the browser. Then, choose
'print to PDF' (choose margins: none).



