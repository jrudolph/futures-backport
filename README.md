This project contains classes added to the Scala library to the `scala.concurrent` package between
Scala 2.9.2 and 2.9.3 (SIP-14 backport).

See the license of the original code in LICENSE-scala.

When to use
-----------

If for some reason you need to use the Scala library version 2.9.2 at runtime at can't
refrain from using classes from `scala.concurrent` like `Future`.

Usage
-----

Add

```scala
libraryDependencies += "net.virtual-void" %% "futures-backport" % "1"
```

to your build. To use it with cross-building add these setting:

libraryDependencies <++= scalaVersion {
  case "2.9.2" => Seq("net.virtual-void" %% "futures-backport" % "1")
  case _ => Nil
}
