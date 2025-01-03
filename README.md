# kraise

## Working with Submodules

### Cloning a Project with Submodules

You must run two commands:

```
git submodule init
```

to initialize your local configuration file, and

```
git submodule update
```

to fetch all the data from that project and check out the appropriate commit listed in your superproject.

There is another way to do this which is a little simpler, however. If you pass

```
git clone --recurse-submodules
```

to the  command, it will automatically initialize and update each submodule in the repository, including nested submodules if any of the submodules in the repository have submodules themselves.

You can combine the git submodule init and git submodule update steps by running

```
git submodule update --init
```

To also initialize, fetch and checkout any nested submodules, you can use the foolproof

```
git submodule update --init --recursive
```

If you want to check for new work in a submodule, you can go into the directory and run

```
git fetch
```
and

```
git merge
```

the upstream branch to update the local code.
