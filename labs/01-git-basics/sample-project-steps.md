# Sample Project Creation Steps (Git Practice)

Use this mini project to practice complete Git operations end-to-end.

## Project Goal
Build a tiny Python CLI app with incremental commits and branch-based changes.

## Step-by-step

```bash
mkdir git-practice-app
cd git-practice-app
git init

echo "# Git Practice App" > README.md
mkdir -p src tests docs
cat > src/app.py <<'PY'
print("hello git")
PY

git add README.md src/app.py
git commit -m "Create initial app skeleton"
```

## Add a feature branch

```bash
git checkout -b feature/add-cli-arg
cat > src/app.py <<'PY'
import sys
name = sys.argv[1] if len(sys.argv) > 1 else "world"
print(f"hello {name}")
PY

git add src/app.py
git commit -m "Add CLI argument support"
```

## Add tests on another branch

```bash
git checkout main
git checkout -b feature/add-tests
cat > tests/test_app.py <<'PY'
def test_placeholder():
    assert True
PY

git add tests/test_app.py
git commit -m "Add initial test scaffold"
```

## Merge both branches

```bash
git checkout main
git merge feature/add-cli-arg
git merge feature/add-tests
```

## Remote practice (optional)

```bash
git remote add origin <your-remote-url>
git push -u origin main
git push -u origin feature/add-cli-arg
git push -u origin feature/add-tests
```

## Practice tasks
- Squash or clean up one commit using interactive rebase.
- Trigger and resolve one merge conflict in `README.md`.
- Recover one accidental change using `git restore` or `git reflog`.
