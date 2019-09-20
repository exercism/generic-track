# Request a new Exercism language track

## How to request support for a new language track

**Does Exercism already support the language?**

Check [this list][trackler-tracks], which contains both the active and inactive tracks on the site.

If you find the language, follow the links from that list to view the repository. The `config.json` file
has an `active` key, which will be true or false.

[trackler-tracks]: https://github.com/exercism/trackler/tree/master/tracks

**Has someone else asked for it?**

Do a search in this repository for the name of the language. Remember to check both open and closed issues.

**Does the language qualify for having a track?**

If you can answer yes to the following:

- It is a Turing-complete programming language, so no regular expressions or web framework tracks.
- Some kind of programming environment, compiler and/or interpreter must be freely available.
- Preferrably, it is possible to program in this language on Mac, Windows *and* Linux.

Then [send in a request][new-issue]!

[new-issue]: https://github.com/exercism/request-new-language-track/issues/new

## How to improve the process for the next new maintainer

It's crucial that we improve the documentation and instructions for launching a track. The best people to discover
issues with our current process are new maintainers, launching a track for the first time. Unfortunately,
that's the worst possible time for them to fix the documentation, because they've got the least amount of
knowledge about how Exercism is put together.

The files in this repository serve as a template for a new track. Some files get edited and added to the track,
others are used to [create new issues in the track][issue-templates], but are not added to the new repository.
If new maintainers have questions, it will often be because these files are confusing or missing information.

When that happens we should tweak the documentation for clarity in a new pull request to the request-new-language-track
repository (not their repository) and tag the maintainer to review it. If it's still confusing, they'll know,
and figuring out how to explain it will help us fix it.

In some cases, we might discover that we're missing high-level documentation that should live in the [docs][]
repo, in which case we should open an issue or pull request there, proposing the new documentation. Tag the new
maintainer there, as well, to get their input on the new docs.

[checklist]: https://github.com/exercism/request-new-language-track/blob/master/CHECKLIST.md
[docs]: https://github.com/exercism/docs
[issue-templates]: https://github.com/exercism/request-new-language-track/blob/master/bin/bootstrap#L67-L73

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
- [ ] Turn on [Travis CI][travis]
- [ ] If Windows-specific language, turn on [AppVeyor][appveyor]
- [ ] If Mac-specific language, turn on [Circle CI][circle]
  Add it as a Linux project, then switch it to OS X in _Project Settings -> Build Environment_
- [ ] Add as a submodule to [trackler][]
  `TRACK_ID=<id>; git submodule add https://github.com/exercism/$TRACK_ID tracks/$TRACK_ID`
- [ ] Create [new team][new-team] for language
- [ ] Add bootstrapped repository to team **with write access**
- [ ] Invite maintainer to team

[travis]: https://travis-ci.org/profile/exercism
[appveyor]: https://ci.appveyor.com/projects/new
[circle]: https://circleci.com/gh/organizations/exercism/settings#projects
[trackler]: https://github.com/exercism/trackler/tree/master/tracks
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
