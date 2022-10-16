# debian-asdf-awscli

[![GitHub](https://img.shields.io/github/v/tag/caspiandb/docker-debian-asdf-awscli?label=GitHub)](https://github.com/caspiandb/docker-debian-asdf-awscli)
[![CI](https://github.com/caspiandb/docker-debian-asdf-awscli/actions/workflows/ci.yaml/badge.svg)](https://github.com/caspiandb/docker-debian-asdf-awscli/actions/workflows/ci.yaml)
[![Lint](https://github.com/caspiandb/docker-debian-asdf-awscli/actions/workflows/lint.yaml/badge.svg)](https://github.com/caspiandb/docker-debian-asdf-awscli/actions/workflows/lint.yaml)
[![Docker Image Version](https://img.shields.io/docker/v/caspiandb/debian-asdf-awscli/latest?label=docker&logo=docker)](https://hub.docker.com/r/caspiandb/debian-asdf-awscli)

Container image with:

- [aws-cli](https://github.com/aws/aws-cli)

Additional Debian packages:

- [bzip2](https://packages.debian.org/bullseye/bzip2)
- [groff-base](https://packages.debian.org/bullseye/groff-base)
- [jq](https://packages.debian.org/bullseye/jq)
- [pv](https://packages.debian.org/bullseye/pv)
- [xz-utils](https://packages.debian.org/bullseye/xz-utils)

## Tags

- `bullseye-YYYYmmdd-awscli-X.Y.Z`, `latest`

## Usage

CLI:

```shell
docker pull caspiandb/debian-asdf-awscli
docker run -v ~/.aws:/root/.aws -e AWS_PROFILE caspiandb/debian-asdf-awscli aws sts get-caller-identity
```

Dockerfile:

```Dockerfile
FROM caspiandb/debian-asdf-awscli:latest
RUN aws --version
```

## License

[License information](https://github.com/asdf-vm/asdf/blob/master/LICENSE) for
[asdf](https://asdf-vm.com/) project.

[License information](https://github.com/aws/aws-cli/blob/develop/LICENSE.txt)
for [aws-cli](https://github.com/aws/aws-cli) project.

[License
information](https://github.com/caspiandb/docker-debian-asdf-awscli/blob/main/LICENSE) for
container image project.
