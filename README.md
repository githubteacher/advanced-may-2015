### Class Material
The material for this course lives [here](https://training.github.com/kit/advanced).

### Asking Questions
Please post create an Issue in this repo and tag it with the `question` label.

### References
- [GitHub help docs](https://help.github.com)
- [Git help docs](http://git-scm.com/docs)
- [Pro Git](http://git-scm.com/book/en/v2) book
  *A thorough introduction to Git and how to use it, including a section on GitHub.*
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
	*Handy for both learning and quickly looking up Markdown syntax.*

### Show Current Branch in Terminal Prompt
If you want this:

![terminal-prompt](https://cloud.githubusercontent.com/assets/2132216/7382003/b514a288-edbe-11e4-9162-ea065519ea08.png)

you can add these lines to your `~/.bashrc` file:

```bash
# show current git branch in prompt
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\w\[\033[36m\]\$(parse_git_branch) \[\033[00m\] > "
```
