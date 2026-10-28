# Wallpaper (WIP)
An opinionated list of tools and practices that any production-level Python project should have.

## Further thoughts
Uv creates the virtual environment and activates it automatically, which makes you wonder how long it'll be necessary to do so since things that are so automatic usually turn into the "fabric" or "the wallpaper" of a project - it's there but no one has to notice.

On the other hand, fine china is what you bring out when guests come over. This works for me because it reminds me of [Plumbing and Porcelain](https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain) from the [Git book](https://git-scm.com/book/en/v2). 

I was asked, during an interview, to look at some code and respond with anything that was missing. I didn't handle the question well. This is a response to that.


## Practices
The rules each project needs to adhere to.
### Code
The project should contain "just enough" code.
- Not Perl Golf.
- Not LLM bloat.

#### Logging
A sane level of logging needs to be present to allow for other humans and observability tools to know when "someone should do something" or other intervention is required.
#### Try/Except
Throw exceptions when conditions aren't correct. Log the event. Consider exiting the app.
### Project
Rules that the project needs to adhere to in order to be considered production-worthy.
#### File and module organization
The main.py is a index of functions. Unless the scope of the project can be addressed with a small tidy function, the functions should exist outside of main.py.

Files should be created to logically group related functions.

Packages should be created or utilized when the developer needs to support use-cases out of scope of the original project.

#### Conventional Commits
Commit messages should be short, easy to understand, and context-specific. See the [Conventional Commits Spec](https://www.conventionalcommits.org/en/v1.0.0/#specification) for further detail.
#### Naming convention
Filenames should be [descriptive enough](https://axioshq.com/smart-brevity) to allow the viewer to intuit it's purpose or reason for existing.

## Tools
- Version control 
  - Pre-commit Hooks (Is this a practice or a tool?)
- [uv](https://docs.astral.sh/uv/): An extremely fast Python package and project manager, written in Rust.
- [ruff](https://docs.astral.sh/ruff/): An extremely fast Python linter and code formatter, written in Rust.
- [ty](https://docs.astral.sh/ty/): An extremely fast Python type checker and language server, written in Rust.
- Testing

## Future
Should this be turned into a template of sorts? Kneejerk says no. It's a collection of ideas. It could be tests. I mean, it _should_ be tests.