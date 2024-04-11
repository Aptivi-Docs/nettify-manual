---
description: Listing all the breaking changes
---

# 🗞️ Breaking Changes

There are new releases of Nettify that cause breaking changes, so you'll need to take them into consideration when upgrading your program to use later versions of Nettify. Here are the version upgrade paths:

## v1.0 to v1.2

When upgrading Nettify from v1.0 to v1.2, you'll need to consider the following breaking changes:

### Read-only lists in RSS feeds and ISP info

You used to directly get a `List<>` instance of some RSS feed and ISP info properties that could occur more than once. Starting from v1.2, to make these properties more secure, we've decided to change how we return such properties so they return an actual array instead of a generic `List` instance. This is so that it's properly conveyed to the application developers that they are not meant to be edited.

## v1.2 to v1.3

When upgrading Nettify from v1.2 to v1.3, you'll need to consider the following breaking changes:

### Migrated internet radio station info

We've migrated the internet radio station information to the upcoming version of BassBoom, which is 0.0.7 at the time of the migration, for that program to be able to play Internet radio stations without having to add a bloat of functions, such as weather forecast. If you want to keep using this feature without having to rely on BassBoom, you'll have to stay in the 1.2 version of Nettify.
