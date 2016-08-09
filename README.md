# hg_hook_check_php_syntax

I use it to check php syntax on 'hg st' command.
Here is my my hgrc file:

```
[hooks]
pre-status = \
	echo "\n======================\n" \
	"CURRENT BRANCH IS:" \
	`hg branch` \
	"\n======================\n" \
	`~/bin/check_php_syntax`
```

Firstly I check what is the current branch.

Then I call check_php_syntax shell file to check php syntax of all changed php files. 
