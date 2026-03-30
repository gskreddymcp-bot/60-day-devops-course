# Git Basics Diagrams (for practice sessions)

## 1) Working Tree -> Staging -> Local Repo -> Remote

```text
[Working Directory] -- git add --> [Staging/Index] -- git commit --> [Local .git]
      ^                                                           |
      |------------------- git restore ---------------------------|

[Local .git] -- git push --> [Remote origin]
[Remote origin] -- git fetch/pull --> [Local .git]
```

## 2) Feature Branch and Merge

```text
main:    A------B--------------E
                 \            /
feature/x:        C----D-----/
```

## 3) Rebase Concept (linear history)

```text
Before:
main:      A-----B-----C
                    \
feature:             D-----E

After `git rebase main` on feature:
main:      A-----B-----C
                          \
feature:                   D'----E'
```

## 4) Conflict Markers

```text
<<<<<<< HEAD
current branch content
=======
incoming branch content
>>>>>>> feature/some-change
```

## 5) Reset Modes

```text
git reset --soft  <sha>   # move HEAD only
git reset --mixed <sha>   # move HEAD + reset staging
git reset --hard  <sha>   # move HEAD + reset staging + working tree
```
