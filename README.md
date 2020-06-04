# Blacksmith Containers Forge

This Blacksmith Forge teaches a [Blacksmith Broker][broker] how to
deploy standalone container based service (powered by Docker),
deployments, which is a useful base for multiple services.

## Deploying

To deploy this forge, you will need to add it to your existing
Blacksmith Broker manifest deployment, co-locating the
`container-blacksmith-plans` job on the Blacksmith instance group.

Here's an example to get you started (clipped for brevity):

```yaml
releases:
  - name:    container-forge
    version: latest

instance_groups:
  - name: blacksmith
    jobs:
      - name:    container-blacksmith-plans
        release: container-forge
        properties:
          plans:
            # your plans here
            # (see below)
```

