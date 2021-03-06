---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: myst
      format_version: '1.1'
      jupytext_version: 1.1.0
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---
<!-- 
+++ {"slideshow": {"slide_type": "slide"}}

# Tutorial slides

- Slides are optional (e.g., you may not use them if your presentation is via live coding).
- If the pre-recorded presentations will use slides, we request that you deposit the slides in this folder.

+++ {"slideshow": {"slide_type": "slide"}}

## Use text-based source

- We ask that you use text-based formats for your slides, e.g., markdown 
- This markdown file is an example source for slides using `nbconvert` and Reveal. See the GitHub action '.github/workflows/slides.yml' in this repo so see how this markdown file is converted to a HTML slide show and published on GitHub Pages - https://fawazsiddiqi.github.io/slides_to_pages

+++ {"slideshow": {"slide_type": "subslide"}}

## An example sub-slide

- Another option: you can write your slide content using markdown and use an app for slide design, like [Deckset](https://www.deckset.com) or similar.

+++ {"slideshow": {"slide_type": "slide"}}

## Naming convention and file list

- Use a **naming convention** where each file name starts with a number, reflecting the order of use in the presentation of the tutorial.
- List your slide files in a markdown, with a brief description.


+++ {"slideshow": {"slide_type": "slide"}} 
-->


**🌟 Overview** <br />
In this workshop, you will learn how to analyze and visualize data to gain quick insights on IBM® Watson™ Studio. We will be analyzing a loan transaction data set using Cognos Embedded and Dashboards to discover insights that can help detect and validate any important relationships and meaningful differences in individual visualizations.

🎓 What will you learn? <br />
• What are interactive dashboards <br />
• How to explore Data Analysis <br />
• How to visualize data

👩‍💻 Who should attend? <br />
All Developers interested in analytics and data science are welcome to attend the webinar!

+++ {"slideshow": {"slide_type": "subslide"}}

🎙️ Speakers <br />
- Mridul Bhandari, IBM Developer Advocate, https://www.linkedin.com/in/mridul-bhandari
- Khalil Faraj, IBM Developer Advocate, https://www.linkedin.com/in/khalilfaraj/

🎈 Prerequisites <br />
☁ Register for a free IBM Cloud Account: https://ibm.biz/credit-loan-analysis <br />

🍉 Register for the live stream and replay on Crowdcast: https://www.crowdcast.io/e/analyze-loan <br />

👩‍💻Resources <br />
- Survey - https://ibm.biz/survey-cognos
- GitHub Repository - https://http://ibm.biz/cognos-emb-ws
- Workshop Slides - https://ibmdevelopermea.github.io/Loan-Bank-Transactions-Cognos-Embedded/
- Meetup page - https://www.meetup.com/IBM-Cloud-MEA/events/ 

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide1.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide2.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide3.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide4.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide5.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide6.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide7.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide8.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide9.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide10.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide11.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide12.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide13.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide14.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide15.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide16.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide17.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide18.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide19.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/IBMDeveloperMEA/Loan-Bank-Transactions-Cognos-Embedded/blob/main/Images/slide_images/Slide20.jpeg?raw=true)


+++ {"slideshow": {"slide_type": "slide"}}
## License

**Recommend** that slides be shared under a [CC-BY](https://creativecommons.org/licenses/by/4.0/) license.
