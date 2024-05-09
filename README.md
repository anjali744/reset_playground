Git reset and revert

    Create a new folder somewhere in your computer, named reset_playground;
    Start a git repository inside reset_playground (make sure you are not inside a git repo before you create it!!!)
    Create a file named countries.txt, commit your changes.
    Add a country name to countries.txt and commit your changes. Repeat this 5 times, so that at the end you have 5 country names in your countries.txt file and a commit for each.
    Create a new branch named feature/more_countries, move to it.
    Create a new file, named more_countries.txt, add the name of 2 countries to that file and commit your changes.
    Go back to master.
    Use git cherry-pick <commit_hash> to get the commit where you created the file more_countries.txt into your master branch (you need to get the commit hash by doing git log when you are in the branch feature/more_countries).
    In the file countries.txt, add one more country, and commit your changes.
    Again, in the file countries.txt, add one more country, and commit your changes.
    Remove the latest commit you did using git reset --soft <commit_hash>
    Either commit or stash the changes from the last step.
    Use git revert <commit_hash> to revert the commit that you cherry picked from the branch feature/more_countries, the one where the file more_countries.txt was added (get the commit hash by doing git log and looking for the commit you want).
    Use git reset --mixed <commit_hash> to get rid of the last 2 commits.
    Either commit or stash the changes from the last step.
    Use git checkout <commit_hash> to check what your repo looked like after your first commit.
    Now go back to your latest commit using git checkout master.
    Finally, use git revert <commit_hash> to revert the commit where you added country number 3. Most likely you will get a conflict and you must solve it.
