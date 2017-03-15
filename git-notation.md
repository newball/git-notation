Git is becoming an essential tool for most development projects. It’s ability to manage changes, and the thought processes for developers has changed the way we deal with project management. One of the most annoying things about dealing with Git are the commit messages, and how confusing, unorganized, and sometimes unhelpful they can be. There’s unofficial (but widely adopted) standards (https://chris.beams.io/posts/git-commit/) and tips (https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message) about commit messages; I believe there’s a better way to indicate the type of commit that is being processes that builds on these existing standards. 

I believe commit messages should begin with a character flag indicating the type of commit that has been processed. I call this Git Notation, and suggest that the +, -, ~, !, and * symbols should be used at the beginning of a commit to indicate if what has been processed is an addition, removal, change, bug or reported fix, or comment. I believe if developers used easy to interpret notations, we can easily sort through issues, find the items that plague projects and possibly even develop a better sorting system in determining what was change, what was fixed or improved, and what was removed. 

Here are some current examples of what a few git commit messages look like in WordPress (my favorite open source platforms):

- Themes: enable browser history support in add new theme screen. https://github.com/WordPress/WordPress/commit/33286df4c10f9db9e438ded1b074a0c6463c6863
- About page: Remove `autoplay` and `loop` attributes on "Theme Starter Content", "Edit Shortcuts", and "Video Headers" videos, originally added as a part of [39512].
- REST API: Do not allow access to users from a different site in multisite. https://github.com/WordPress/WordPress/commit/eb8457d3f489e51bc457604a7744d8eb541707ae
- Taxonomy: Improve 'Parent' label when editing taxonomy terms. https://github.com/WordPress/WordPress/commit/b6572af5d227103f185e5646394644837755a694
- REST API: Fix multiple issues with setting dates of posts and comments. https://github.com/WordPress/WordPress/commit/b6ce4e283080332525bb276e2bacaf566c4a9b5c
- FINALLY https://github.com/WordPress/WordPress/commit/a939c7571a9a3f833180f83c7e084b78b26a2b83

By using my suggestion of Git Notation, these commits would look like this:

- + Themes: enable browser history support in add new theme screen. https://github.com/WordPress/WordPress/commit/33286df4c10f9db9e438ded1b074a0c6463c6863
- - About page: Remove `autoplay` and `loop` attributes on "Theme Starter Content", "Edit Shortcuts", and "Video Headers" videos, originally added as a part of [39512].
- - REST API: Do not allow access to users from a different site in multisite. https://github.com/WordPress/WordPress/commit/eb8457d3f489e51bc457604a7744d8eb541707ae
- ~ Taxonomy: Improve 'Parent' label when editing taxonomy terms. https://github.com/WordPress/WordPress/commit/b6572af5d227103f185e5646394644837755a694
- ! REST API: Fix multiple issues with setting dates of posts and comments. https://github.com/WordPress/WordPress/commit/b6ce4e283080332525bb276e2bacaf566c4a9b5c
- * FINALLY https://github.com/WordPress/WordPress/commit/a939c7571a9a3f833180f83c7e084b78b26a2b83

Now, here are the details of my recommendations:

- + (plus symbol): the plus symbol indicates an addition and can include any sort of addition such as: new features, files, functions, etc. The idea here is to indicate something has been added to the project.
- - (minus symbol): the minus symbol indicates a removal and can include any sort of removal such as: removing a feature, files, function, etc. The idea here is to indicate something has been removed from the project.
- ~ (squiggly symbol): the (squiggly) symbol indicates a change. Think of this as a combination of + and -. Often, in the development process, there are changes to code that isn’t merely an addition or a removal, it’s a new way of thinking or processing data. This is really important when a function or feature has been depreciated. This notation should be used when indicating these changes and depreciations. 
- ! (Exclamation mark): the exclamation mark indicates a fix to a bug/issue or comment. This is different than the change, as it points directly to an issue or comment that has been raised in the development process. Think of this as a way of directly responding to things that arise in the development process.
- * (star symbol): the star symbol indicates a comment. Use this to comment in a project what ever one feels is relevant. Some of these comments can be as simple as indicating the first commit or a notation that's important to the project development.

The recommendation is to use the Git Notation flag, followed by a space, taking up no more than the first two characters of a commit message. After these three characters, simply write the rest of your commit message as normal, using your preferred commit notation standards.

The aim of Git Notation is to make sorting, managing, and even committing to a repository an easier process to find, indicate and classify what is occurring during the life of a project.