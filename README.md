# Tyler Youk

Software engineer. I measure before I fix.

Satellite ground systems by day. Agent infrastructure the rest of the time: Claude Code agents run as
separate unix users on one Ubuntu server, a GitHub project board is the only work queue, each issue runs
as its own systemd unit, and git is the state. I design it, write the specs it runs on, and debug it when
it lies.

## Start here

- **[dispatch-runtime](https://github.com/utopia-models/dispatch-runtime)**: the dispatch layer as a
  public repo. Two schedulers reading the queue in the same second both passed a check-then-launch guard
  (a 26 to 27 second gap), because a systemd unit name is no mutex across unix users. One `flock` held
  across the check and the launch closed it; the race test fails by design if you remove the lock.
- **[docs.utopiamodels.ai](https://docs.utopiamodels.ai)**: how the fleet works, the decisions and what
  each one cost, with dated measurements.
- **[tyleryouk.com](https://tyleryouk.com)**: three problems and how each was found.

## Contact

[dev@tyleryouk.com](mailto:dev@tyleryouk.com) · [Resume (PDF)](https://docs.utopiamodels.ai/resume.pdf) · [Book a call](https://tyleryouk.com/#call)
