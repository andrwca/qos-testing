# QoS testing
A sample project showing how to set the TOS (DS) field in an IP header, with docker compose suitable for testing traffic control in Linux.

# Notes

- To use the `tc` command when execing into the sender container, make sure docker isn't using the WSL backend. This uses a linux kernel without the correct configuration for `tc`. If you try this, you'll get an error when issuing `tc` commands. Work around is to switch to using hyper-v as the docker backend.
- See https://github.com/docker/for-win/issues/13882
