execute using [glci](https://github.com/firecow/gitlab-ci-local) `gitlab-ci-local --stage build`, change first `mill -i` to mill or remove `COURSIER_CACHE` make it works

```
build_branch starting eclipse-temurin:17 (build)
build_branch copied to docker volumes in 378 ms
build_branch $ find .cache/coursier -type d -name "*-SNAPSHOT" -print -exec rm -rf '{}' \; || true
build_branch > find: ‘.cache/coursier’: No such file or directory
build_branch $ find out/ -maxdepth 1 -type d -name "mill-worker-*" -print -exec rm -rf '{}' \; || true
build_branch > find: ‘out/’: No such file or directory
build_branch $ ./mill -i mill.scalalib.scalafmt.ScalafmtModule/checkFormatAll __.sources || true
build_branch > Downloading mill 0.12.2 from https://repo1.maven.org/maven2/com/lihaoyi/mill-dist/0.12.2/mill-dist-0.12.2.jar ...
build_branch >   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
build_branch >                                  Dload  Upload   Total   Spent    Left  Speed
build_branch > still running...
build_branch > still running...
100 64.6M  100 64.6M    0     0  3160k      0  0:00:20  0:00:20 --:--:-- 9205k
build_branch > Preparing Java 17.0.8.1 runtime; this may take a minute or two ...
build_branch > ============================= mill.scalalib.scalafmt.ScalafmtModule/checkFormatAll __.sources ========================
build_branch > ======================================================================================================================
build_branch > [build.mill-58/62] compile
build_branch > [build.mill-58] [info] compiling 4 Scala sources to /gcl-builds/out/mill-build/compile.dest/classes ...
build_branch > [build.mill-58] [info] done compiling
build_branch > [5/5] mill.scalalib.scalafmt.ScalafmtModule.checkFormatAll
build_branch > [5] Checking format of 2 Scala sources
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalafmt-core_2.13/3.8.2/scalafmt-core_2.13-3.8.2.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-reflect/2.13.13/scala-reflect-2.13.13.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-reflect/2.13.13/scala-reflect-2.13.13.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalafmt-core_2.13/3.8.2/scalafmt-core_2.13-3.8.2.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.13/scala-library-2.13.13.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalafmt-config_2.13/3.8.2/scalafmt-config_2.13-3.8.2.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalameta_2.13/4.9.6/scalameta_2.13-4.9.6.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/mdoc-parser_2.13/2.5.2/mdoc-parser_2.13-2.5.2.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalafmt-sysops_2.13/3.8.2/scalafmt-sysops_2.13-3.8.2.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.13/scala-library-2.13.13.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/mdoc-parser_2.13/2.5.2/mdoc-parser_2.13-2.5.2.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalafmt-sysops_2.13/3.8.2/scalafmt-sysops_2.13-3.8.2.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalameta_2.13/4.9.6/scalameta_2.13-4.9.6.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalafmt-config_2.13/3.8.2/scalafmt-config_2.13-3.8.2.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/modules/scala-parallel-collections_2.13/1.0.4/scala-parallel-collections_2.13-1.0.4.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/geirsson/metaconfig-core_2.13/0.12.0/metaconfig-core_2.13-0.12.0.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/parsers_2.13/4.9.6/parsers_2.13-4.9.6.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scalap/2.13.14/scalap-2.13.14.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.14/scala-library-2.13.14.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/geirsson/metaconfig-typesafe-config_2.13/0.12.0/metaconfig-typesafe-config_2.13-0.12.0.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/modules/scala-parallel-collections_2.13/1.0.4/scala-parallel-collections_2.13-1.0.4.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/geirsson/metaconfig-typesafe-config_2.13/0.12.0/metaconfig-typesafe-config_2.13-0.12.0.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/geirsson/metaconfig-core_2.13/0.12.0/metaconfig-core_2.13-0.12.0.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scalap/2.13.14/scalap-2.13.14.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.14/scala-library-2.13.14.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/parsers_2.13/4.9.6/parsers_2.13-4.9.6.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/typesafe/config/1.4.1/config-1.4.1.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/geirsson/metaconfig-pprint_2.13/0.12.0/metaconfig-pprint_2.13-0.12.0.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/trees_2.13/4.9.6/trees_2.13-4.9.6.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/typelevel/paiges-core_2.13/0.4.3/paiges-core_2.13-0.4.3.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-compiler/2.13.14/scala-compiler-2.13.14.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/modules/scala-collection-compat_2.13/2.11.0/scala-collection-compat_2.13-2.11.0.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/geirsson/metaconfig-pprint_2.13/0.12.0/metaconfig-pprint_2.13-0.12.0.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/typelevel/paiges-core_2.13/0.4.3/paiges-core_2.13-0.4.3.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/typesafe/config/1.4.1/config-1.4.1.pom                                                                                                                                                    18:11:25 [71/1243]
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-compiler/2.13.14/scala-compiler-2.13.14.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/modules/scala-collection-compat_2.13/2.11.0/scala-collection-compat_2.13-2.11.0.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/trees_2.13/4.9.6/trees_2.13-4.9.6.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/lihaoyi/fansi_2.13/0.4.0/fansi_2.13-0.4.0.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-reflect/2.13.14/scala-reflect-2.13.14.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/common_2.13/4.9.6/common_2.13-4.9.6.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/jline/jline/3.25.1/jline-3.25.1.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-reflect/2.13.14/scala-reflect-2.13.14.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/lihaoyi/fansi_2.13/0.4.0/fansi_2.13-0.4.0.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/common_2.13/4.9.6/common_2.13-4.9.6.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/jline/jline/3.25.1/jline-3.25.1.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/jline/jline-parent/3.25.1/jline-parent-3.25.1.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/jline/jline-parent/3.25.1/jline-parent-3.25.1.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/lihaoyi/sourcecode_2.13/0.4.2/sourcecode_2.13-0.4.2.pom
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/lihaoyi/sourcecode_2.13/0.4.2/sourcecode_2.13-0.4.2.pom
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalameta_2.13/4.9.6/scalameta_2.13-4.9.6.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/mdoc-parser_2.13/2.5.2/mdoc-parser_2.13-2.5.2.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/modules/scala-collection-compat_2.13/2.11.0/scala-collection-compat_2.13-2.11.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/geirsson/metaconfig-core_2.13/0.12.0/metaconfig-core_2.13-0.12.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/geirsson/metaconfig-typesafe-config_2.13/0.12.0/metaconfig-typesafe-config_2.13-0.12.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/lihaoyi/fansi_2.13/0.4.0/fansi_2.13-0.4.0.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/modules/scala-collection-compat_2.13/2.11.0/scala-collection-compat_2.13-2.11.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/trees_2.13/4.9.6/trees_2.13-4.9.6.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/mdoc-parser_2.13/2.5.2/mdoc-parser_2.13-2.5.2.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/jline/jline/3.25.1/jline-3.25.1.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/lihaoyi/fansi_2.13/0.4.0/fansi_2.13-0.4.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalafmt-sysops_2.13/3.8.2/scalafmt-sysops_2.13-3.8.2.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/geirsson/metaconfig-typesafe-config_2.13/0.12.0/metaconfig-typesafe-config_2.13-0.12.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/typesafe/config/1.4.1/config-1.4.1.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalafmt-sysops_2.13/3.8.2/scalafmt-sysops_2.13-3.8.2.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/modules/scala-parallel-collections_2.13/1.0.4/scala-parallel-collections_2.13-1.0.4.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/geirsson/metaconfig-core_2.13/0.12.0/metaconfig-core_2.13-0.12.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/lihaoyi/sourcecode_2.13/0.4.2/sourcecode_2.13-0.4.2.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalameta_2.13/4.9.6/scalameta_2.13-4.9.6.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/parsers_2.13/4.9.6/parsers_2.13-4.9.6.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/lihaoyi/sourcecode_2.13/0.4.2/sourcecode_2.13-0.4.2.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/common_2.13/4.9.6/common_2.13-4.9.6.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/typesafe/config/1.4.1/config-1.4.1.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-compiler/2.13.14/scala-compiler-2.13.14.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/jline/jline/3.25.1/jline-3.25.1.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/com/geirsson/metaconfig-pprint_2.13/0.12.0/metaconfig-pprint_2.13-0.12.0.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/parsers_2.13/4.9.6/parsers_2.13-4.9.6.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scalap/2.13.14/scalap-2.13.14.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/com/geirsson/metaconfig-pprint_2.13/0.12.0/metaconfig-pprint_2.13-0.12.0.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalafmt-config_2.13/3.8.2/scalafmt-config_2.13-3.8.2.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/modules/scala-parallel-collections_2.13/1.0.4/scala-parallel-collections_2.13-1.0.4.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.14/scala-library-2.13.14.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scalap/2.13.14/scalap-2.13.14.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/typelevel/paiges-core_2.13/0.4.3/paiges-core_2.13-0.4.3.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalafmt-config_2.13/3.8.2/scalafmt-config_2.13-3.8.2.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scala-lang/scala-reflect/2.13.14/scala-reflect-2.13.14.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/typelevel/paiges-core_2.13/0.4.3/paiges-core_2.13-0.4.3.jar
build_branch > [5] Downloading https://repo1.maven.org/maven2/org/scalameta/scalafmt-core_2.13/3.8.2/scalafmt-core_2.13-3.8.2.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/common_2.13/4.9.6/common_2.13-4.9.6.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/scalafmt-core_2.13/3.8.2/scalafmt-core_2.13-3.8.2.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-reflect/2.13.14/scala-reflect-2.13.14.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.14/scala-library-2.13.14.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scala-lang/scala-compiler/2.13.14/scala-compiler-2.13.14.jar
build_branch > [5] Downloaded https://repo1.maven.org/maven2/org/scalameta/trees_2.13/4.9.6/trees_2.13-4.9.6.jar
build_branch > [5] parsed config (v3.8.2): /gcl-builds/.scalafmt.conf
build_branch > [5] /gcl-builds/bar/qux/mymodule/src/BarQux.scala
build_branch > [5] /gcl-builds/foo/src/Foo.scala
build_branch > [5/5] ======================= mill.scalalib.scalafmt.ScalafmtModule/checkFormatAll __.sources ==================== 21s
build_branch > ======================================================================================================================
build_branch > 1 tasks failed
build_branch > mill.scalalib.scalafmt.ScalafmtModule.checkFormatAll Found 2 misformatted files
build_branch $ ./mill -i clean
build_branch > ========================================================== clean =====================================================
build_branch > ======================================================================================================================
build_branch > still running...
build_branch > [build.mill-58/62] compile
build_branch > [build.mill-58] [info] compiling 4 Scala sources to /gcl-builds/out/mill-build/compile.dest/classes ...
build_branch > [build.mill-58] [error] /gcl-builds/out/mill-build/generateScriptSources.dest/build_/bar/qux/package.mill:22:7: `override` modifier required to override concrete member:
build_branch > [build.mill-58] [error] override def ivyDeps: mill.T[mill.Agg[mill.scalalib.Dep]] (defined in trait JavaModule)
build_branch > [build.mill-58] [error]   def ivyDeps = Agg(ivy"com.lihaoyi::scalatags:0.8.2")
build_branch > [build.mill-58] [error]       ^
build_branch > [build.mill-58] [error] /gcl-builds/out/mill-build/generateScriptSources.dest/build_/foo/package.mill:17:7: `override` modifier required to override concrete member:
build_branch > [build.mill-58] [error] def moduleDeps: Seq[mill.scalalib.JavaModule] (defined in trait JavaModule)
build_branch > [build.mill-58] [error]   def moduleDeps = Seq(build.bar.qux.mymodule)
build_branch > [build.mill-58] [error]       ^
build_branch > [build.mill-58] [error] /gcl-builds/out/mill-build/generateScriptSources.dest/build_/foo/package.mill:18:7: `override` modifier required to override concrete member:
build_branch > [build.mill-58] [error] override def ivyDeps: mill.T[mill.Agg[mill.scalalib.Dep]] (defined in trait JavaModule)
build_branch > [build.mill-58] [error]   def ivyDeps = Agg(ivy"com.lihaoyi::mainargs:0.4.0")
build_branch > [build.mill-58] [error]       ^
build_branch > [build.mill-58] [error] /gcl-builds/out/mill-build/generateScriptSources.dest/build_/foo/package.mill:21:8: object package_ inherits conflicting members:
build_branch > [build.mill-58] [error]   def moduleDeps: Seq[mill.scalalib.JavaModule] (defined in trait JavaModule) and
build_branch > [build.mill-58] [error]   def moduleDeps: Seq[build_.package_.bar.qux.mymodule.type] (defined in class package_)
build_branch > [build.mill-58] [error]   (note: this can be resolved by declaring an `override` in object package_.);
build_branch > [build.mill-58] [error]  other members with override errors are: ivyDeps
build_branch > [build.mill-58] [error] object package_ extends package_ {
build_branch > [build.mill-58] [error]        ^
build_branch > [build.mill-58] [error] four errors found
build_branch > [62/62] ================================================== clean ================================================= 13s
build_branch > ======================================================================================================================
build_branch > 1 tasks failed
build_branch > compile Compilation failed
build_branch finished in 1.02 min  FAIL 1
build_branch Running after script...
build_branch $ find .cache/coursier -type d -name "*-SNAPSHOT" -print -exec rm -rf '{}' \; || true
build_branch > find: ‘.cache/coursier’: No such file or directory
build_branch $ find out/ -maxdepth 1 -type d -name "mill-worker-*" -print -exec rm -rf '{}' \; || true
```
