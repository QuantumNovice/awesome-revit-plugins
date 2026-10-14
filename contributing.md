# Contributing

Thanks for helping improve this list. Please read these guidelines before opening a pull request.

## Rules

* Only add tools or plugins that work with Autodesk Revit.
* Put open-source projects under **Open Source** and commercial products under **Paid**.
* Each entry uses the format `* [Name](URL) - Short description. (License)`. Leave out the license if it is not known.
* Link to the project's main page or repository, not a search result.
* Keep descriptions short and factual. No marketing language.
* Check that the project is still maintained and supports a current Revit version.
* Do not add duplicate entries.

## Adding an entry

The list is generated from `data/resources.json`. Do not edit `README.md` by hand.

1. Add the entry to the right section in `data/resources.json`. Each item has `name`, `url`, and `description`, and may have `license`.
2. Install the requirements and render the README:

   ```sh
   pip install -r requirements.txt
   python generate.py
   ```

3. Commit both `data/resources.json` and `README.md`.

`python generate.py --check` fails if the README is out of date. The CI workflow runs the same check.

## Commit messages

Use one of these prefixes:

* `feat:` for a new entry or section
* `bug:` for a fix to a broken link or wrong info
* `docs:` for wording changes to the README or this file
* `chore:` for repository housekeeping
* `ci:` for workflow changes
* `test:` for test changes

Example: `feat: add ricaun.RevitTest to developer tools`

## Pull requests

1. Fork the repository and create a branch.
2. Make your change and check the links work.
3. Open a pull request against `main` and describe what you added or fixed.
