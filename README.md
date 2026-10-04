# agentworks-builds

Release builds of [AgentWorks](https://github.com/manishiitg/agentworks), built once by GitHub Actions and downloaded by the servers that run it.

This repository holds no source code. Each release (`build-<builder>-<mcpagent>-<provider>`, the first 8 characters of the three commits it was built from) carries:

- the build tarball (binaries, frontend, CLI downloads, the three repositories' source without `.git`), and
- `manifest.json`: the three revisions, CPU architecture, glibc version, and the sha256 of every file.

A server verifies every file against the manifest before it activates a build. Only the newest builds are kept; older ones are deleted automatically.

You do not need anything here to use AgentWorks: get it from the main repository.
