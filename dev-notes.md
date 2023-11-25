# Development Notes file for the Excursion OPP
202311091000
------------
## reStart following the directions point by point
Existing stuff moved to folder OPP-Excursion-saved

### Point One - Getting started  *done*
Redline and design mocks copied from ...-saved

### Point  Two - create project directory *done*
new directory 'excursion' created in ~/projects/Codecademy/OPP-Excursion
Note: Thought about renaming the repo on GH to something like 'excursion-saved' but reading the docs here:
https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository
'Warning: If you create a new repository under your account in the future, do not reuse the original name of the renamed repository. If you do, redirects to the renamed repository will no longer work.'
... it looks like this will be messy in the extreme. Best just delete it and start again. I wouldn't normally do that but this is a special case. I saved the code locally so that I didn't lose stuff I'd already had to think through. The remote repo is different though.
HA! but I can archive it ... will that work? Nah, that's probably worse.

### Point Three - create files *done*
Note: make sure the files are created in the correct directories.

### Point Four - initialise git repo *done*

### Point Five - commit files *done*

### Point Six - create remote repo *done*
Named the repo excursion per instructions but how about 'symmetrical-eureka' instead?
Note: the ' ... instructions to add an existing Git repository ...' are not on the screen where you create the repo. The instructions to follow are on the next screen under the heading '…or push an existing repository from the command line'.
Note: you may be asked to authenticate; that is outside the scope of these notes
Q: is it somewhere in an earlier Cc lesson on this skill path?
Q: will my changes to this file post commit be included in what I push? I doubt it.
Followed instructions as above.
No, the recent changes are not included.
Note/Word-to-the-Wise: the git repo is a set of links to local files on your development box [aka 'machine', i.e. your computer]. The stuff in your local repo is no more backed up than the files you edit. Pushing to remote, however, does create another copy of the files.
Aside - a note about git since that's a big part of this lesson:
git tracks changes to your files so it won't 'git add <file> if <file> hasn't changed ... neat, huh?
Note: the site isn't available by default. You have to specify the source. see here:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

### Point Seven - add boilerplate code *done*
Since we're doing this by the book I'm starting from scratch with boilerplate. I'll add in stuff from what I did the first time round though.

### Point Eight - commit initial coding *done*
Add command is
git add <file>
or git add .
	will add everything

Commit command is
git commit -m "<commit message>"

Push command is
git push -u origin main

Note: This page reverses the norm of black text on a white background. Try setting CSS rules color: white and background-color: black before you do anything else.

### Points Nine to Eleven *done*

### Point Twelve - add footer *done*

### Point Thirteen - wrapping up



202311083400
------------
## Wrap up from first attempt
index.html not showing issue
Here's the answer:
https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site
This is a GitHub Pages (GHP) site so the source has to be set.
Now it's time to go back over the instructions and follow step by step instead of jumping ahead/about/around/&c.
----------------------------------------------
20231125043000
--------------
btw: loving the name congenial-pancake; haven't I got one called ubiquitous-pancake? Seems GH like their pancakes ... with maple syrup? ... expecially on a Tuesday?
Now they're offering congenial-chainsaw ...ouch!
Description text:
Codecademy OPP-Excursion project
At Point Six:
Follow the instructions to add an existing Git repository, since you have already initialized yours on your own computer.
I didn't find any such instructions on the GH home page. Searched
docs.github.com
for
"add existing repo"
Found
Adding locally hosted code to GitHub
Note to use git (instead of the gh CLI) you have to authenticate first.
Or jubilant-enigma?
So, now we have a message
To https://github.com/mcnairsa/excursion.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
All looks good, right? Only problem is we're using the *nasty* name for the main branch. How do we change that?
PS: the authentication thing mentioned in the docs article didn't happen. We must be still authorised. Are we happy with that?
From Stack Overflow
https://stackoverflow.com/questions/67543278/git-how-to-change-default-branch-for-everything-i-do
via ddg
I have to change my ~.gitconfig
to add
Currently it looks like this: 
sam@Sams-MBP ~ % cat .gitconfig
# This is Git's per-user configuration file.
[user]
# Please adapt and uncomment the following lines:
	name = Sam McNair
	email = sam@Sams-MacBook-Pro.local
sam@Sams-MBP ~ % 
Do I want to change
	email = sam@Sams-MacBook-Pro.local
to
	email = mcnairsa@gmail.com
?
Probably not that just yet but to something like
Sam.McNair@mcnairs.net
or
sam@[or Sam.McNair@]themetaproject.dev
btw: possible domain names include:
themetaproject.dev
thetestingtimes.com/net/org/dev/whatever
And I really ought to be using vi/vim or nano ... (pico?)
but I used the cl instruction
git config --global init.defaultBranch main
instead.
Note: the dates ('yesterday') of the commits are from my *local* repo, not the date I created the repo on GH. Makes sense.
No README.md yet since this file isn't tracked. I know this because VSC is telling me it's not tracked. Probably want to change this to another name and created a README.md that makes more sense.
Renamed 'master' to 'main' on GH. GH v helpfully offered me this:
git branch -m main <BRANCH>
git fetch origin
git branch -u origin/main main
git remote set-head origin -a
I obvs have to change <BRANCH> TO master
Oops! no...
It's the other way around. They're assuming it's currently called main. <BRANCH> is the *to* not the *from*.
...
sam@Sams-MBP OPP-Excursion % git remote set-head origin -a
origin/HEAD set to main
sam@Sams-MBP OPP-Excursion % git branch
* main
sam@Sams-MBP OPP-Excursion %                              
K! now we're good to go.
And when I go back to the main page for the repo it tells me about the change and offers me that block of code again. I'm liking this more and more. Feels like the world has my back.
HaHaHa!
Not seeing the project live (Point Eleven). I didn't do stuff in the order they say in the instructions. Next step is to delete (or archive? if I archive on GH will the name 'excursion' become available again?) back to where I diverged and follow their instructions more closely/precisely. Obvs going to save/archive the stuff I've done locally.