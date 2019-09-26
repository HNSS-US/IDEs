#### Git Tutorial for Beginners - Crash Course 
Used this video as main source, however I start to deviat at step  

<a href="https://www.youtube.com/watch?v=_OZVJpLHUaI
" target="_blank"><img src="http://img.youtube.com/vi/_OZVJpLHUaI/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>  
**Goal Create Git Repository for all my classes at Del Tech**  
The following is copied and pasted from my terminal. I am showing  
the command entered and then the result. Note, I am repeating commands
only to see the changes and not as part of the process.
1. Current directory structure  
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
2. Create local git repository  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git init
Initialized empty Git repository in /home/james/DelTech/.git/
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font></pre>  
*New directory .git is created*  
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
3. Checking status of Git Repository  
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
4. Checking status of log  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git log
fatal: your current branch &apos;master&apos; does not have any commits yet
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> </pre>
5. Now adding changes  
*(Notice: Notice, there is no response. Also, I had a lot of files and this took a few seconds.
  this method adds everything in the directory and below to git.)*
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git add .
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> </pre>  
6. Repeat checking status    
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git status
On branch master
No commits yet
Changes to be committed:
  (use &quot;git rm --cached &lt;file&gt;...&quot; to unstage)
	<font color="#4E9A06">new file:   CSC/CSC114/Assignment0/Assignment0.odt</font>
	<font color="#4E9A06">new file:   CSC/CSC114/Assignment0/CSC114Assignment0_Ethics.pdf</font>
	<font color="#4E9A06">new file:   CSC/CSC114/Assignment1/.vscode/tasks.json</font>
	<font color="#4E9A06">new file:   CSC/CSC114/Assignment1/Assignment1.zip</font>
	<font color="#4E9A06">new file:   CSC/CSC114/Assignment1/averagevalues</font>
	.
	.
	.
</pre>  
<pre>	<font color="#4E9A06">new file:   HIS/HIS111/TestNotes/Test1_Paragraphs.txt</font>
	<font color="#4E9A06">new file:   HIS/HIS111/Zip_Files/HIST, Comprehensive 5th Edition by Kevin M. Schultz sm.zip</font>
	<font color="#4E9A06">new file:   HIS/HIS111/Zip_Files/HIST, Comprehensive 5th Edition by Kevin M. Schultz_test_bank.zip</font>
	<font color="#4E9A06">new file:   README.md</font>
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  
7. Repeat Checking log  
<pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> git log
fatal: your current branch &apos;master&apos; does not have any commits yet
<font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech $</b></font> 
</pre>  








#### GitHub Tutorial for Beginners - Crash Course  
<a href="https://www.youtube.com/watch?v=mVnZVw4KJnc
" target="_blank"><img src="http://img.youtube.com/vi/mVnZVw4KJnc/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>  
