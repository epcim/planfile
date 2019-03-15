
# Git workflow concept to fetch and sync habitat plans

TLDR;
Individual plans from upstream repositories are fetched directly to root of your git repository.
Each plan folder is worktree branch tracking upstream repository with configured spare-checkout.

## Requirements

Requires `git --version >= 2.20`.
Requires `git-cross` http://github.com/epcim/git-cross

## Usage

Configure your tracked plans, hooks in Planfile.cross:

```sh
  use core https://github.com/habitat-sh/core-plans
  use ncerny https://github.com/ncerny/habitat-plans
  use qago https://github.com/qago/habitat-plans
  use jarvus https://github.com/JarvusInnovations/habitat-plans
  use eeyun https://github.com/eeyun/habitat-plans
  use starkandwayne https://github.com/starkandwayne/habitat-plans

  # example: origin/plan [branch]
  patch core/consul
  patch core/cacerts
  patch core/etcd
  patch ncerny/cfssl
```

Track and checkout plans with:

```sh
curl -sS https://raw.githubusercontent.com/epcim/git-cross/master/git-cross -o git-cross; chmod u+x $_
./git-cross
```

Use `git add/checkout/commit/rebase` as you are used to.


## Examples

TBD

