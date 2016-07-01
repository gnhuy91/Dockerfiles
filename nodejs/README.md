# Nodejs image
Inherit the official [node](https://hub.docker.com/_/node/) image with the addition of using an unprivileged user (`node`) to run your application.
By default the official image runs your application on `root`, which might cause some unexpected security problems.

Using an unprivileged user will also avoid having to `bower install --alow-root` (which is not recommended).
