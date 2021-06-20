# Gitbash
Technology required:
* Gitbash

## Setting up Gitbash
1. Install gitbash

## Gitbash commands
1. Clone branch
    ```
    git clone: 'url copy from github.com'
	
	Example:
		>>> git clone: https://github.com/George-Eliot-Archive/gearchive-theme.git
    ```

2. Make separate branch
	```
	git checkout -b 'new branch name & directory'
	
	Example:
		>>> git checkout -b Note_Jeff
	```

3. Check & Add & Commit changes I made (three steps I must follow)
	(a) Check changes I made:
	```
	git status
	```
	(b) Check differences to original branch:
	```
	git diff
	```
	(c) Add Changed files:
	```
	git add fileDirectory
	```
	(d) commit added files:
	```
	git commit
	```
	Note: 	After 'git commit', you will be into a new page indicating commit message.
			You can write by typing and escape the commit by pressing
				'esc' ==> type ':wq'
	

4. Push new branch
	```
	git push 'new branch name'
	```
	>>> The console will return line of saying setting an upstream
	```
	git push 'Note_Jeff'
		>>>console: git push --set-upstream origin Note_Jeff
	git push --set-upstream origin Note_Jeff
	```

5. Push branch (those branch already been created)
	Use this when you made changes to your local branch already been pushed.
	```
	git push branch_name
	```
	Note: Always remeber, whenever you made changes, you must go through "step 3"