Bug Description

`snap installation of local files fails with: cannot find signatures`

The recent release of snapd to xenial-updates breaks the demos test suite:

`$ sudo snap install Lepton_1.7.snap`

`error: cannot find signatures with metadata for snap "Lepton_1.7.snap"`

Now it requires the --force-dangerous flag when installing a local file.

`$ sudo snap install Lepton_1.7.snap --force-dangerous`

Lepton installed

Also note that the flag will be renamed to --dangerous in a following release.