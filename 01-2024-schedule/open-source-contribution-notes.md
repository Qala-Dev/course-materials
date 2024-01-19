# Open source contribution notes

## The crux of modern open source projects

The tragedy of the commons relates to to the self-interest of individuals with unhindered access to a common resource who cause the depletion of that resource. In the world of open source software, that common resource takes on many forms. It could be the limited number of maintainers and reviewers for contributors, the lack of people willing to contribute, but many users in the community making feature requests, and so on. These days it also includes funding of the actual software project itself. An open source tool may be consumed by multinational enterprises, but only funded by a select few community members and perhaps smaller companies.

A decent lay-of-the-land when it comes to the social and economical story of open source software can be found in Nadia Eghbal's [_Working in Public: The Making and Maintenance of Open Source Software_](https://www.goodreads.com/book/show/54216469-working-in-public)

## Etiquette

### There are no dumb questions, but there are repeated ones

If you're about to ask a question on any sort of community forum, please ensure you've made some effort in the following way:

* You've searched the forum and web _properly_. Search can be a powerful tool and you'll need to learn how to use it effectively. General programming questions which are very likely to have been already answered on StackOverflow or within the language's documentation, should not be asked on community forums. It's just noisy. Use the power of search by quoting parts of errors to find exact matches, use filters provided by GitHub. It's very likely you're not the first asking the question. This is one way to ensure we don't deplete the resources of the commons.
* You've spent enough time trying to figure out the solution yourself. If you ask for assistance before you've struggled through a problem for some time, you're not going to retain that experience and remember it for when the problem comes about again.
* Maintainers and fellow contributors are humans. Don't expect an immediate reply and always be courteous (this isn't a Twitter thread). While waiting for a reply, try working on something else or you could even try researching your problem even further.

### Code of conduct

Ensure that you always read a project's code of conduct if one is present. Often, these will be very similar, for example, in the Rust community, there is a lot of _borrowing_ (pun intended) of the Rust Language project's Code of Conduct going on.

NOTE: If you're a good and genuine person who communicates in a respectful manner and keeps discussion away from personal traits, you will ace basically any code of conduct.

For projects that don't have a code of conduct, refer to NOTE above.

### Contributing Guidelines

These guidelines are what standardize the way we work on a project. You are coming to a project that you are new to. It's not going to go down well if you try to force your opinions on style and Git workflow. Discussions around these can definitely be had in GitHub issues to update the guidelines over time, but while contributing, stick to the prescribed guidelines and things will go smoothly.

## Git style

### Good messages

Writing good commit messages takes practice. So if you've been merging in garbage commits like "fix 1", "more updates", "fix 3", take note that these are not helpful at all to open source projects. I'd even say that unless your project is a throwaway toy, never make commits on shared history like this. I'd go further to say that for practice, you should ideally never ever make commits like these on shared history, even for throwaway toys.

Here are some good write-ups on some generally accepted best practices:

https://cbea.ms/git-commit/ https://www.conventionalcommits.org/en/v1.0.0/

## Review

Reviewing in open source projects is almost always the main bottleneck of development. Everyone wants to push code, but who will review? Review is actually an incredibly powerful way to understand more of the project over time. Good quality review is always highly appreciated, and the ability to do good quality review comes with time and built-up experience.

See: https://conventionalcomments.org/
