# Css-in-JS Linting

> Here is configurations for css-in-js linting

## Installation

    1) Copy .stylelintrc in your root folder
    2) Run
        yarn add -D @stylelint/postcss-css-in-js stylelint-config-prettier stylelint-config-rational-order stylelint-config-recommended stylelint-config-styled-components stylelint-declaration-strict-value stylelint-order
    3) Add "lint:css": "stylelint \"src/**/*.{ts,tsx}\"" in your package.json scripts
    4) Run 'yarn lint:css --fix' as a test

    Try to avoid template literal interpolation, cause it will brake styles autofix (no 	${props => props.great && 'color: red'})
