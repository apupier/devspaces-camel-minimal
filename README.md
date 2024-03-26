[Open in Red Hat Developer Sandbox](https://workspaces.openshift.com/#https://github.com/apupier/devspaces-camel-minimal.git)

# Minimal example for Camel standalone in OpenShift Dev Spaces

This repository shows the minimal setup to have Red Hat Developer Sandbox setup with capabilities to create, edit graphically or textually, run, debug and deploy a standalone Camel Yaml route.

After opening the repository in Red Hat OpenShift Dev Spaces, wait for all extensions to be installed. You can notice that it is mentioning `installing` during this waiting phase.

On first run, you will have to accept the `https://github.com/apache/camel/` domain in the terminal which is opening.

# Technical considerations

To use this example on a productized installation of OpenShift Developer Spaces, you will need to provide a specific container image with `jbang`. It means to provide your own devfile with this kind of content (here using the upstream image):

```yaml
schemaVersion: 2.1.0
metadata:
  name: demo-project-minimal-with-run
components:
  - name: tools
    container:
      image: quay.io/devfile/universal-developer-image:latest
      memoryRequest: 1Gi
      memoryLimit: 3Gi
      cpuLimit: 1000m
      cpuRequest: 500m
```
