# Orthanc DICOM server for caMicroscope

caMicroscope DICOM server (Orthanc) build scripts

```
docker run [-v /path/to/images:/images] -i -t -p 8042:8042 camicroscope/dicomsrv
```

`-i -t` required [to be able to stop the container](https://stackoverflow.com/a/41099052)

# Updating caMicroscope orthanc-indexer plugin

Because build_orthanc_indexer.sh does "git clone" without specifying commit hash, Docker caches this line so if caMicroscope plugin repository is updated, please make a new tag there (such as: v0.3) and update the version in number in the script. See also the [BFBridge documentation](https://github.com/camicroscope/BFBridge/wiki/Updating-BFBridge) which describes the exact steps.

## Testing

The easiest way to test Orthanc is the GUI but for DICOM server testing, please see the storescu command on https://book.orthanc-server.com/users/cookbook.html
