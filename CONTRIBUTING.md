- [Contributing to Mockito](#)
	- [Pull request criteria](#)
	- [General info](#)
	- [More on pull requests](#)

# Contributing to Mockito

## Pull request criteria

* At least one commit message in the PR contains "Fixes #id" where id is an [issue tracker](https://github.com/mockito/mockito/issues) id. This allows automated release notes generation
* Use `@since` tags for new public APIs
* Include tests
* Document public APIs with examples
* For new feautres consider adding new documentation item in main `Mockito` class
* Also, look at the [GitHub's Pull Request guide](https://github.com/blog/1943-how-to-write-the-perfect-pull-request)

## General info

* Comment on issues or pull requests
* If you know the answer to a question posted to our [mailing list](https://groups.google.com/forum/#!forum/mockito) - don't hesitate to write a reply. That helps us a lot.
* Also, don't hesitate to ask questions on the [mailing list](https://groups.google.com/forum/#!forum/mockito) - that helps us improve javadocs/FAQ.
* Please suggest changes to javadoc/exception messages when you find something unclear.
* If you miss a particular feature in Mockito - browse or ask on the mailing list, show us a sample code and describe the problem.
* Wondering what to work on? See [task/bug list](https://github.com/mockito/mockito/issues/) [(old task/bug list)](http://code.google.com/p/mockito/issues/list) and pick up something you would like to work on. Remember that some feature requests we somewhat not agree with so not everything we want to work on :)
* Mockito currently uses Github for versioning so you can *create a fork of Mockito in no time*. Go to the [github project](https://github.com/mockito/mockito) and "Create your own fork". Create a new branch, commit, ..., when you're ready let us know about your pull request so we can discuss it and merge the PR!
* Note the project now uses *gradle*, when your Gradle install is ready, make your IDE project's files (for example **`gradle idea`**). Other gradle commands are listed via **`gradle tasks`**.

## More on pull requests

As you may have noticed, Mockito has now a continuous release bot, that means that each **merged** pull request will be automatically released in a newer version of Mockito.
For that reason each pull request has to go through a thorough review / discussion.

Things we pay attention in a PR :

* On pull requests, please document the change, what it brings, what is the benefit, the issue on Google Code, etc.
* Clean commit history in the topic branch in your fork of the repository, even during review. For that matter it's possible to commit [_semantic_ changes](http://lemike-de.tumblr.com/post/79041908218/semantic-commits). Tests are an asset, so is history.
* In the code, always test your feature / change, in unit tests and in our `acceptance test suite` located in `org.mockitousage`. Older tests will be migrated when a test is modified.
* New test methods should follow a snake case convention (`ensure_that_stuff_is_doing_that`), this allows the test name to be fully expressive on intent while still readable.
* When reporting errors to the users, if it's a user report report it gently and explain how a user should deal with it, see the `Reporter` class. However not all errors should go there, some unlikely technical errors don't need to be in the `Reporter` class.
* Documentation !!! Always document with love the public API. Internals could use some love too. In all cases the code should _auto-document_ itself.



_If you are unsure about git you can have a look on our [git tips to have a clean history](https://github.com/mockito/mockito/wiki/Using git to prepare your PR to have a clean history)._

