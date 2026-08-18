# Stage 0 — Final Progress Record v1.4

**Engineering Environment, Git and Baseline — COMPLETION RECORD**

**Stage:** Stage 0
**Version:** Progress Record v1.4 — Final
**Governing resource:** Master Curriculum v1.2 FINAL
**Status:** ✅ **COMPLETE**
**Exit-gate decision:** Passed

The Master Curriculum defines Stage 0 around the professional workspace, Git/GitHub, the source-to-executable pipeline, basic header/source understanding, documentation habits, and a baseline used to determine what can be accelerated in Stage 1.

## Completed competencies

Established and used the engineering workspace:

```text
~/Engineering/

├── README.md

├── experiments/

├── learning/

│   └── stage0-baseline/

└── projects/
```

Demonstrated basic terminal navigation and filesystem interpretation, including `pwd`, `cd`, `ls`, hidden files, file permissions, `touch`, `cat`, executable invocation and basic path concepts.

Installed/configured VS Code and its CLI launcher; distinguished the editor/IDE environment from the actual native compiler/toolchain.

Verified the macOS Intel x86_64 development environment and Apple Clang toolchain.

Compiled and executed C++ outside Arduino IDE.

Generated/inspected preprocessing, assembly and object-file artifacts.

Demonstrated and diagnosed both compiler/build and genuine linker failures.

Demonstrated multi-file C++ compilation and linking.

Demonstrated introductory `.h`/`.cpp` separation: declarations/interface versus definitions/implementation.

Created and verified `.gitignore`, including exclusion of generated `.o`, `.i`, `.s`, executable and macOS artifacts.

Created and maintained project README documentation.

Initialized and operated a local Git repository; demonstrated working-directory, staging-area and committed-history states.

Demonstrated tracked versus staged distinction and that modified tracked files must be staged again for subsequent commits.

Created meaningful Git history and configured a privacy-preserving GitHub noreply author identity.

Created `feature-output`, modified/tested code independently, committed the change, switched back to `main`, compared the branches, and merged using a fast-forward.

Explained branch, commit and HEAD at the required Stage 0 level.

Connected the repository to GitHub through `origin`.

Demonstrated first push/upstream setup, subsequent push, pull, remote tracking and clone.

Created a temporary clone and verified that cloning reproduces files, Git history and remote configuration.

Created the master Engineering Development Portfolio/project index at:

```text
~/Engineering/README.md
```

This closes the items that v1.3 still listed as gaps: branch/merge, GitHub remote workflow, linker understanding, `.h`/`.cpp`, project index and final exit-gate review.

## Current competency level

| **Area**                           | **Stage 0 exit estimate** |
| ---------------------------------- | ------------------------- |
| Command-line / filesystem          | ~L2 introductory          |
| Development environment/toolchain  | ~L2                       |
| Native C++ build workflow          | ~L2                       |
| Compiler/linker diagnosis          | ~L2                       |
| Git local fundamentals             | ~L2                       |
| Branches / HEAD / history          | ~L2                       |
| GitHub remote workflow             | ~L2 introductory          |
| `.h` / `.cpp` organization         | ~L2 introductory          |
| README / engineering documentation | ~L2 foundation            |
| Code literacy                      | CL1 developing toward CL2 |

These levels do **not** imply mastery. Stage 0 deliberately establishes enough foundation to stop these systems being black boxes; Stage 1 deepens programming and code literacy substantially.

## Projects / experiments completed

### stage0-baseline

**Location:**

```text
~/Engineering/learning/stage0-baseline
```

**GitHub remote:**

```text
origin → Afxb9/stage0-baseline
```

**Final demonstrated source structure includes:**

```text
main.cpp
math.cpp
math.h
README.md
.gitignore
```

Generated build artifacts remain local/ignored where applicable.

## Demonstrated Git history

Latest verified history:

```text
929c3be  Add multi-file C++ and header experiment

63fad3e  Update README.md

0dca466  Add feature brach output

2bfeea4  Add Git tracking experiment

c35a3e6  Create Stage 0 C++ baseline project
```

At the final verified repository state:

```text
HEAD -> main
origin/main -> 929c3be
```

with:

```text
nothing to commit, working tree clean
```

## Branch experiment

Created:

```text
feature-output
```

Added/tested a third output line, committed it, switched to `main` and verified the feature disappeared from the working-directory version, compared the histories, and merged the feature.

**Merge result:**

```text
Fast-forward
```

The temporary branch was subsequently deleted without losing its committed history.

## GitHub experiment

Demonstrated:

```text
local → push → GitHub

GitHub → pull → local

GitHub → clone → new local repository
```

A GitHub-side README change produced commit:

```text
63fad3e Update README.md
```

and was successfully pulled into the local repository.

## Build/linker experiment

Created `math.cpp` and compiled:

```bash
clang++ -c math.cpp -o math.o
```

Deliberately produced:

```text
Undefined symbols for architecture x86_64:

"add(int, int)"
```

when the implementation was omitted from the link.

Corrected using both:

```bash
clang++ main.cpp math.o -o baseline
```

and:

```bash
clang++ main.cpp math.cpp -o baseline
```

Then refactored the function declaration into `math.h`.
## Current mental models

### Git

```text
Working Directory

      ↓ git add

Staging Area

      ↓ git commit

Repository / History

      ↓ git push

Remote Repository
```

Key rule:

**Tracked ≠ staged.**

Tracking persists; staging represents the particular version prepared for the next commit.

### Branches

Commit = saved snapshot

Branch = movable pointer/name to a commit

HEAD = current checkout

### Build pipeline

```text
source

→ preprocess

→ compile

→ assemble

→ object files

→ link

→ executable
```

### Header/source separation

```text
.h   → interface / declarations

.cpp → implementation / definitions
```

## Diagnostic / retention result

A short whole-Stage-0 diagnostic was performed rather than a large conventional exam.

Demonstrated retained understanding of terminal navigation, executable permissions, VS Code versus compiler/toolchain, architecture identification, source/object/executable distinction, linker-error diagnosis, Git local-versus-remote state, branches/HEAD, and header/source separation.

Minor terminology/recall points to reinforce naturally in Stage 1:

* `~` = home directory.
* `-a` in `ls -la` is what includes hidden files.
* Retain the exact build-pipeline order.
* Continue strengthening precise programming terminology while working with real code.

These are **non-critical reinforcement points**, not Stage 0 blockers. The curriculum explicitly says not to demand perfection before moving on; non-critical gaps can be documented and deliberately revisited.

## Documentation & Portfolio status

Project README established.

Meaningful Git history established.

GitHub repository published.

`.gitignore` repository hygiene established.

Master workspace/project index created at:

```text
~/Engineering/README.md
```

Stage 0 therefore satisfies the curriculum expectation to establish the GitHub/README foundation and an equivalent portfolio/project index. Stage 1 will move to documenting electronics/programming experiments and publishing the first properly structured capstone repository.

## Stage 0 Exit Gate

| **Required exit evidence**                            | **Result** |
| ----------------------------------------------------- | ---------- |
| Create and push a small C/C++ project repository      | ✅          |
| Make a branch, change code, merge and explain history | ✅          |
| Compile simple program outside Arduino IDE            | ✅          |
| Explain `.h` / `.cpp` at basic level                  | ✅          |
| Create master repository structure                    | ✅          |

These are the explicit Stage 0 exit requirements in Master Curriculum v1.2.

## Final decision

**STAGE 0 PASSED — proceed to Stage 1.**

