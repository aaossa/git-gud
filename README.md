# git-gud

A simple git commit checker. I often use a commit message template I created a while ago, and I wanted to make sure that everything was in the right place after writing a commit, that's why this script exists. Use it if you want to *git gud* too. To add this custom git command to git, just place the file in a folder that's in your path (a.k.a `PATH`).

### Checks

- [x] Commit author name is in a valid format ( `Antonio Ossa`)
- [x] Commit author name is the same in your config file
- [x] Commit author email is in a valid format (`aaossa@uc.cl`)
- [x] Commit author email is the same in your config file
- [x] Commit subject message uses a maximum of **50 characters**
- [x] Commit body message is not empty
- [x] Commit body message lines use a maximum of **72 characters**
- [x] Commit body message has lines with comments (i.e. not "Signed-off-by: ...")
- [x] Commit body message has a "Signed-off-by: ..." line (`Signed-off-by: Antonio Ossa <aaossa@uc.cl>`)
- [x] Commit signature is "good"

### Template

This is the template I use. You can find it as [`.gitmessage`](https://github.com/aaossa/git-gud/blob/master/.gitmessage) in this repo and install it following [these instructions](https://robots.thoughtbot.com/better-commit-messages-with-a-gitmessage-template#automation). The script assumes that you're following these conventions, but you can use your own template if you want (or none) and customize the checker too! That's why is OSS :heart::

```
# |<----  Using a Maximum Of 50 Characters  ---->|
# If this commit is applied, it will...
# Examples of imperative mood: Refactor X, Update Y, Remove Z
Subject

# |<----   Try To Limit Each Line to a Maximum Of 72 Characters   ---->|
# What/why/how was this change made?

# Any references to relevant tickets, articles, resources, etc?
# Example: GitHub issue #23

# Something more?
# Reported-by: A person or @somebody
Signed-off-by: Antonio Ossa <aaossa@uc.cl>

# (:heart: emoji? http://emoji.muan.co/)

```

### To do

- [ ] Wiki: How to use template
- [ ] Instructions: Use git-gud as custom command
- [ ] Instructions: Use git-gud as pre-commit hook
- [x] ~~Script: Allow check multiple commits (`git gud -n 10`)~~
- [x] ~~Script: Allow check on another branch (`git gud branch`)~~
- [ ] Script: Check imperative mood in subject
- [ ] Script: Add flags about output verbosity (`--full`/current, `--warn`/warnings+errors, `--error`/errors only)

### License

This software is released under the [MIT License](https://opensource.org/licenses/MIT)