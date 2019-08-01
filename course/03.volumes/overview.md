# OVERVIEW
## Section

- Containers are **usually** immutable and ephemeral.
- "Immutable infrastructure": Only re-deploy containers, never change.
- This is the ideal scenario, but what about databases, or unique data?
- Docker gives us features to ensure these "separation of concerns".
- This is known as "persistent data".
- Two ways: Volumes and bind mounts.
- Volumes: Make special location outside of container UFS.
- Bind mounts: Link container path to host path.