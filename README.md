# Minimal example for Camel standalone in OpenShift Dev Spaces

This repository shows the minimal setup to have Red Hat Developer Sandbox setup with capabilities to create, edit graphically or textually, run, debug and deploy a standalone Camel Yaml route.

After opening the repository in Red Hat OpenShift Dev Spaces, wait for all extensions to be installed. You can notice that it is mentioning `installing` during this waiting phase.

On first run, you will have to accept the apache.org domain in the terminal which is opening.

# Technical considerations

A devfile is provided to have `jbang` available on system path. This is a requirement for several features to run and debug. For this purpose, the community `devfile/universal-developer-image` is used.
