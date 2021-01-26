# earthly --push --no-cache +docker

ARG EARTHLY_TARGET_TAG
ARG VERSION=$EARTHLY_TARGET_TAG

docker:
    BUILD --build-arg VERSION="$VERSION" ./2019+docker
    BUILD --build-arg VERSION="$VERSION" ./2020+docker
