# NEED: Tooling to automate git+markfdown/transifex

  * Yes but transifex requires pull access
  * Requires some formatting standardization
  * Tails: gens po files from source code using PO4A that merges partially/existing translated documents to bootstrap
  * SSGs lack translation PO file plugin; perhaps we must deal with this outside the SSG work

Summary need: 2-way git/PO workflow

# NEED: List of SSGs; other tooling infrastructure for write-git-review workflow

what is the continuous integration wrokflow
what are the review processes and checklists (internationalized, localized, what is the doc testing protocol)

* Maya knows a list of SSGs: staticgen.com
* Jekyll; Metalsmith?
* Content as Code also has some options
* gitlab, github, gitlab.com

problem: interactive things commenting, sitesearch?

# NEED: non-tech contributors in markdown workflow

* Atom with git
* plus solid training to express the git magic words in normal editing workflow, git workflow is horribly obfuscated
* Prose is probably not good for large-scale, but worth noting
* git* web interfaces allow some preview/live editing -- web interfaces may be a requirement

# NEED: How do we as a documentation community share best practices, document documentation, and continue our work?

* Is there an existing place where people gather?
  * orgsec.community? contentascode? discourse? gitlab/hub to use issues-as-discussion
  * Jun to host a rocket.chat or mattermost?
  * Please something with email and chat and stuff

There is an IFF mattermost channel, @houndbee / kaustubh@ttc will follow up with Jun and others to create something better. Michael wants it pushed to email.

WHO DOCUMENTS THE DOCUMENTERS

# NEED: Localization presentation standardization

* making this work the same at some level
* standardized info architecuture/metadata?
* establish a norm: translation: all in the same folder: resource.lang.ext

# NEED: De-duping atomized documents

* e.g. having one guide for a tool, and have that at the tool, built with the tool, and linked across!

# NEED: Better output / exploration interface

* Better build workflows to avoid indesign lockin
* We need to build a list of current approaches!
  * Seamus' Document-Builder to string markdown preprocessing; pandoc, PDF printing and CSS underpinning with pandoc and wkhtmltopdf which leverages CSS to solve some problems
  * Tom has as process as well
  * SIAB also uses pandoc
  * is web to pdf the best path, or do we template in LaTeX? -- easier CI workflow than htmlcss->pdf
  * Depends on the frequency of content vs design changes and # of design targets (books, web, booklets, apps, mobile...?) -- monthly or annually has big different pain points
  * cryptoparty - CI with pandoc with html/pdf/ via github.com/cryptoparty/handbook

* SIAB pipeline uses pandoc for html and pdf; there is overall a dependency problem
