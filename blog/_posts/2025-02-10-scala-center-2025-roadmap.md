---
layout: blog-detail
post-type: blog
by: the Scala Center team
title: Scala Center Roadmap for 2025
description: Scala Center Roadmap for 2025.
---

In this post, we share the Scala Center plans for 2025.

## Role of the Scala Center in the Scala Ecosystem

Overall, the mission of the Scala Center is to **improve the experience of becoming and being a Scala developer**, and to **help the community to build a rich ecosystem of libraries**.

The Scala ecosystem is made of the following pillars:

- **Language, compiler, standard library:** they are the core tools that all programmers interact with when they work in Scala.
  The role of the Scala Center is to reduce the number of bugs in the compiler implementation, to help the community to contribute to these tools, and to make sure they evolve in a way that takes into account the needs of the community.
- **Documentation and MOOCs:** this website is the entry point to the ecosystem.
  It showcases the strengths of the language and its use cases, and it hosts all its documentation.
  The role of the Scala Center is to simplify the structure and the content of the website, to create and maintain high-quality online educational content (including online courses), and to help the community to contribute to the website.
- **Developer experience:** Scala programmers often don't interact directly with the compiler, but they use a tool (build tool, compile server) that does that for them.
  They also use tools to edit, analyze, navigate through, transform, compile, run, and debug Scala programs.
  The role of the Scala Center is to make sure these tools are as easy to use as possible, that they work reliably for everyone, and deliver a great developer experience.
- **Community and contributor experience:** the last pillar is the result of the work done _outside_ the Scala Center.
  The community has created thousands of projects that bring simple solutions to complex problems.
  The role of the Scala Center is to create the best environment for the emergence of such libraries.

TODO Double-check here:

> We would like to use this opportunity to raise awareness about the need for additional funds to keep our mission going.
> The Scala Center is a foundation that depends on companies and other donors who understand the importance of reinvesting in the Scala open source ecosystem.
> We are now down to one part-time in-house engineer, one contributing engineer from a sister organization and part-time support staff.
> To continue covering the broad scope and deep work on the Scala infrastructure, which each user depends on, we need your support.
> We opened a fundraising campaign in 2023, which is still ongoing.
> Please check out the [short article](https://scala-lang.org/blog/2023/09/11/scala-center-fundraising.html) and [get in touch](https://airtable.com/appu0c7lWteTaOonJ/shrMKPncLDdVK5cyW).
> The scope of the 2025 roadmap reflects this crisis.
> In order to do more, we need more resources.
>
> -- Darja Jovanovic, executive director

The remainder of this article presents our specific goals for 2025.

## Roadmap for 2025

We have identified the priorities for 2025 through our discussions with the community (online or at conferences), with our [Advisory Board members](https://scala.epfl.ch/#advisory-board-member-list), and with the main organizations that are [behind Scala](https://www.scala-lang.org/community/#whos-behind-scala) ([LAMP](https://lamp.epfl.ch), [Lightbend](https://lightbend.com), and [VirtusLab](https://virtuslab.com)).
We are grateful to all of them.

In the following subsections we remind you of our ongoing and recurring projects, and we present our most important goals as well as some additional stretch goals that would need more resources.

The roadmap we present here is of course subject to adjustments throughout the year.

### Language, Compiler, Standard Library

On the language and compiler side, we participate in the maintenance of several projects, together with LAMP, VirtusLab and Lightbend.
At the Scala Center, we are notably focused on the Scala compiler itself, the language specification and Scala.js.
We also steward the Scala Improvement Process (SIP).
In addition to those ongoing projects, our Scala Center team plans to work on the following topics this year:

- **Better integration of the compiler with Metals.**
  Metals, the LSP-based IDE architecture for Scala, relies on dedicated features of the compiler, known as the "presentation compiler".
  These features are not always as robust as they should be, which is one major cause of issues with Metals.
  We intend to audit the presentation compiler, and possibly re-architect it, in order to make it more reliable.
- **Compilation to WebAssembly.**
  In 2024, we released a first [experimental WebAssembly backend for Scala.js](https://www.scala-js.org/doc/project/webassembly.html).
  Early benchmarks suggested that it can achieve significantly better performance than the traditional JavaScript target.
  This year, we will explore further optimizations, and add support for standalone Wasm (without a JavaScript engine), in collaboration with VirtusLab.
  This will push the frontier of where Scala is applicable, allowing to use it in sandboxed environments, as increasingly found in cloud-computing offerings.
  If time permits, we would like to explore what unique features Wasm has to offer to the Scala language, such as generalized tail calls or continuations.
- **Stretch goal: Security audit of the standard library.**
If sufficient funding is secured, we aim to collaborate with security experts to conduct a thorough audit of the Scala standard library. This effort would focus on identifying potential vulnerabilities, and applying necessary patches.

### Documentation

In addition to maintaining the Scala website and managing our online course learners, we will:

- **Merge the Scala 2 and 3 books, and the tour of Scala.**
  During the previous year, we brought the Scala 3 book up to date with the content available in the Scala 2 book.
  It is now time to merge them to simplify the documentation structure.
  Moreover, we will replace the Tour of Scala by a single section at the beginning of the common book.
- **Complete the Scala 3 language specification.**
  In 2024, we updated the Scala 3 specification with all the core changes brought by Scala 3.
  We will finish the effort of integrating the remaining aspects from the Scala 3 reference.
- **Reshape the index of documentation, guides and overviews.**
  The documentation index page, as well as the index of guides and overviews, have grown organically over the years.
  Resources permitting, we intend to restructure them, so that it is easier to find the information one is looking for.
- **Stretch goal: Expand toolkit tutorials.**
  If resources allow, we plan to develop more hands-on tutorials that guide users through practical scenarios. These will include topics such as building command-line applications, interacting with SQL databases, and developing web user interfaces.

### Developer Experience

In addition to maintaining some of the core tools of the ecosystem (sbt, tasty-query, scaladex), we will:

- **Stretch goal: Conclude the development of sbt 2.**
  During 2024, we helped stabilizing sbt 2, which is based on Scala 3.
  It is currently available as a milestone release.
  We also brought significant performance improvements.
  We hope to conclude that effort this year, with the following key tasks: implement non-blocking `run` and `test`, fixing the remaining major bugs, migrate key sbt plugins, and provide documentation.
- **Stretch goal: Integrate Scala CLI into Scastie.**
  In 2024, we began integrating Scala CLI into Scastie to enable support for using directives in Scala code snippets. This year, we aim to complete the integration.
- **Stretch goal: Unify artifact publishing.**
  Currently, publishing workflows are implemented independently across various build tools, such as sbt, Scala CLI, and Mill. If resources allow, we aim to develop a common library to streamline and unify artifact publishing across these tools.

We will dedicate some of our time to supporting key stakeholders in the tooling ecosystem, including:

- JetBrains, on improving the support of Scala 3 in IntelliJ.
- VirtusLab and Akka, on improving the coverage support in Scala 3.
- VirtusLab, on improving Scaladoc.

Finally, we acknowledge that many more projects would deserve our attention but we do not have the capacity to support them.
Notably, but not exclusively, this includes Coursier, Scalafix, and Scaladex.

### Community and Contributor Experience

The Scala Center stays committed to its mission of supporting and developing the Scala community.
In 2025, we will focus on:

- **Google Summer of Code 2025.**
  We are applying to be a part of the program again, helping new Scala programmers get a head start in their careers while bringing fresh contributions to established community projects.
- **Scala Advent of Code 2025.**
  Many Scala developers like to participate to the annual Advent of Code event.
  Each year, we set up a platform where participants using Scala can share their solutions, with articles showcasing how Scala helped them solve the puzzles.
- **TODO Check this: Scala Ambassador Program.**
  Historically, the Scala Center has been involved in the organization of a wide variety of events, from sprees to conferences.
  With the Scala Ambassador Program, we are looking to transfer that experience to the Scala Communities all around the world.
  The Scala Ambassador Program will be a combination of a toolkit giving local community leaders a playbook of how to organize an event, as well as an outreach program to find early adopters of the program and help galvanize local communities.

## Conclusion

In this article, we have looked at the pillars of the Scala ecosystem, and for each of them we have listed our main goals for 2025.

Thanks to your support, and with the help of all the [people behind Scala](https://www.scala-lang.org/community/#whos-behind-scala), we came this far!
Help us go even further by [supporting the Scala Center](https://scala.epfl.ch/faqs.html).

You can find our detailed roadmap for the current quarter [here](https://scala.epfl.ch/projects.html), and track our progress by looking at our [quarterly reports](https://scala.epfl.ch/records.html), or by browsing the [Scala Center Updates](https://contributors.scala-lang.org/c/scala-center/25) category of the Scala Contributors forum.
