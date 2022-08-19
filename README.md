# Securonix Documentation as Code

![alt text](https://www.securonix.com/wp-content/uploads/2021/12/thumbnail_logo2.jpg "Securonix Logo")

This repository contains the Documentation for Securonix API service.

## To add new content:

For adding new content to the Documentation base, please follow the steps listed below:

1. If you are accessing the repo for the first time, clone the main branch. If not, skip to step 2.
<pre><code> git clone git@github.com:securonixinc/Securonix_API_Documentation.git
</code></pre>
2. If you already have a local repo, pull the recent changes. 
<pre><code> git pull origin main
</code></pre>

3. To add documentation in markdown format:

* Add a markdown file in the exampleSite/content path in main branch to add your data. Refer to the [markdown syntax]
* Add necessary content in the markdown file
* Add images/gifs etc in the static folder


[markdown syntax]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

4. Push your changes to the main branch
<pre><code>git add .
git commit -m "Add commit message"
git remote add origin git@github.com:securonixinc/Securonix_API_Documentation.git
git push -u origin main
</code></pre>
5. After a few minutes, the information you added would be automatically reflected in the Documentation website
