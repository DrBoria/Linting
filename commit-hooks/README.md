# Commit hooks

> Here is configurations for husky and commitlint

## Installation

    1) Copy all files from this folder into your root repository (except README.md)
    1.1) .husky folder is required for Windows
    2) If you use Styled-components
        Add:

        "husky": {
            "hooks": {
            "commit-msg": "commitlint -E $1",
            "pre-commit": "tsc --noEmit && lint-staged"
                }
            },
            "lint-staged": {
                "*.{ts,tsx}": [
                "prettier --write",
                "eslint --fix",
                "stylelint --fix"
            ],
            "*.{js,html,md,json}": [
                "prettier --write"
            ]
        },

        into your package.json

        For SCSS add:

        "lint-staged": {
            "*.{ts,tsx}": [
                "prettier --write",
                "eslint --fix"
            ],
            "*.scss": [
                "stylelint --fix"
            ],
            "*.{js,html,md,json}": [
                "prettier --write"
            ]
        },


    3) For private repository add "postinstall": "husky install" in your package.json scripts
    3.1) For public repository add
        "postinstall": "husky install",
        "prepublishOnly": "pinst --disable",
        "postpublish": "pinst --enable"

        in your package.json scripts
    4) Run
        yarn add -D husky lint-staged pinst @commitlint/cli @commitlint/config-conventional
    5) Now try to commit something for test

> Info about hooks for windows (https://typicode.github.io/husky/#/?id=yarn-on-windows)
> If you use jira you can add jira commitLint config (https://github.com/Gherciu/commitlint-jira)
