# Instructions
Ref: https://ssmusoke.com/tag/gitbook/

<pre>
Install npm
Install Gitbook cli by typing the command below
$ npm install gitbook-cli -g
Setup a git repository for the project and add the following files:
.gitignore – include the _book directory in which the book will be generated
book.json sample below
{
  "title": "My Book",
  "description": "Description",
  "author": "Author Name",
  "gitbook": ">= 3.0.0",
  "structure": {
    "summary": "SUMMARY.md",
    "readme":"README.md"
  }
}
README.md the default information on the book
SUMMARY.md the Table of contents for the book, which may be in different directories recommended is a docs directory
# Summary

* [Introduction](README.md)
* [Chapter 1](docs/chapter1.md)
* [Chapter 2](docs/chapter2.md)
package.json – contains build commands for the book
{
  "scripts": {
    "docs:prepare": "gitbook install",
    "docs:watch": "npm run docs:prepare && gitbook serve"
  }
}

You can view the book locally by running the command below which starts up a server running on port 4000
$ npm run docs:watch

Commit the contents to your git repo
</pre>