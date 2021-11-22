# SCSS Linting

> Here is configurations for SCSS linting

## Installation

    1) Copy .stylelintrc in your root folder
    2) Run
        yarn add -D postcss postcss-scss stylelint-config-prettier stylelint-scss stylelint-config-rational-order stylelint-config-recommended stylelint-config-styled-components stylelint-declaration-strict-value stylelint-order
    3) Add "lint:css": "stylelint \"src/**/*.{ts,tsx}\"" in your package.json scripts
    4) Run 'yarn lint:css --fix' as a test
