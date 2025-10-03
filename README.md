# Onboarding
Assets to assist onboarding new developers. Assumes Macbook.

## Usage

Install Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
After completion, run the following:

```bash
# create a temp file
TMPFILE=$(mktemp)
BREWFILE="https://raw.githubusercontent.com/7dayslabs/onboarding/refs/heads/main/Brewfile"
# fetch your Brewfile into it
curl -fsSL "${BREWFILE}?_=$(date +%s)" -o "${TMPFILE}"
# run brew bundle against it
brew bundle install --file="${TMPFILE}"
# optional: remove afterwards
rm "${TMPFILE}"
```
