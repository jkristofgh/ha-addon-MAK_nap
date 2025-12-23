# Nap Home Assistant Add-on Repository

This folder contains the files that Home Assistant expects when you add a custom add-on repository. To make it usable:

1. Build and push a multi-architecture container image for the simulator (see `docs/DEPLOY_HOME_ASSISTANT.md`).
2. Replace `REPLACE_WITH_GITHUB_USERNAME/REPO` references with the path to the GitHub repository that will host these files.
3. Replace the `image:` in `nap-sim/config.yaml` with the container image you pushed (for example `ghcr.io/janos/nap-ha-{arch}`).
4. Push this folder to a public or private GitHub repository and add that repository URL to Home Assistant under Settings → Add-ons → Add-on Store → ⋮ → Repositories.

Home Assistant Supervisor will use `repository.yaml` for metadata and display the `Nap Simulation` add-on defined in `nap-sim/config.yaml`.
