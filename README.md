# Request a new Exercism language track

## Does Exercism already support the language?

Please [check the list of track repositories](https://github.com/search?q=topic%3Aexercism-track+org%3Aexercism+fork%3Atrue&type=repositories) to find both active and inactive tracks.
If you find a repository for your language, check the `active` key's value in the repository's `config.json` file for its status:

- `true`: the track is active and listed on the website's [tracks page](https://exercism.org/tracks).
- `false`: the track is inactive and not listed on the website. The track still requires work for it to become active. If you'd like to help out, please open an issue on that repository to say hello.

## Has someone else asked for it?

Do a search in the [issues of this repository](https://github.com/exercism/request-new-language-track/issues) for the name of the language to see if the language was already requested.
Remember to check both open and closed issues.

## It doesn't exist - I want to create it!

Awesome!! Please open a [new issue](https://github.com/exercism/request-new-language-track/issues/new), filling out the template. We'll take a look!

## How to improve the process for the next new maintainer

It is crucial that we improve the documentation and instructions for launching a track. The best people to discover
issues with our current process are new maintainers, launching a track for the first time. Unfortunately,
that's the worst possible time for them to fix the documentation, because they've got the least amount of
knowledge about how Exercism is put together.

The files in this repository serve as a template for a new track. Some files get edited and added to the track,
others are used to [create new issues in the track][issue-templates], but are not added to the new repository.
If new maintainers have questions, it will often be because these files are confusing or missing information.

When that happens we should tweak the documentation for clarity in a new pull request to the request-new-language-track repository (not their repository) and tag the maintainer to review it. If it is still confusing, they will know, and figuring out how to explain it will help us fix it.

In some cases, we might discover that we're missing high-level documentation that should live in the [docs][docs]
repo, in which case we should open an issue or pull request there, proposing the new documentation.
Tag the new maintainer there, as well, to get their input on the new docs.

[docs]: https://github.com/exercism/docs
[issue-templates]: https://github.com/exercism/request-new-language-track/blob/main/bin/bootstrap#L67-L73

---

# Notes for Org Owners

## How to bootstrap a new track

**Only owners of the organization can create new repositories.**

### One-time setup

1. Install [hub][].
1. Clone the [request-new-language-track][] repository.
1. Clone the [tools][] repository.
1. Follow the instructions in the [tools README][clone-tracks] to clone all the existing tracks.
1. Create a [saved reply][saved-replies] with the following checklist:

```
- [ ] Run bootstrap script
  `TRACK_ID=<id> LANGUAGE=<language> bin/bootstrap`
  Add it as a Linux project, then switch it to OS X in _Project Settings -> Build Environment_
- [ ] Add as a submodule to [trackler][]
  `TRACK_ID=<id>; git submodule add https://github.com/exercism/$TRACK_ID tracks/$TRACK_ID`
- [ ] Create [new team][new-team] for language
- [ ] Add bootstrapped repository to team **with write access**
- [ ] Invite maintainer to team

[trackler]: https://github.com/exercism/trackler/tree/main/tracks
[new-team]: https://github.com/orgs/exercism/new-team
```

### Bootstrap a Track

1. Add the "new track" label.
1. Confirm maintainer

   - If the requestor is volunteering, that's fine.
   - If the requestor is volunteering someone else for the job, confirm with that person.
   - If there is no maintainer, label with "needs maintainer"

1. Once a maintainer is confirmed, add the "new track" checklist as a reply.
1. Once the checklist is complete, let the requestor/maintainer know that the repo is ready for them,
   and point them to the launch checklist issue.

[saved-replies]: https://github.com/blog/2135-saved-replies
[request-new-language-track]: https://github.com/exercism/request-new-language-track
[tools]: https://github.com/exercism/tools
[clone-tracks]: https://github.com/exercism/tools#scripts
[hub]: http://github.com/github/hub
