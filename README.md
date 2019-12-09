# vuetify-loader error

## Installation

1. Install `my-app` and `my-lib` packages:
    ```bash
    cd my-lib && npm i && cd ../my-app && npm i 
    ```

2. Serve the application. Inside `my-app` folder:
    ```bash
    npm run serve
    ```

As you can see, the sidebar works as expected.

## Error reproduction

1. Stop any localhost serve of `my-app`.

2. Simply install vuetify as **dev-dependency** inside `my-lib`:
    ```bash
    cd ../my-lib && npm i -D vuetify
    ```

3. Serve again the application:
    ```bash
    cd ../my-app && npm run serve
    ```

4. Go back to your browser, the sidebar crashed. It is failing to access
`Vue.$vuetify.application` and `Vue.$vuetify.breakpoint` because
`Vue.$vuetify` is undefined. You can see all the errors on the console.