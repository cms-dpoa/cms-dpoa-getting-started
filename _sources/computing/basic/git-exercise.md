# Git Exercise

Follow these instructions to add a new file or to update a file:
1.  add a shh key for git authentication (needed to upload your changes) following [the instructions link](./computing/basic/git.html)
2.  in your Linux terminal, git clone this repository `git clone git@github.com:cms-dpoa/cms-dpoa-getting-started.git`
3. change to  the `cms-dpoa-getting-started` directory in your local area
4. if  `pip` is not yet installed (check if it exists with `which pip` or `which pip3`), install `pip` following the instructions in https://linuxize.com/post/how-to-install-pip-on-ubuntu-20.04/
5. check the messages, you may need to add a directory to your PATH variable with `PATH="$PATH:$HOME/.local/bin"` so that the installed program can be found
6. run  `pip install -r requirements.txt` (or `pip3`)
7.  remove files in the existing `_build/html` directory 
8.  Run `jupyter-book build .`
9. Check your local build in your browser: if you use WSL 2 linux, you can find it in `file:///C:/Users/[USER]/[YOUR-DIRECTORY]/dpoa-getting-started/_build/html/intro.html`
10.  make a new branch `yourname-updates` or a name of your choice in your local area with `git checkout -b yourname-updates`
11. either update an existing file or make a new file with new content and add its name to `_toc.yml`
12.  build the book again and check changes
13. add the changes to git in your local area with `git add /your_new_file.md _toc.yml` in case you added a new file, or with 
`git add /your_updated_file.md` in case you upadted an existing file, and commit them `git commit -m "Updated instructions"`
14.  push the changes of your branch to the original github repository with `git push origin yourname-updates`
15. you'll see a message for your updated branch in the github web interface https://github.com/cms-dpoa/cms-dpoa-getting-started, you can make a pull request to merge your branch

