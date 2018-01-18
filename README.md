# contentful.sh
[![Build Status](https://travis-ci.org/pierreprinetti/contentful-management.sh.svg?branch=master)](https://travis-ci.org/pierreprinetti/contentful-management.sh)

Shell client for the Contentful Content Management API.

This is a partial implementation; see below for the available commands.

## Usage

### Configuration

The script requires two environment variables to be set:

- `CONTENTFUL_SPACE`: the ID of the space to operate in
- `CONTENTFUL_TOKEN`: a valid Contenful Management API token

### Calls

```shell
./contentful entry get 31C9Zv7rp6IaMef2K4QI42
```

- The first argument is the name of the target resource
- The second argument is the verb of action
- Further arguments are specific to the type of call

Available commands:

- `content-type`
  - `put <typename> <filename>`
  - `activate <typename>`
  - `delete <typename>`
- `entry`
  - `get <id>`
  - `post <typename> <filename>`
  - `delete <id>`
- `upload`
  - `post <filename>`
