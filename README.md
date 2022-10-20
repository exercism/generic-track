# Request a new Exercism language track

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

## It doesn't exist - I want to create it!

Awesome!! Please open a [new issue][new-issue], filling out the template.
We'll take a look!

## How to improve the process for the next new maintainer

It is crucial that we improve the documentation and instructions for launching a track.
The best people to discover issues with our current process are new maintainers, launching a track for the first time.
Unfortunately, that's the worst possible time for them to fix the documentation, because they've got the least amount of knowledge about how Exercism is put together.

The files in this repository serve as a template for a new track.
Some files get edited and added to the track, others are used to [create new issues in the track][issue-templates], but are not added to the new repository.
If new maintainers have questions, it will often be because these files are confusing or missing information.

When that happens we should tweak the documentation for clarity in a new pull request to the request-new-language-track repository (not their repository) and tag the maintainer to review it.
If it is still confusing, they will know, and figuring out how to explain it will help us fix it.

In some cases, we might discover that we're missing high-level documentation that should live in the [docs][docs] repo, in which case we should open an issue or pull request there, proposing the new documentation.
Tag the new maintainer there, as well, to get their input on the new docs.

---

# Notes

**Only owners of the organization can create new repositories.**

## How to bootstrap a new track

### One-time setup

1. Install [hub][].
1. Clone the [request-new-language-track][] repository.

### Bootstrap a Track

1. Add the "new track" label.
1. Confirm maintainer

   - If the requestor is volunteering, that's fine.
   - If the requestor is volunteering someone else for the job, confirm with that person.
   - If there is no maintainer, label with "needs maintainer"

1. Run `bin/bootstrap`
1. Let the requestor/maintainer know that the repo is ready for them, and point them to the launch checklist issue.

[request-new-language-track]: https://github.com/exercism/request-new-language-track
[hub]: http://github.com/github/hub
[track-repositories]: https://github.com/search?q=topic%3Aexercism-track+org%3Aexercism+fork%3Atrue&type=repositories
[exercism-tracks]: https://exercism.org/tracks
[this-repo-issues]: https://github.com/exercism/request-new-language-track/issues
[new-issue]: https://github.com/exercism/request-new-language-track/issues/new
[docs]: https://github.com/exercism/docs
[issue-templates]: https://github.com/exercism/request-new-language-track/blob/main/bin/bootstrap#L67-L73
