# Hello Folks
This is the source code of my [personal site](http://tony-jones.github.io) based on Jekyll. I have recently moved from this [WordPress](https://github.com/tony-jones/anthonyjones) theme I built to Jekyll.

## About this Repository
All code is open for you to use, change, edit, learn from etc.
Let me know if you need any help setting up a similar workflow.

## The Workflow
* Type '**rake new**' to create a new post or '**rake import**' to import an old post
* Commit changes to the 'source' branch on GitHub
* Run the '**rake publish**' Rake task to compile and push to the master branch
* GitHub Pages pulls master branch by default

## Say Hello!
Feel free to say hello over on twitter [@iamtonybagels](http://twitter.com/iamtonybagels).

## Initial Release Features
- Rake tasks to Create a new post and import old post
- Rake task to automatically update the master branch from the source branch
- SASS _assets compile to /assets folder
- Blog and Project Post Types are separated out.
- Post Read Time estimations in Liquid
- Jekyll-Timeago plugin for human readable dates
- Post Navigation for Collections (Navigation for posts is already in Jekyll)

## To-do Features
- Minify Javascript, CSS, and HTML
- Refactor old code and styles that aren't needed.
- Responsive Images using srcset/fill.

## License

Apache 2.0  
Copyright 2015 Anthony Jones
