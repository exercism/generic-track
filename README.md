# Request a new Exercism language track

If you wish to request a new track, **you must post in the [Support category on the Exercism Community Forum][forum-support]** to discuss this with the team.

Before opening the post, it's worth considering:

- Is it a programming language?
- Does Exercism already support the language?
- Has anyone else asked for it?
- Will you be available to actively build and launch the track?

## Is it a programming language?

At Exercism we provide a learning platform for developers who want to practice a programming language or learn a new one.

If the language is a general purpose programming language, then we'll probably be interested in having the track on Exercism.
We do not create tracks for tools, libraries, frameworks, or technologies.

## Does Exercism already support the language?

Please [check the list of track repositories][track-repositories] to find both active and inactive tracks.
If you find a repository for your language, check the `active` key's value in the repository's `config.json` file for its status:

- `true`: the track is active and listed on the website's [tracks page][exercism-tracks].
- `false`: the track is inactive and not listed on the website.
  The track still requires work for it to become active.
  If you'd like to help out, please open an issue on that repository to say hello.

## Has someone else asked for it?

Do a search in the [issues of this repository][this-repo-issues] for the name of the language to see if the language was already requested.
Remember to check both open and closed issues.

## Will you be available to actively build and launch the track?

Exercism is a not-for-profit organization, and all the language tracks are built by volunteers.
We will only create a track if there is at least one volunteer who has offered to take the lead on building it.

The minimum to launch a track is:

- 20 practice exercises (these can be based on specifications in the [problem-specifications][] repository).
- Continuous integration that checks that the exercises can be solved.
- A bit of configuration and documentation.

We are available to guide you along the way, and you can also get help from the community of folks who have done this for other languages.

## It doesn't exist - I want to create it!

Awesome! Please create a new post in the [Exercism Forum][forum-support] so we can discuss the details.
If the new track is authorized, then create a [new-issue][] in this repository, and we'll create the new repository for the track.

---

# Instructions for Exercism Admins

**This section is not relevant for maintainers. Please do not try and bootstrap repos yourselves. It won't work. Follow the instructions above and we will sort things for you.**

## How to bootstrap a new track

### One-time setup

1. Install the [GitHub CLI][github-cli].
1. Login via `gh auth login`
1. Clone the [generic-track][] repository.

### Bootstrap a Track

1. Add the "new track" label.
1. Confirm maintainer

   - If the requestor is volunteering, that's fine.
   - If the requestor is volunteering someone else for the job, confirm with that person.

1. Run `LANGUAGE=<language> SLUG=<slug> USERNAMES=<comma,separated,list> bin/bootstrap` (e.g. `LANGUAGE="Common Lisp" SLUG="common-lisp" USERNAMES="foo,bar" bin/bootstrap`)
1. Let the requestor(s)/maintainer(s) know that the repo is ready for them, and point them to the launch checklist issue.

#### Bootstrap Test Runner (optional)

1. Open a prompt in the root of the cloned [`generic-test-runner`][generic-test-runner] repo
1. Run `LANGUAGE=<language> SLUG=<slug> bin/bootstrap.sh` (e.g. `LANGUAGE="Common Lisp" SLUG="common-lisp" bin/bootstrap.sh`)

#### Bootstrap Representer (optional)

1. Open a prompt in the root of the cloned [`generic-representer`][generic-representer] repo
1. Run `LANGUAGE=<language> SLUG=<slug> bin/bootstrap.sh` (e.g. `LANGUAGE="Common Lisp" SLUG="common-lisp" bin/bootstrap.sh`)

#### Bootstrap Analyzer (optional)

1. Open a prompt in the root of the cloned [`generic-analyzer`][generic-analyzer] repo
1. Run `LANGUAGE=<language> SLUG=<slug> bin/bootstrap.sh` (e.g. `LANGUAGE="Common Lisp" SLUG="common-lisp" bin/bootstrap.sh`)

[generic-track]: https://github.com/exercism/generic-track
[github-cli]: https://cli.github.com/
[track-repositories]: https://github.com/search?q=topic%3Aexercism-track+org%3Aexercism+fork%3Atrue&type=repositories
[exercism-tracks]: https://exercism.org/tracks
[this-repo-issues]: https://github.com/exercism/generic-track/issues
[new-issue]: https://github.com/exercism/generic-track/issues/new
[docs]: https://github.com/exercism/docs
[issue-templates]: https://github.com/exercism/generic-track/blob/main/bin/bootstrap#L67-L73
[forum-support]: https://forum.exercism.org/c/support/8
[problem-specifications]: https://github.com/exercism/problem-specifications
[generic-test-runner]: https://github.com/exercism/generic-test-runner
[generic-representer]: https://github.com/exercism/generic-representer
[generic-analyzer]: https://github.com/exercism/generic-analyzer
