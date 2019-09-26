#### How to delete multiples files in Github  
(* TODO *)  
The steps for doing this are:  
* In the command-line, navigate to your local repository.  
* Ensure you are in the default branch:  
> $ git checkout master  
* Remove folder  
> $ git rm -r _folder-name_ 
* Commit the change:  
> git commit -m _Remove duplicated directory_  
* Push the change to your remote repository:  
> $ git push origin master  
