# Sample 

## About Searchex Repos and Collections

Searchex supports the public exchange of searchable document repositories.
Searchex repositories are managed by Git.  You can install a Searchex
repository in seconds.

Each `repo` contains one or more `collections`.  Each `collection` is defined
by a `config` file - a yaml file with indexing and search parameters.

To install this Sample repo on your system, use the command:

    searchex fetch elixir-search/sample

Then view your new collections with the command:

    searchex ls

Now you can search any of the collections in the Sample Repo.

## Behind the Scenes

Searchex auto-creates a hidden directory `~/.searchex`.  Under this directory,
there is one subdirectory for each Repo.  Each Repo directory can contain one
or more `config` files.

    ~/.searchex
    |-- local
      |-- collection1.yml
      |-- collection2.yml
    |-- sample
      |-- genesis.yml
      |-- constitution.yml
      |-- dickens.yml
    |-- another_repo
      |-- some_other_config.yml

Things to note:

- Searchex auto-creates a `~/.searchex/local` directory which contains your
  locally-created `config` files. This is your `local` repo.

- You can fetch other Searchex repos from any location on the internet.

- You can manually add/remove/edit/update any file under `~/.searchex`.
  Any sort of Git operation (commit/pull/revert/etc) is ok.  

- Documents and cache-file locations are defined in the `config` file.  They
  can be located in the repo directory itself, or elsewhere on your filesystem.

Best practices:

- Before publishing a Searchex Repo, test it locally to make sure everything works.

- Publish documents and a populated cache file in your Repo, so everything is
  self-contained and pre-warmed.
