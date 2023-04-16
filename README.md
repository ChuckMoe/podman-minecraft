# Image
The image used was created by [itzg](https://hub.docker.com/r/itzg/minecraft-server). For all variable descriptions, go there.

# Volumes
Change the volumes.hostPath.path to the directory where you want to save and access all the data available to Minecraft. If you do not want or need direct access, you can instead use:

```yaml
volumes:
  - name: data
    persistentVolumeClaim:
          claimName: minecraft-data
```

# Commands

Start Minecraft
```bash
podman play kube --configmap=secrets.yaml pod.yaml
```

Stop Minecraft
```bash
podman play kube --down pod.yaml
```

To update Minecraft, aka. use the newest container, just stop and start again.
