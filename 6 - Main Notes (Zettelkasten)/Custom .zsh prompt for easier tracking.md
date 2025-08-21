2025-08-21 10:23

### Status: #child

### Tags: [[os]]

# What is  Custom .zsh prompt for easier tracking?

### The Why

When you're working on a project with Git, you often need to know which branch you're on. Instead of constantly typing `git branch`, this setup gives you an instant visual cue right in your terminal prompt. It's a key part of an efficient and mistake-free developer workflow.

### How to Set It Up

This process involves adding a small code snippet to your Zsh configuration file.

1. **Open your Zsh configuration file.** In your terminal, run the following command to create and open the file.
    
    `touch ~/.zshrc; open ~/.zshrc`
    
    _Note: On some systems,_ `open` _might not work. In that case, use a different text editor, like_ `nano ~/.zshrc`_._
    
2. **Add the code.** Copy and paste the entire code block below into the `.zshrc` file.
    
    `function parse_git_branch() { git branch 2> /dev/null | sed -n -e 's/^\* \(.*\)/[\1]/p' } setopt PROMPT_SUBST export PROMPT='%F{grey}%n%f %F{cyan}%~%f %F{green}$(parse_git_branch)%f %F{normal}$%f '`
    
3. **Save and apply the changes.** Save the file and close your editor. To see the new prompt, either open a new terminal window or run this command in your current one:
    
    `source ~/.zshrc`
    
    Your prompt will now show the Git branch name (e.g., `[main]`) whenever you are inside a Git repository.
    

### What the Code Does

- The `parse_git_branch` function is a mini-program that runs the `git branch` command and filters the output to extract only the name of the current branch.
    
- `setopt PROMPT_SUBST` is a special Zsh command that allows the prompt to run our `parse_git_branch` function.
    
- The final `export PROMPT` line defines the full look of your new prompt, including the username, the current directory, and the output of our Git branch function, all with custom colors.


## Descriptions





# References









