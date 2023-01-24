# Creating a Project

## Project Generation

Now that the CLI is installed, you can generate a new project by using the `wails init` command.

Pick your favourite framework:

=== "Svelte"

    Generate a [Svelte](https://svelte.dev/) project using JavaScript with:

    ```
    wails init -n myproject -t svelte
    ```

    If you would rather use TypeScript:<br/>

    ```
    wails init -n myproject -t svelte-ts
    ```

=== "React"

    Generate a [React](https://reactjs.org/) project using JavaScript with:

    ```
    wails init -n myproject -t react
    ```

    If you would rather use TypeScript:<br/>

    ```
    wails init -n myproject -t react-ts
    ```

=== "Vue"

    Generate a [Vue](https://vuejs.org/) project using JavaScript with:

    ```
    wails init -n myproject -t vue
    ```

    If you would rather use TypeScript:<br/>

    ```
    wails init -n myproject -t vue-ts
    ```

=== "Preact"

    Generate a [Preact](https://preactjs.com/) project using JavaScript with:

    ```
    wails init -n myproject -t preact
    ```

    If you would rather use TypeScript:<br/>

    ```
    wails init -n myproject -t preact-ts
    ```

=== "Lit"

    Generate a [Lit](https://lit.dev/) project using JavaScript with:

    ```
    wails init -n myproject -t lit
    ```

    If you would rather use TypeScript:<br/>

    ```
    wails init -n myproject -t lit-ts
    ```

=== "Vanilla"

    Generate a Vanilla project using JavaScript with:

    ```
    wails init -n myproject -t vanilla
    ```

    If you would rather use TypeScript:

    ```
    wails init -n myproject -t vanilla-ts
    ```

There are also [community templates](../community/templates.md) available that offer different capabilities and frameworks.

To see the other options available, you can run `wails init -help`.
More details can be found in the [CLI Reference](../reference/cli.md#init).

## Project Layout

Wails projects have the following layout:

```
.
├── build/
│   ├── appicon.png
│   ├── darwin/
│   └── windows/
├── frontend/
├── go.mod
├── go.sum
├── main.go
└── wails.json
```

### Project structure rundown

- `/main.go` - The main application
- `/frontend/` - Frontend project files
- `/build/` - Project build directory
- `/build/appicon.png` - The application icon
- `/build/darwin/` - Mac specific project files
- `/build/windows/` - Windows specific project files
- `/wails.json` - The project configuration
- `/go.mod` - Go module file
- `/go.sum` - Go module checksum file

The `frontend` directory has nothing specific to Wails and can be any frontend project of your choosing.

The `build` directory is used during the build process. These files may be updated to customise your builds. If
files are removed from the build directory, default versions will be regenerated.

The default module name in `go.mod` is "changeme". You should change this to something more appropriate.
