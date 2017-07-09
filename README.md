# NuKeeper

Automagically update nuget packages in .NET projects.

## Why
 
Because .Net devs are bad at applying nuget package updates.

## What

**NuKeeper** will compare the nuget packages used in your solution to the latest versions available on [Nuget.org](https://www.nuget.org/), and make PRs containg updates.


## How

Written in .Net core.

You will need command line versions of `git` and `dotnet`.

You will need [a github api token](https://github.com/blog/1509-personal-api-tokens) with access to public repositories.

## Repository mode

Will PR a single repository. Point it at the https url of a github repo, like this:

syntax:
```
C:\Code\NuKeeper\NuKeeper>dotnet run repository <GitToken> <RepoUrl>
```

## Organisation mode

Will discover repositories in that organisation and update them.

```
C:\Code\NuKeeper\NuKeeper>dotnet run organisation <GitToken> https://api.github.com/ <OrgName>
```

Inspired by [Greenkeeper](https://greenkeeper.io/).

