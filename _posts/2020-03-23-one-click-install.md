---
layout: blog-detail
post-type: blog
by: Sébastien Doeraene
title: "One-click install for Scala"
---

Installing Scala has always been a task more challenging than necessary, with the potential to drive away beginners.
Should I install Scala itself? sbt? Some other build tools? What about a better REPL like Ammonite? Oh and before all that I need to install Java?

To solve this problem, the Scala Center contracted Alexandre Archambault in January 2020 to add a one-click install of Scala to [coursier](https://get-coursier.io/).
Starting today, [the main Scala download page](/download/) gives one-liner command lines incantations (and a one-click executable for Windows) to fully install Scala and all the main related tools.
For example, on Linux, all we now need is:

```bash
$ curl -Lo cs https://git.io/coursier-cli-linux && chmod +x cs && ./cs setup
```

which will install all the following software, if not yet installed:

* a JDK
* the build tools [sbt](https://www.scala-sbt.org/) and [mill](https://www.lihaoyi.com/mill/)
* the [Ammonite](https://ammonite.io/) enhanced REPL
* [scalafmt](https://scalameta.org/scalafmt/), the Scala formatter
* the [coursier](https://get-coursier.io/) CLI, to install further Scala-based applications
* the `scala` and `scalac` command-line tools

With all those installed, we are ready to go!

The download page then proceeds with two suggestions for IDEs: IntelliJ or VS Code with Metals.

For power users, [the `cs setup` command](https://get-coursier.io/docs/cli-setup) offers more configuration options, such as a non-interactive mode.

With this new simple, all-encompassing installer, we at the Scala Center hope to significantly reduce the burden of getting started with Scala.
