# vscode-rust

Here is a basic tasks.json file that you can use with Visual Studio Code to make Rust development easier. Perform common tasks with standard keyboard shortcuts. Don't bother manually going to the command line to do these common operations.

For the build tasks, press Ctrl+Shift+B, then pick the task from the list.

For the test tasks, press Ctrl+Shift+P, select Task: Run Test Tasks, then pick the test task from the list.

When I create a new Rust project in Visual Studio Code, I create a folder in the root called .vscode, then copy this tasks.json file in there and check it in with the other code. Commands are generally available immediately. If they aren't, restart Visual Studio Code.

Supported build tasks:
- build
- build all (Same as --all-targets. Added so tests get compiled as well.)
- run
- run with backtrace (RUST_BACKTRACE set to 1)
- run --release
- check
- fmt (format)
- clean
- doc

Supported test tasks:
- test
- test with backtrace (RUST_BACKTRACE set to 1)

Unsupported tasks, since I don't see how to do this in the context of a project:
- new

Note to self: add test task for running ignored tests, like this:

cargo test -- --ignored
