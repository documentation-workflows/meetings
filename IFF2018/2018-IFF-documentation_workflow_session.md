# Documentation workflow best practices - creating standards and commons for collaborative resources

*Presenters*

Floriana Pagano
Michael Carbone 
Jon Camfield 
Maya Richman 
Chris Walker 
Rose Regina Lawrence 
Tom Lowenthal


*Contributors*

Brian Connley 
Kaustubh Srikanth
Holly Kilroy

*Notes*

This is a follow up from efforts from IFF from the past two years on how to
create documentation that can be shared and updated easily by communities and
what tools we can use to facilitate this. 

Documenation can be many different things, iuncluding guides, educational
materials, PDFs, websites. 

https://github.com/documentation-workflows/meetings  includes needs from last
year's session. 

* Tooling to automate git + markdown + transifex (for translation) 
* List of static site gernerators and other tooling for writing in markdown on
* git and then it becoming a webpage 
* non-tech contributors in markdown workflows (things besides git) 
* how do we share this? the network-centric workflows mailing list 
* locatization, presentation standardiszation 
* de-dupping atomized documents 
* better output/exploration interface (related to content not getting trapped in
* certain formats)  

### Access Now Documentation 

accessnow.github.io/community-documentation 

github.com/accessnow/community-documentation 

Processes and tools for incident handlers from the Access Now Helpdesk.
Currently the documentation is prviate in a ticketing system that is perl-based,
but they are looking at how some of it could be made public. 

There are three levels of documentation confidentiality, so things like email
addresses stay private, but there are other resources that they want to share
with partners, and then other resources that they would like to make publicly
available. Three repositiories to match this separation. There is metadata at
the top of each markdown file. This uses CI build. They are adding a <div> tag
that is parsed by a script to remove sensitive information. There is no case
documentation, so they are not having to deal with removing that. 
The hope is that this will be launched by the end of the year. 

There is not yet a plan for encouraging updates from the public. This is tied an
ongoing efforts related to a network of helpdesks. 

Currently, it is only in English, but they are looking at how to add multiple
language support. 

Partners are local and regional organizations who are already or are interested
in running helpdesks. 

Internal repo is on their internal gitlab; partner version is on gitlab.com;
public version is on github.com

Every time someone has a case that hasn't already been covered, they write a new
article. 

Suggestion: Standard Notes encrypted editor with markdown support


### Security in a Box 

securityinabox.org

SiaB migrated from Drupal to a git and markdown based static site about a year,
year and a half ago. Now, we are working on migrating it from an internal gitlab
to a private gitlab.com repo.  https://siab.gitlab.io/securityinabox/en/ 
It uses a metalsmith ssg (it is simmilar to jeckyll). 

There was a major update push last year and there has been a lot of work on the
platform, like flagging unmaintained and out of date content. 

Having the content on gitlab.com allows for us to have this staging site:
siab.gitlab.io/securityinabox 

There are personal forks that people are able to use and see to allow different
people to work on it at the same time

The number of languages included slows down the updating process, we think. The
idea is that we will see how well this set up works with translators in the next
few months after there is a major update push for the tactics guides. 

There is a desire for integration between transifex and git, but that does not
one that we know about. 

There is no clever way of showing how old various pieces are. 

This project is using ticketing and issues to address workflow. 

This uses a Content as Code approach from iilab:
https://iilab.github.io/contentascode/

This project does not contain videos and audio, but markdown allows for html
blocks really nicely, and other sites we have worked on use that approach. 


### Level UP 

level-up.cc 

The website went through the drupal to content as code process as well. 

A lot of the material is about methodologies for trainers, some of it is more
time-tied. There is curriculum as well. There needs to be a community manager or
steward to keep it going, but there is not currently one. 

They experimented with transifex, but the content has not been fully translated
into any single language, but this would be really good. 

They recently migrated to an eclipse server, since hosting is an ongoing need
like contributions and translations. There is a seperate workflow for
contributions and other concerns about them. It is really hard to coordinaate
and manage a resource, even when everyone is really amazing. The human side of
this is very important. 

There is not currently a "needs list" but one will be going out soon, but that
is more about maintainance than about specific technical needs like making a
nicer inerface. 

This gets a lot more complicated when it is a network-centric thing than a
single team. 

Major challenges in restructuring the content in the website: figuring out what
goes where, user expectations, trainers are not a homogenous approach. 

Questions about exporting the thought process of workflows. The wiki for the
level up project has a lot of screenshots on how to do this. 


### SAFETAG

https://safetag.org/ , https://safetag.org/guide/ ,

https://github.com/SAFETAG/SAFETAG  

SAFETAG is a high-level framework for how to approach an audit. There are many
different ways to do things. It is modular and not a step-by-step. It exists as
a website, PDF, and github repo. Current site is horrible javascript, but it
works. There are specific exercises and goals. There are many different levels
and kinds of objects and the entire thing is remixable. They started with
markdown and git and isn't quite the same approach as CaC, but coming from the
same idea. 

There are lots of markdown files that then pull in other markdown files, but
this means that they can pull different sectinos and only pull what is needed. 

There are also curriculla. They did transclusion the hard way. They are now
looking at how to move SAFETAG into the CaC framework. They are working on
figuring out the new interface as well. 

The issues with creating a PDF or even a website is that it makes this very
non-linear thing into something with a heavy linear assumption. 
They are looking for beta-testers/ beta-victims. 

The new site is up on github.io, but it is a few iterations behind. 


### Activist Apprentice / Station

Content as Code has been being bounced around a lot for a few years ago. 
There is a problem that when stuff doesn't look good, people are unlikely to use
it. And it's hard to make things look good. So starting with markdown was a hard
sell, especially if we need to convince people to use the materials in the first
place.  

This project is specifically for addressing low or no internet context. 
Git is hard for people who aren't techies. 

AA converts content into android apps, and optionally publishes it on Station
Station is built on F-droid, which is basically just a market place for people
to access. Ripple is integrated in so that there is a panic button that hides
the app on the phone. This is to address problems where people get trained and
given resources and then they get caught on the way back into a country and it
gets seized or the person is arrested or worse. 

One nice things is that the folders in git look a lot like folders on a laptop
and using that with atom is ugly, but approachable. 

The goal is to be able to go from text files to an APK in three terminal
commands. They are maybe a month away from being able to build APKs. 

The development is public: https://gitlab.com/contentascode/activist-apprentice
https://gitlab.com/contentascode/activist-apprentice-course-template

Why not have a CI that makes the APK? That is kind of the hope eventually. but
also doing it locally means that you don't need to have internet access in order
to make this happen. 

Currently, it makes an Expo app instead of a native app. 


### Umbrella and Tent

https://secfirst.org/

Umbrella is an app with digital and physical security advice. The content is
being continuously updated and pulled for other reoucres in the community and
then made to work well on a mobile platform. 

Version 2.0 is adding in a management system for teams and organizations. There
is also a visualization of this and support for iOS and desktop. 

Language support for Spanish and Chinese. French and Arabic coming soon. 

Tent allows other people to do this as well and to still get the benefit of
updates to umbrella. 

Also uses git and Content as Code. 

Will be available for iOS later this year. 


### Totem

https://totem-project.org/

Online learning platform from Greenhost for digital security learning. 

Built on top of Open EdX, but with security and privacy enhancements. 

Open EdX Studio is a CMS for making courses, but it is bad for writing text and
stuff cannot be easily reused or translated. 

They are starting to use weblate, which is similar in features to transifex. 

The problem that they are currently addressing is that they need to make the
pipeline for going from markdown to something that connects to open EdX Studio,
as well as piping to go from OpenLeaningXML or OLX back and forth to markdown. 
Weblate allows you to work directly with json isntead of using PO files, like
transifex does. Also, since it is open source and self-hosted, they have more
ability to build a workflow. 

Weblate integrates directly with git repos, but you still have to figure out how
to structure it so that everything works. 


### General Discussion

Drupal gives you much easier onboarding and there are lots of plugins, but
markdown means that you don't have to worry about your drupal getting hacked and
your content isn't locked in. The bit thing that is missing from this is really
the editor and workflow. 

Reminder that drupal can also have a really hard learning curve. harder to
create content maybe, but everything else is easier, including saving and
archiving content. 

there is a need to basically hide the git from main contributors. Even fairly
technical people have a really hard time with this 

There is a potential trade-off between git and manager. 

Git does still have a lot to help with 

GUI that goes bing would be really amazing because it's helpful for developer
types, let alone non devs. Can we have unified system best practices and make a
nice GUI for this? 

Idea that there is different mindset from sys admin mode and trainer mode even
for people who are both of them. 

forestry.io might allow people to edit static sites with visual editor, also
Prose. 

There is also tooling to go from other formats 

There is no centralized building of this and there is no main funding. We are
not going to find this, we will need to make it and we are more likely to
succeed together.  

Problem of forgetting how to do this (method documentation) 

There is a difference between corporate tools and FOSS that we use. it's going
to be rougher. 

With rapid response situations, it's really local. Free is really important.
Free as in beer 

Transclusion is the ability to pull secttions of another thing into a place.
Technically, if you pull an entire document it is called transclusion instead. 



Potential Lists that might be helpful: 

* edge case problems (like bulk uploading images) 
* list of workflows/ work models 

https://www.fabriders.net/network-centric/

