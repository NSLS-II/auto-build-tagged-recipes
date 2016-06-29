# nsls2-tag
The recipes that are needed at nsls2 but are not on `conda-forge` yet.

## Building the stack from scratch

### If you can see `anaconda.org`

Navigate to the root of this git repository.
Decide what channel you want to upload to, `UPLOAD_CHANNEL`.
Have your anaconda token ready, `BINSTAR_TOKEN`.
Invoke the build script.

```
export BINSTAR_TOKEN=your_binstar_token
export UPLOAD_CHANNEL=lightsource2-tag
bash scripts/run_docker_build.sh
```

or, as a one-liner
```
BINSTAR_TOKEN=your_binstar_token UPLOAD_CHANNEL=lightsource2-tag bash scripts/run_docker_build.sh
```


### If you are at nsls2 and can see `anaconda.nsls2.bnl.gov`

Navigate to the root of this git repository.
Decide what channel you want to upload to, `UPLOAD_CHANNEL`.
Have your anaconda token ready, `BINSTAR_TOKEN`.
Get the current url of anaconda.nsls2.bnl.gov for uploading, `ANACONDA_SERVER_URL`
Invoke the build script.

```
export ANACONDA_SERVER_URL="https://pergamon.cs.nsls2.local:8443/api"
export BINSTAR_TOKEN=your_binstar_token
export UPLOAD_CHANNEL=lightsource2-tag
bash scripts/run_docker_build.sh
```

or, as a one-liner
```
ANACONDA_SERVER_URL="https://pergamon.cs.nsls2.local:8443/api" BINSTAR_TOKEN=your_binstar_token UPLOAD_CHANNEL=lightsource2-tag bash scripts/run_docker_build.sh
```
