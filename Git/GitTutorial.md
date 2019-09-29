#### Git Tutorial for Beginners - Crash Course 
##### Table of contents
1. [Introduction](#introduction)  
2. [Steps](#steps)   
3. Trobule shooting  
   3.1 [File was deleted via command line](#TS1)  
       Changes not staged for commit:

**1. Introduction**  <a name="introduction"></a>
I used this video as reference source. However, I start with
an existing directory structure and add that to Git. Then, I work on
just one file.

<a href="https://www.youtube.com/watch?v=_OZVJpLHUaI
" target="_blank"><img src="http://img.youtube.com/vi/_OZVJpLHUaI/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>  

**2. Goal Create Git Repository for all my classes at Del Tech**  
The following is copied and pasted from my terminal. I am showing  
the command entered and then the result. Note, I am repeating commands
only to see the changes and not as part of the process.  
**Steps <a name="steps"></a>
**2.1 Current directory structure**  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> ls -alF
total 120
drwxrwxr-x  5 james james  4096 Sep 26 16:22 <font color="#729FCF"><b>.</b></font>/
drwx------ 59 james james 20480 Sep 26 10:47 <font color="#729FCF"><b>..</b></font>/
-rw-rw-r--  1 james james   820 Sep  1 18:17 ConfigureDTCCUsersWiFi.md
drwxrwxr-x  5 james james  4096 Sep 23 21:57 <font color="#729FCF"><b>CSC</b></font>/
drwxrwxr-x  3 james james  4096 Sep  1 21:48 <font color="#729FCF"><b>HIS</b></font>/
-rw-rw-r--  1 james james 65285 Sep  3 07:22 README.md
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  
**2.2 Create local git repository**  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git init
Initialized empty Git repository in /home/james/DelTech/.git/
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font></pre>  
*(Notice: A new directory ".git" is created*)*
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> ls -alF
total 120
drwxrwxr-x  5 james james  4096 Sep 26 16:22 <font color="#729FCF"><b>.</b></font>/
drwx------ 59 james james 20480 Sep 26 10:47 <font color="#729FCF"><b>..</b></font>/
-rw-rw-r--  1 james james   820 Sep  1 18:17 ConfigureDTCCUsersWiFi.md
drwxrwxr-x  5 james james  4096 Sep 23 21:57 <font color="#729FCF"><b>CSC</b></font>/
drwxrwxr-x  7 james james  4096 Sep 26 16:25 <font color="#729FCF"><b>.git</b></font>/
drwxrwxr-x  3 james james  4096 Sep  1 21:48 <font color="#729FCF"><b>HIS</b></font>/
-rw-rw-r--  1 james james 65285 Sep  3 07:22 README.md
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>
**2.3 Checking status of Git Repository**    
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git status
On branch master  
No commits yet  
Untracked files:  
  (use &quot;git add &lt;file&gt;...&quot; to include in what will be committed)  
	<font color="#CC0000">CSC/</font>  
	<font color="#CC0000">ConfigureDTCCUsersWiFi.md</font>  
	<font color="#CC0000">HIS/</font>  
	<font color="#CC0000">README.md</font>  
nothing added to commit but untracked files present (use &quot;git add&quot; to track)  
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font>   
</pre>  
**2.4 Checking status of log** 
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git log
fatal: your current branch &apos;master&apos; does not have any commits yet
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> </pre>
**2.5 Now adding changes**  
*(Notice: There is no response after running this command. Also, I had a lot of files 
and this took a few seconds. Here the ".", adds everything in the directory and below to git.)*  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git add .
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> </pre>  
**2.6 Repeating *git log* and *git status* is the same as before.**  
**2.7 Commiting to Git with "comment"**  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git commit -m &quot;creation of git&quot;
[master (root-commit) 3f2d714] creation of git
 159 files changed, 179954 insertions(+)
 create mode 100644 CSC/CSC114/Assignment0/Assignment0.odt
 create mode 100644 CSC/CSC114/Assignment0/CSC114Assignment0_Ethics.pdf
 create mode 100644 CSC/CSC114/Assignment1/.vscode/tasks.json
 create mode 100644 CSC/CSC114/Assignment1/Assignment1.zip
 .
 .
 .
 create mode 100644 HIS/HIS111/Zip_Files/HIST, Comprehensive 5th Edition by Kevin M. Schultz sm.zip
 create mode 100644 HIS/HIS111/Zip_Files/HIST, Comprehensive 5th Edition by Kevin M. Schultz_test_bank.zip
 create mode 100644 README.md
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  
**2.8 Checking status of log**  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git log
<font color="#C4A000">commit 3f2d714968fcb87dfc13d008fa0ca2f813c1623c (</font><font color="#34E2E2"><b>HEAD -&gt; </b></font><font color="#8AE234"><b>master</b></font><font color="#C4A000">)</font>
Author: HNSS-US &lt;james@T420&gt;
Date:   Thu Sep 26 18:51:48 2019 -0400

    creation of git
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font></pre>  
**2.9 Check Status**  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git status
On branch master
nothing to commit, working tree clean
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  
**2.10 Git branch diagram**  
The following diagram shows what we have 
done and what we are about to do  
Git branching:  
![git branch](https://guides.github.com/activities/hello-world/branching.png "Git Branch Image")  
**2.11 Working with one file**

### 3 Trobule shooting  
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
