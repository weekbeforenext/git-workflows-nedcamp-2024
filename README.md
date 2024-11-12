# Introduction to Agile and Git Workflows for Web Developers
This project was created for the *Introduction to Agile and Git Workflows for Web Developers* training.

[Story links](stories/README.md)

* [Create a Feature Branch](#create-a-feature-branch)
* [Create a Pull Request](#create-a-pull-request)
* [Request a Review](#request-a-review)
* [Review a Pull Request](#review-a-pull-request)
* [Resolve Merge Conflicts](#resolve-merge-conflicts)

## Getting Started
* [Setting your username in Git](https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git)
* [Setting your commit email address in Git - Setting your email address for a single repository](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address#setting-your-email-address-for-a-single-repository)

## Resources
* [Set up Git](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git)
* [GitHub: Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [Story Prompts](#story-prompts)

## Create a Feature Branch
1. When starting a issue, use these commands to create an issue feature branch:

    ```
    git checkout develop
    git pull
    git checkout -b feature/<github-username>/<issue-number>--<short-description-of-issue>
    ```
2. Complete your issue task.
3. When your changes are ready, use the following to review your file changes:

    ```
    git status
    ```

3. Use the following commands to stage your changes:

    New files:
    ```
    git add <path/to/file>
    ```

    Existing files:
    ```
    git add -p
    ```
    [Interactive mode with patch subcommands](https://git-scm.com/docs/git-add#Documentation/git-add.txt--p) will allow you to review each change and intentionally stage it with  [patch subcommands](https://git-scm.com/docs/git-add#Documentation/git-add.txt--p).
4. Once everything is staged, run the following command to commit your changes to your feature branch:

    ```
    git commit -m "<issue-number>: <short-description-of-changes>."
    ```
    Including the issue number in your commit comes in really handy when a developer needs to track down why particular changes were made. This is also why issue comments and documentation are important.
5. Now that changes are committed, you can push them to GitHub using this command:

    ```
    git push -u origin <feature-branch>
    ```

## Create a Pull Request
Pull requests are how you merge your feature branches into the `develop` working branch. It also allows your work to be reviewed by a mentor or team member before it merges.
- [Creating a pull request (GitHub)](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)

Just be sure to set your "base" to `develop` and "compare" to your feature branch.

## Request a Review
1. Update your issue:
    1. Remove yourself from "Assignees".
    2. Assign to your partner or a teammate.
    3. Set "Status" to "Review".
2. Assign the Pull Request to the partner or teammate.

## Review a Pull Request
1. Verify the target branch is `develop`.
2. Verify there are no merge conflicts.
3. Click on the "Files changed" tab to review the changes.
    1. Verify the changes do not violate the event's Code of Conduct.
    2. Verify the Acceptance Criteria of the issue has been met.
    3. Verify there are minimal grammatical or syntax errors.
        * It is probably helpful to click on the feature branch, navigate to the changed file, and verify it renders as expected.

### Review Pass
1. Click on the "Review changes" button.
    1. Leave a positive comment.
    2. Select "Approve".
    3. Click on the "Submit review" button.
2. Merge the Pull Request.
2. Update the related issue:
    1. Remove yourself from "Assignees".
    2. Assign back to the original assignee.
    3. Set "Status" to "Done".

### Review Fail
1. Leave a comment in the "Files changed", kindly suggesting changes.
2. Click on the "Review changes" button.
    1. Leave a kind comment, indicating you've completed your review and are requesting changes.
    2. Select "Comment" or "Request changes".
    3. Click on the "Submit review" button.
3. Update the related issue:
    1. Remove yourself from "Assignees".
    2. Assign back to the original assignee.
    2. Set "Status" to "To do".

## Resolve Merge Conflicts
1. Checkout the `develop` branch.

    ```
    git checkout develop
    ```
2. Pull the latest changes from the remote repository.

    ```
    git pull
    ```
3. Checkout your feature branch.

    ```
    git checkout <feature-branch>
    ```
4. Merge `develop` into your feature branch.

    ```
    git merge develop
    ```
5. Use your code editor's conflict resolution tool to resolve the conflicts.
    * [Visual Studio Code](https://code.visualstudio.com/docs/sourcecontrol/overview#_merge-conflicts)
    * [PhpStorm](https://www.jetbrains.com/help/phpstorm/resolving-conflicts.html#distributed-version-control-systems)
6. Verify all of the changes are staged.

    ```
    git status
    ```
7. Commit the merged changes.

    ```
    git commit --no-edit
    ```
8. Push your feature branch to the remote repository.

    ```
    git push origin <feature-branch>
    ```

## Story Prompts
1. A road trip was just the thing for me and my friends.
2. I suddenly found out that I was heir to a throne...
3. She opened the letter and it said she’d won $100,000.
4. It all started when I accidentally picked up the wrong suitcase at the airport.
5. It sounded like piano music and it was coming from my living room...
6. She broke open the fortune cookie, but there was a map on the tiny slip of paper.
7. Every Tuesday at 3 pm, flowers were delivered to my house.
8. I had to go on stage in 15 minutes and my clothes were ripped and muddy.
9. When she looked at her cellphone, she was shocked to see she had 33 voicemails.
10. When I heard that familiar jingle coming down the street, I assumed it was the ice cream truck; I never knew they had mobile deliveries of those.
11. “Don’t look at me, I thought we were going for tacos.”
12. Late for work, I throw open the front door and find myself face-to-face with a UPS driver standing next to the biggest box I’ve ever seen.
13. Mark’s favorite band is playing a sold-out show tonight but thankfully, he's figured out a way to get in.
14. “Pick a number, any number,” she said, her voice a taunt, “And I’ll show you your future self.”
15. Though Tom knew the dog was special, he'd never realized he was magical.
16. The return address on the gold envelope is in Greenland — had they really tracked me down from the other side of the world?
17. “Does this purple shirt make me stand out?” asked the giant one-eyed cat.
18. She’d eaten a lot of pie during her career as a restaurant critic, but never before had she tasted one quite like this.
19. At first, I had thought telepathy would be a cool superpower, but that was before I knew of the chaos that lives in every person’s mind.
20. I had just finished crocheting the small grey elephant for my nephew and was placing it in a gift bag when it let out a little trumpeting noise.
21. She was on the hunt for a way to ease her anxiety, and it didn’t take her long to discover that goat yoga was not the answer.
22. I had no idea how big a polar bear’s stomach really was until I was inside of one.
23. "Surprise!" They cried, leaping out from behind the door...
24. Oliver couldn’t believe he was finally here...
25. Whatever that object in the sky was, it was becoming increasingly clear that only I could see it...
26. People say that dragons aren’t real, but I know better...
27. If I’d never learned to time travel, none of this would have happened...
28. The day I got my pet cat was also the day the trouble began...
29. I woke with a jolt and glanced at the clock. With a groan, I realised I’d overslept again...
30. I was tired of living with my name. I decided it was time to change my name to something I really liked…
