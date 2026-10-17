# OpenProjects

One skill that turns a chat in the agent app you already use into a project coordinator. You post asks in that chat. The coordinator acknowledges each one, hands it to its own thread agent working on its own branch, keeps shared project memory, and drives pull requests to green.

## Install

Copy `skills/openprojects/` into your agent's skills folder, for example `.agents/skills/openprojects/` in your repository.

## Use

Open a chat in your repository and invoke the `openprojects` skill. The chat becomes the coordinator. Project state lives in `.openprojects/` in your main checkout, which the skill adds to `.gitignore`:

- `memory/` holds shared project memory.
- `threads/` has one file per thread.
- `files/` holds shared outputs.
- `worktrees/` holds each thread's checkout.

Invoke the skill again in a new chat to resume. The new coordinator picks up memory and any running threads.

## License

Apache-2.0
