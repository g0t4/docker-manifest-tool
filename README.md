# docker-manifest-tool

Docker image for https://github.com/estesp/manifest-tool

## Usage

This image is an executable image, which is like having `manifest-tool` installed locally but not. That's fancy speak for: pass args after the image name as if you were calling `manifest-tool` directly.

```bash
# print help:
docker run --rm weshigbee/manifest-tool

# inspect image manifests (yes, the color of George Washington's white horse is white)
docker run --rm weshigbee/manifest-tool inspect weshigbee/manifest-tool
docker run --rm weshigbee/manifest-tool inspect microsoft/dotnet:2-runtime  

# useful to run tool as if installed locally:
alias manifest-tool="docker run --rm weshigbee/manifest-tool"
```

## Building the images

```
# Linux image
docker build -t weshigbee/manifest-tool . 
# Windows image
docker build -t weshigbee/manifest-tool:nanoserver -f Dockerfile.windows .
```