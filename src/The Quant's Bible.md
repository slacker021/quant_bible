---
dg-publish: true
dg-home: true
---
# Home
Welcome to the *Quant's Bible*! This is a personal project that Zachary Ong originally created for his friends who needed help with their mathematics classes and skills. He had trouble with his mathematics classes during the first half of his undergraduate degree in computer science, bombing and barely passing many of them. 

However, his desire to be a quantitative finance researcher required him to relearn all the necessary mathematical and computer science skills that he struggled to during his first two years of undergrad. At the same time, much of the knowledge required were scattered throughout various textbooks, websites, forums, and videos all over the internet. This made constantly referring back and forth between references much harder than it had to be. Alas, he realized that he needed a way to store interrelated information in a single place that's easily accessible.  

Therefore, this collection of notes was formed as a public and ever-expanding knowledgebase dedicated to quantitative finance. The fundamental topics of focus within this knowledgebase are

  1. Pure and applied mathematics, with a special focus on mathematical finance.
  2. Mathematical and applied statistics, with a special focus on measure-theoretic theoretical statistics. 
  3. Computer science, with a focus on programming languages and paradigms 
  4. The modern art and science of finance focused on econometrics, Numeraire framework, and portfolio management. 

This collection of notes aims to present quantitative finance as a dynamic social science and independent field of study. Rather than being a disparate collection of facts and tricks, these notes construct quantitative finance from the ground-up by viewing it through the language of pure mathematics. Nearly all the notes here are interconnected, allowing readers to go back and forth between different sections as if they were in one universe.This is intended to provide a more seamless transition between different topics

---
# Who is this For?

### Quants, Economists, and Actuarial Scientists
First and foremost, this collection of notes was designed for those looking to become independent, academic, or industry researchers in quantitative finance. While much of modern quantitative finance has become abstracted by new discoveries in mathematics, economics, and finance—as well as more powerful software packages, such as *Formal Verification Systems*, *Numerical Software*, *Computer Algebra Systems*, and *Generative Artificial Intelligence*, capable of performing the most complex tasks with ease and precision—the quintessential quant researcher still demands mathematical maturity. This offers quants, actuarial scientists, and economists an uncompromised approach to topics in finance that were traditionally considered to be qualitative.

### Managerial Sciences
Researchers specializing in the managerial sciences, especially those with strong interests in data science, will appreciate the unique approach to finance that these notes offer. While business has traditionally been known to be a qualtitative artform that uses intuition and corporate know-how, the rise of big data and AI in the managerial sciences calls for the integration of quantitative skills in corporate finance. However, those who may not be very familiar with quantitative jargon may also read the intuitive explanations offered in the notes. 

### Natural Sciences and Engineering 
Students of the natural sciences and hard engineering fields, especially those interested in breaking into quantitative finance, can use this as a refresher on the mathematical knowledge they've learned but may have forgotten about. However, this offers a very different take on applied mathematics that most STEM researchers may be used to. Rather than presenting mathematics in a very intuitive manner, these notes prioritize rigor and zero-abstraction pure mathematics. Every lemma, proposition, theorem, and other deduced facts have proofs that show how these claims were derived in the first place. 

Given that quantitative finance has roots in the natural sciences and makes use of engineering principles, the mathematics sections also have non-financial mathematical examples. Many of the models that quantitative finance uses are taken directly from physics, chemistry, biology, and other natural scientific fields. However, these re-tooled models are fitted with random variables to suit the non-deterministic and stochastic nature of financial markets. 

### Quant Devs and Fintech
Members of the fintech community, quant devs, and other software developers with a strong interest in quantitative computing will be glad to see the programming knowledge on offer. The computer science and developer knowledge offered by these notes provide a mix of general programming advice, which is mostly focused on functional programming, that have applications in quantitative development. Furthermore, these notes aren't constrained to a single language and instead—the author tries to incorporate different languages into the mix so as to expose readers to different languages they otherwise may haven't heard of. In other cases, pseudocode may be used as an alternative to actual programming languages to create a more software-agnostic reading experience. 

---
# Pure and Applied Mathematics
This knowledgebase provides a rigorous and unambiguous treatment of pure and applied mathematics, showcasing full proofs and derivations so as to provide a more rigorous and step-by-step approach. 

In providing a unified approach to pure mathematics, this knowledgebase attempts to construct its own mathematical universe. All the mathematics topics are interconnected, with backlinks in one note leading to another. This applies for the proofs and derivations for various facts, as well as topics that in different branches of mathematics that have overlap. 

As for applied mathematics, the various mathematics notes have real-world examples that provide context and examples of where these abstract notions may be applied to. Unlike pure mathematics textbooks, which are often rigorous but lacking context, and applied mathematics textbooks, which provide dynamic examples but are criticized for a lack of rigor, this collection aims to be a unified approach. In this collection, mathematics is viewed as the language of the universe.

### Real and Applied Analysis
This is the most foundational of all the mathematics topics within this knowledgebase. Most of the other topics are built from real analysis. In the case of these notes, real analysis serves as the epicenter of the mathematical universe from which all other branches are constructed from. 
##### Volume 1: Elementary Calculus:
**Module 1: General Mathematical Concepts and Notation**
[[Chapter 1 - Basic Rules of Logic]]
[[Chapter 2 - Elementary Set Theory]]
[[Chapter 3 - Cartesian Products and Relations]]
[[Chapter 4 - Functions and Cardinality]]

##### Module 2: The Space of Real Numbers
[[Chapter 1 - Basic Properties of Real Numbers]]

---
# Finance
Finance has evolved greatly, from a qualitative artform that was merely considered a subfield of economics or a tool in corporate studies. These notes provide a rigorous and math-based foundation for contemporary neoclassical finance, as well as other paradigms that financial markets have accommodated. 

### Portfolio Theory

##### Volume 1: Modern Portfolio Theory and Basic Investment Analysis
[[Chapter 1 - The Theory of Choices]] 
[[Chapter 2 - Financial Instruments and Securities]]
[[Chapter 3 - Financial Markets]]

---
# Disclaimers and Notices

### Incomplete or Incorrect Information
This project is an ever-expanding collection of notes, and is expected to take years to become on par with what university textbooks offer. At the same time, managing and checking for mistakes is difficult due to the large amount of information stored here. Thus, feedback and corrections would be greatly appreciated. Send all concerns to ong.zach13@gmail.com. 

Overtime, more information will be added to this collection. It's likely that whatever the reader is looking for is merely something waiting to be added. 
### On Generative Artificial Intelligence
Certain parts of this knowledgebase have employed the use of generative artificial intelligence. Artificial intelligence is used in the following ways:
- Checking mathematical derivations and answers.
- Spotting grammatical errors or missing content.
- Generating Tikz figures of visualizations, which are first rendered via the Tikz editor before being uploaded into the notes as PNGs. 
- To help expand on the information that was originally gathered to form these notes, which are mainly taken from textbooks. 
- While the base notes are generated using a LLM, the output is heavily scrutinized and modified to ensure that they fit the author's standards of pedagogy and readability. 
The models used for assisting in developing these notes are 
- **Proprietary Models:** *Gemini 3*
- **Open-Source:** *Gemma 4 4B, Gemma 4 12B, and Gemma 4 26B*

### Financial Advice and Career Assistance
This knowledge base is intended solely for learning, conceptual development, and education demonstration. While the content synthesizes sophisticated principles from diverse disciplines, it must not be interpreted or utilized as personalized financial advice, investment counsel, or a professional mandate. Financial markets are complex systems fraught with inherent risks that no theoretical model can predict nor eliminate. Therefore, all participation in investments based on this material is undertaken solely on the reader's own discretion and risk. Furthermore, any financial data that is based in reality reflects outdated market conditions.

Additionally, this knowledge base may or may not be suited for career assistance. While this provides the conceptual and practical framework for many skills and roles in quantitative finance, it lacks personalized features like exercise problems, one-on-one meetings with an instructor, interview questions, and other creature comforts that usually come with career assistance. Should a reader desire career assistance or learning how to break in to a specific niche in quantitative finance, they should seek said career assistance from someone who explicitly provides those courses. Nevertheless, this is a useful resource as the theoretical backbone and practical knowledge one may need. 

### On Open-Access and Public Learning
This knowledge base was curated with explicit commitment to universal accessibility. It operates under an "open science" philosophy, meaning its contents are designed for communal learning and critical inquiry—from personal self-study modules to advanced university coursework. The synthesized material here is intended as a foundational resource for discussion. While the author encourages all forms of academic utilization, it's not intended as proprietary intellectual property for commercial or for-profit exploitation. The author believes that the advancement of knowledge in quantitative finance must remain freely accessible to the global research community. 

To maintain this mission of open access, the author doesn't solicit funds nor accept donations and sponsorships. The existence of this collection of research notes is predicated purely on the principle of free dissemination. Any external claim to commercialize or sell material from these notes would be contrary to the principles of this resource, and must be approached with extreme caution by anyone interested. 

To accept donations and sponsorships would jeopardize the integrity of these notes as open-access material. The author cannot be bought out nor can he be coerced into designing the notes to cater to a specific crowd of people whose vision may not align with his. Everything in these notes are curated and designed with the preferences of the author. 

# Technical Information
These notes were created markdown syntax in [Obsidian](https://obsidian.md/), a free software that allows users to view markdown files in a more elegant fashion. Hosting is done via [Forestry.md](https://forestry.md/), a web hosting service that is available as an Obsidian plugin. This allows for the look and feel of the website to be drafted before being published. In addition to using Markdown for text, all visualizations are rendered in using [Tikz](https://tikz.dev/), which the figures being exported as PNG images after being rendered in the [Tikz editor](https://tikz.dev/editor/). To help preserve and backup information in this knowledge base, this collection of notes is stored in a [public Github repository](https://github.com/slacker021/zachs_online_quant_notes.git). 

These notes can be found in the [Obsidian Garden Gallery](https://vaults.obsidian-community.com/), which is a curated showcase of the best public sites bult with Obsidian. Check out other awesome Obsidian vaults in the gallery!
