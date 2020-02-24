# The solution of merge hell in monorepo
Maria Guseva

3k commits into the monorepo per work day.

Half of GitHub repositories are around a MB (is the case for mine :-) )

## Advantages of the Monorepo
Common infrastructure, changes in one commit


## Bitbucket merge hell
For each PR, BitBucket generates a {pullRequestId}/merge branch. So if you have N pull requests waiting, after including one you'll have to recalculate the merge branch for N - 1 PRs.

They have a *lot* of PRs waiting.

## Build manager plugin
Define a project (included path, excluded suffixes etc), and from that determine whether something specific thing changed in *that* project.


