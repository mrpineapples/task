## Task (task manager)

CLI to keep track of your tasks

To use Task
```go
go get github.com/mrpineapples/task
cd $GOPATH/src/github.com/mrpineapples/task
go install
```
**or** clone the repo anywhere on your machine and `go install` at the root.

`task` will now be available to use as a global command.

## How to use
```
Task is a CLI task manager

Usage:
  task [command]

Available Commands:
  add         Adds a task to your task list
  do          Marks a task as completed
  help        Help about any command
  list        Lists all of your tasks

Flags:
  -h, --help   help for task

Use "task [command] --help" for more information about a command.
```
_Note: Using `task add` creates a `tasks.db` file in your home directory (usually `/Users/NAME` on unix machines). This is the database which the CLI will interact with._

#### Example
```
$ task add Test the application
Added "Test the application" to your task list.
$ task add Update docs for the app
Added "Update docs for the app" to your task list.
$ task list
You have the following tasks:
1. Test the application
2. Update docs for the app
$ task do 1 2
Marked "1" as completed.
Marked "2" as completed.
$ task list
You have no tasks to complete! It's lit 🔥
```
