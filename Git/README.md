https://academind.com/learn/web-dev/git-the-basics/

### Git
-   Repositories, Branches & Commits
- Local version control
_Repository_ where code is stored
    |
    v
_Branch_"Folder"_ within repository containing commits  
    |
    v
_Commits_ Different stages of code in branch

Create project folder
mkdir ~/desired/directory
cd ~/desired/directory
~/desired/directory $
1. Create local git repository
    $ git init    
    > Initialized empty Git repository in ~/desired/directory.git  
2. Add change
    $ git add .
    > 
    2.1 Instead of all files, do by name
    git add some_file_name t
3. See what is staged
    $ git status
    > No commits yet
    Changes to be commited:
    ...  
4. Commit change
    $ git commit -m "Give commit a name"
    > git config --global user.email ...  
5. Running status shows nothing to commit
    $ git status
    > git commit --amend --reset-author
    ...
    nothing to commit, working tree clean
6. To view branch
    $ git branch  
    > * master  
7.  After editing file(s)
    $ git add .
    >  
8. Commit change
    $ git commit -m "State change made"  
        > git config --global user.email ...  
        
So far:
    Repository
    ----------
    | Master |
    ----------
  Commit 1 *
           |
           |
  Commit 2 *

9. Check git log
    $ git log 
    > commit de2b1fbd65a3575270b799748cb5f52e06a37aff (HEAD -> master)
    Author: HNSS-US <james@T420>
    Date:   Mon Sep 23 19:25:51 2019 -0400

    State change made //Note: from step 8

    commit 81199ea42573fd9d86d166e129634b6907be9b0e
    Author: HNSS-US <james@T420>
    Date:   Mon Sep 23 15:16:30 2019 -0400
    :

    Give commit a name //Note: from step 4
//Type q to exit

10. Here, removed files
     <pre><font color="#8AE234"><b>es@T420</b></font> <font color="#729FCF"><b>~/DelTech/HIS/HIS111 $</b></font> ls -ltr
     total 60
     drwxrwxr-x 2 james james  4096 Sep 14 12:25 <font color="#729FCF"><b>Zip_Files</b></font>
     drwxrwxr-x 2 james james  4096 Sep 14 12:25 <font color="#729FCF"><b>Papers</b></font>
     drwxrwxr-x 2 james james  4096 Sep 16 20:17 <font color="#729FCF"><b>TestNotes</b></font>
     drwxr-xr-x 2 james james  4096 Sep 16 22:39 <font color="#729FCF"><b>HISTTestBank</b></font>
     drwxrwxr-x 8 james james  4096 Sep 18 12:28 <font color="#729FCF"><b>Assignments</b></font>
     drwxr-xr-x 2 james james 12288 Sep 18 12:28 <font color="#729FCF"><b>HISTSummary</b></font>
     -rw-rw-r-- 1 james james 16752 Sep 23 22:54 GuidelinesAndRubricForOnlineDiscussionBoards.docx
     <font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/HIS/HIS111 $</b></font> 
     </pre>

     $ rm  GuidelinesAndRubricForOnlineDiscussionBoards.docx
     $ git add .
     $ git commit -m "removed files"
     > On branch master
       Changes not staged for commit:
	   deleted:    GuidelinesAndRubricForOnlineDiscussionBoards.docx

       no changes added to commit  
     $ git add .
     >  
     $ ls -ltr
     <pre><font color="#8AE234"><b>es@T420</b></font> <font color="#729FCF"><b>~/DelTech/HIS/HIS111 $</b></font> ls -ltr
     total 60
     drwxrwxr-x 2 james james  4096 Sep 14 12:25 <font color="#729FCF"><b>Zip_Files</b></font>
     drwxrwxr-x 2 james james  4096 Sep 14 12:25 <font color="#729FCF"><b>Papers</b></font>
     drwxrwxr-x 2 james james  4096 Sep 16 20:17 <font color="#729FCF"><b>TestNotes</b></font>
     drwxr-xr-x 2 james james  4096 Sep 16 22:39 <font color="#729FCF"><b>HISTTestBank</b></font>
     drwxrwxr-x 8 james james  4096 Sep 18 12:28 <font color="#729FCF"><b>Assignments</b></font>
     drwxr-xr-x 2 james james 12288 Sep 18 12:28 <font color="#729FCF"><b>HISTSummary</b></font>
     <font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/HIS/HIS111 $</b></font> 
     </pre>     
     
11. Here, added test file
     $ touch test_file.tst
     $ git add .
     $ git commit -m "added test file"
     $ git log
     <pre><font color="#C4A000">commit 7470569374a52560acfcdbe501d7a4446c7fb803 (</font><font color="#34E2E2"><b>HEAD -&gt; </b></font><font color="#8AE234"><b>master</b></font><font color="#C4A000">)</font>
     Author: HNSS-US &lt;james@T420&gt;
     Date:   Mon Sep 23 22:35:48 2019 -0400
     
         added test file
     
     <font color="#C4A000">commit de2b1fbd65a3575270b799748cb5f52e06a37aff</font>
     Author: HNSS-US &lt;james@T420&gt;
     Date:   Mon Sep 23 19:25:51 2019 -0400
     
         added text
     
     <font color="#C4A000">commit 81199ea42573fd9d86d166e129634b6907be9b0e</font>
     Author: HNSS-US &lt;james@T420&gt;
     Date:   Mon Sep 23 15:16:30 2019 -0400
     
         start
     </pre>     
         
So far:
    Repository
    ----------
    | Master |
    ----------
  Commit 1 *  (start)
           |
           |
  Commit 2 *  (added text)
           |
           |
  Commit 3 *  (added test file)
     
** Note: Git does not make copies of files, only the changes **
Therefore, in the statement (HEAD -> master) the last 
commit is the HEAD. To go back to previous state.  
1. Get list of commits 
    $ git log
     <pre><font color="#C4A000">commit 7470569374a52560acfcdbe501d7a4446c7fb803 (</font><font color="#34E2E2"><b>HEAD -&gt; </b></font><font color="#8AE234"><b>master</b></font><font color="#C4A000">)</font>
     Author: HNSS-US &lt;james@T420&gt;
     Date:   Mon Sep 23 22:35:48 2019 -0400
     
         added test file
     
     <font color="#C4A000">commit de2b1fbd65a3575270b799748cb5f52e06a37aff</font>
     Author: HNSS-US &lt;james@T420&gt;
     Date:   Mon Sep 23 19:25:51 2019 -0400
     
         added text
     
     <font color="#C4A000">commit 81199ea42573fd9d86d166e129634b6907be9b0e</font>
     Author: HNSS-US &lt;james@T420&gt;
     Date:   Mon Sep 23 15:16:30 2019 -0400
     
         start
     </pre>   
2. To go back 
    get checkout -b <new-branch-name>
    $ git checkout de2b1fbd65a3575270b799748cb5f52e06a37aff
    > HEAD is now at 81199ea start
    $ ls -ltr
    <pre><font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/HIS/HIS111 $</b></font> ls -ltr
    total 60
    drwxrwxr-x 2 james james  4096 Sep 14 12:25 <font color="#729FCF"><b>Zip_Files</b></font>
    drwxrwxr-x 2 james james  4096 Sep 14 12:25 <font color="#729FCF"><b>Papers</b></font>
    drwxrwxr-x 2 james james  4096 Sep 16 20:17 <font color="#729FCF"><b>TestNotes</b></font>
    drwxr-xr-x 2 james james  4096 Sep 16 22:39 <font color="#729FCF"><b>HISTTestBank</b></font>
    drwxrwxr-x 8 james james  4096 Sep 18 12:28 <font color="#729FCF"><b>Assignments</b></font>
    drwxr-xr-x 2 james james 12288 Sep 18 12:28 <font color="#729FCF"><b>HISTSummary</b></font>
    -rw-rw-r-- 1 james james 16752 Sep 23 22:54 GuidelinesAndRubricForOnlineDiscussionBoards.docx
    <font color="#8AE234"><b>james@T420</b></font> <font color="#729FCF"><b>~/DelTech/HIS/HIS111 $</b></font> 
    </pre>
    Deleted file is back and Repository is at Commit 2
    
    Repository
    ----------
    | Master |
    ----------
  Commit 1 *  (start)
           |
           |
  Commit 2 *  (added text)
