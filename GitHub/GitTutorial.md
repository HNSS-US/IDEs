# Git Tutorial for Beginners - Crash Course  
## Table of contents  
1. Introduction to [guide](#introduction)  
2. Instructions  
   2.1 synch local directory with existing repository on [Github](#synchGithub)  
   2.2 Create new repository and synch with Github [(TODO)](#newRepository)
3. Troubleshooting  
   3.1 File was deleted via command [line](#TS1)  
       error: *Changes not staged for commit:*  
4. References  
   4.1 git [website](https://git-scm.com/ "git-scm.com")  
   4.2 Pro Git [book](https://git-scm.com/book/en/v2 "ProGitBook")  
   4.3 Tower [website](https://www.git-tower.com/learn/git/ebook/en/command-line/basics/what-is-version-control#start "git-tower.com")  
   4.4 This page was built with Visual Studio using the Instant Markdown [extension](https://marketplace.visualstudio.com/items?itemName=dbankier.vscode-instant-markdown "marketplace.visualstudio.com")  

**1. Introduction**  <a name="introduction"></a>
Git is a type of version control. Version control allows you to 
store your progress in a type of "database".
(Diagram from git-tower.com)  
![etower](https://www.git-tower.com/learn/media/pages/git/ebook/en/command-line/basics/what-is-version-control/1234869142-1570000299/what-is-vcs.png "Version Control")  
The advantage to using version control is you are able to go back in time to  
see the changes made to a project. For example, you changed a program and  
want to revert back to what was done. Version controlworks whether working  
alone or in a group.  

**2.1 synch local directory with existing repository on Github** <a name="synchGithub"></a>  
I have information saved on Github, but not to a local repository.  
I am going to create the local repository to update Github. This  
pulls all the directories and files from my Github account.  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~ $</b></font> git clone https://github.com/HNSS-US/DelTech.git
Cloning into &apos;DelTech&apos;...
remote: Enumerating objects: 101, done.
remote: Counting objects: 100% (101/101), done.
remote: Compressing objects: 100% (99/99), done.
remote: Total 656 (delta 43), reused 0 (delta 0), pack-reused 555
Receiving objects: 100% (656/656), 1.00 MiB | 9.61 MiB/s, done.
Resolving deltas: 100% (278/278), done.
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~ $</b></font> </pre>  

**2.1.1  [Ignoring files](#IgnoreFiles)**  
Creating .gitignore file now. I am ignoring .pdf  
files so the textbooks are not pushed to Github.  
Those files are too large to store on Github.  

**2.1.2 Adding files and directories**  
I added the source code from the textbook to  
my DelTech repository and the .gitignore file.  

***Checking status:***  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git status
On branch master
Your branch is ahead of &apos;origin/master&apos; by 1 commit.
  (use &quot;git push&quot; to publish your local commits)

Untracked files:
  (use &quot;git add &lt;file&gt;...&quot; to include in what will be committed)

	<font color="#CC0000">.gitignore</font>
	<font color="#CC0000">CSC/CSC114/GaddisExamples/</font>

nothing added to commit but untracked files present (use &quot;git add&quot; to track)
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font>  
</pre>  
***Now to add the directory:***  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git add -vA  
add &apos;.gitignore&apos;
add &apos;CSC/CSC114/GaddisExamples/AppendixE/PrE-1.cpp&apos;
</pre>
.
.
.
<pre>add &apos;CSC/CSC114/GaddisExamples/Chapter21/Pr21-3.cpp&apos;
add &apos;CSC/CSC114/GaddisExamples/Chapter21/Pr21-4.cpp&apos;
add &apos;CSC/CSC114/GaddisExamples/Chapter21/Pr21-5.cpp&apos;
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> </pre>  

The options used for the *git add* command where:  
-v --verbose be verbose and  -A --all --no-ignore-removal  
The complete list of options is found on the git [website](https://git-scm.com/docs/git-add#_name "git-scm.com")  

***Doing a commit*** 
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git commit -m &quot;Added Gaddis directory and .gitignore&quot;
[master 964aa29] Added Gaddis directory and .gitignore
 605 files changed, 26670 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 CSC/CSC114/GaddisExamples/AppendixE/PrE-1.cpp
 create mode 100644 CSC/CSC114/GaddisExamples/AppendixE/PrE-2.cpp
</pre>
...
<pre>create mode 100644 CSC/CSC114/GaddisExamples/Chapter21/Pr21-5.cpp
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech</b></font></pre>  
***Checking status***  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git status
On branch master
Your branch is ahead of &apos;origin/master&apos; by 2 commits.
  (use &quot;git push&quot; to publish your local commits)

nothing to commit, working tree clean
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font></pre>  
**2.1.3 Pushing to Github**  
(Diagram from git-tower.com)  
![Remote Repository](https://www.git-tower.com/learn/media/pages/git/ebook/en/command-line/remote-repositories/introduction/-1045933932-1570000299/basic-remote-workflow.png "Remote Repository")  
Here, the remote repository is Github.  The command used is *git push*. This command takes two arguments:  
(a) The remote repository we want to push.  
(b) The branch on that remote repository we want to push.  

**2.1.3.1**
***Checking before push. (-v List all currently configured remotes)***
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git remote -v
origin	https://github.com/HNSS-US/DelTech.git (fetch)
origin	https://github.com/HNSS-US/DelTech.git (push)
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  
The "fetch URL" which is used for reading access.  
The "push URL", used when you want to write data to the remote.  
In many cases, both URLs are the same. However, you can also  
use this to define different URLs for read and write access  
(for security and performance reasons).  

<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git branch -va
* master                964aa29 [ahead 2] Added Gaddis directory and .gitignore
  remotes/origin/HEAD   -> origin/master
  remotes/origin/master 6390ad1 Add files via upload
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  

**This command gives the repository names.**  
**for (a) The remote repository we want to push:**  
***origin***  
**and (b) The branch on that remote repository we want to push is:**  
***master***    

This is the Github repository before git push:
![Before push](https://raw.githubusercontent.com/HNSS-US/images/master/BeforePush.jpeg "Before push")  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git push origin master
Username for &apos;https://github.com&apos;: HNSS-US
Password for &apos;https://HNSS-US@github.com&apos;: 
Counting objects: 668, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (638/638), done.
Writing objects: 100% (668/668), 250.29 KiB | 3.63 MiB/s, done.
Total 668 (delta 54), reused 0 (delta 0)
remote: Resolving deltas: 100% (54/54), completed with 3 local objects.
To https://github.com/HNSS-US/DelTech.git
   6390ad1..964aa29  master -&gt; master
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  
This is the Github repository after git push:  
![After push](https://raw.githubusercontent.com/HNSS-US/images/master/AfterPush.jpeg "After push")  
The GaddisExample directory and all 660+ files are saved to the remote repository Github.

*** TODO  New Repository *** <a name="newRepository"></a>


### 3 Troubleshooting  
**3.1 File was deleted via command line, now unable to have it sync with Git <a name="TS1"></a>  
      Changes not staged for commit:**  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/Textbooks $</b></font> rm text.txt</pre>  
##### After completing Assignment4, checked Git status
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/CSC114/Assignment4 $</b></font> git status  
On branch master  
Changes to be committed:
  (use &quot;git reset HEAD &lt;file&gt;...&quot; to unstage)
	<font color="#4E9A06">modified:   .vscode/tasks.json</font>
	<font color="#4E9A06">new file:   Assignment4.zip</font>
	<font color="#4E9A06">new file:   distance_traveled5_6</font>
	<font color="#4E9A06">modified:   distance_traveled5_6.cpp</font>
	<font color="#4E9A06">new file:   membership_fee_increase5_5</font>
	<font color="#4E9A06">modified:   membership_fee_increase5_5.cpp</font>
	<font color="#4E9A06">new file:   sum_numbers5_1</font>
	<font color="#4E9A06">modified:   sum_numbers5_1.cpp</font>
Changes not staged for commit:
  (use &quot;git add/rm &lt;file&gt;...&quot; to update what will be committed)
  (use &quot;git checkout -- &lt;file&gt;...&quot; to discard changes in working directory)

	<font color="#CC0000">deleted:    ../../Textbooks/dropped text.txt</font>

<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/CSC114/Assignment4 $</b></font></pre>  
##### Commited to 
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/CSC114/Assignment4 $</b></font> git commit -m &quot;Assignment4&quot;
[master b3aa52c] Assignment4
 8 files changed, 244 insertions(+), 82 deletions(-)
 create mode 100644 CSC/CSC114/Assignment4/Assignment4.zip
 create mode 100755 CSC/CSC114/Assignment4/distance_traveled5_6
 create mode 100755 CSC/CSC114/Assignment4/membership_fee_increase5_5
 create mode 100755 CSC/CSC114/Assignment4/sum_numbers5_1
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/CSC114/Assignment4 $</b></font></pre>  

##### Checked Git status  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/CSC114/Assignment4 $</b></font> git status
On branch master
Changes not staged for commit:
  (use &quot;git add/rm &lt;file&gt;...&quot; to update what will be committed)
  (use &quot;git checkout -- &lt;file&gt;...&quot; to discard changes in working directory)

	<font color="#CC0000">deleted:    ../../Textbooks/dropped text.txt</font>

no changes added to commit (use &quot;git add&quot; and/or &quot;git commit -a&quot;)
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/CSC114/Assignment4 $</b></font> </pre>  
##### To remove  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/Textbooks $</b></font> git add -u .
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/Textbooks $</b></font></pre>  

##### Corrected  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/Textbooks $</b></font> git status
On branch master
Changes to be committed:
  (use &quot;git reset HEAD &lt;file&gt;...&quot; to unstage)

	<font color="#4E9A06">deleted:    dropped text.txt</font>

<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/CSC/Textbooks $</b></font> 
</pre>  

##### [Back to top](#introduction)  