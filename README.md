# vscode-test

To reproduce the bug

1. Open my.code-workspace. It should open the workspace in VSCode
2. Press Cmd+P and type `>Tasks: Run Task` and select task called `run` from folder `Project2`

Expected console output:

```console
> Executing task in folder Project2: npm install <

npm WARN Project2@1.0.0 No description
npm WARN Project2@1.0.0 No repository field.

up to date in 0.483s
found 0 vulnerabilities


Terminal will be reused by tasks, press any key to close it.

> Executing task in folder Project2: node index.js <

Hello Project 2

Terminal will be reused by tasks, press any key to close it.
```

Actual console output:

```console
> Executing task in folder Project1: npm install <

npm WARN Project1@1.0.0 No description
npm WARN Project1@1.0.0 No repository field.

up to date in 0.594s
found 0 vulnerabilities


Terminal will be reused by tasks, press any key to close it.

> Executing task in folder Project2: node index.js <

Hello Project 1

Terminal will be reused by tasks, press any key to close it.
```
