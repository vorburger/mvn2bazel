Maven to Bazel how to (mvn2bazel)
=================================

This document is a brain dump of ideas for as-much-as-possible "in an ideal world" automated Maven to Bazel migration.

This should ultimately permit migrating a complex real world project such as git.OpenDaylight.org's build system to Bazel.

It may evolve into a more formal spec for such a project.

- [X] build using external Maven repo deps? DONE, see examples/java-maven/WORKSPACE

- [ ] generate maven_jar rules from POM in preparation? https://docs.bazel.build/versions/master/generate-workspace.html but https://github.com/bazelbuild/migration-tooling/issues/47

- [ ] _Eclipse plugin_

- [ ] automatically find *Test classes instead of explicit listing like in examples/java-maven/BUILD java_test test_class

- [ ] generate maven_jar rules from POM on the fly

- [ ] Checkstyle?

- [ ] error-prone

- [ ] SpotBugs

- [ ] custom (YANG) code generator

- [ ] mvn install (deploy?) from Bazel, for integration with external still-Maven builds

- [ ] run some sub-modules still under Maven, during migration (ideally using Maven server)

- [ ] JavaDoc

- [ ] karaf-maven-plugin

- [ ] wraper script "mvn <goal>" -> "bazel build //`PWD`[?]/<goal>"

- [ ] target/bazel/... instead of polluting root directory
