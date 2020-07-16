# PHP Composer with NPM

Based on: https://github.com/prooph/docker-files

## Usage

Add to the `.zshrc`

```
function composer () {
    tty=
    tty -s && tty=--tty

    docker run \
        $tty \
        --interactive \
        --rm \
        --volume /etc/passwd:/etc/passwd:ro \
        --volume /etc/group:/etc/group:ro \
        --volume $(pwd):/app \
        codibly/composer "$@"
}
```
