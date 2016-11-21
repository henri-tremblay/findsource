To reproduce (https://youtrack.jetbrains.com/issue/IDEA-164137).

With IntelliJ 2016.2.5 Ultimate

First compile the `lib` project

```bash
pushd lib
mvn install
popd
```

Then create a project from `main`.

Open `App.java`
Cmd+B on `MyCode` in the class

This will open `MyCode.class`. All normal, the sources are not available.

Now click on "Scroll to source". It will do nothing.

If would expect to be taken to `External Libraries->Maven: pro.tremblay:lib:1.0-SNAPSHOT-> pro.tremblay -> MyCode` like
it would do if the source code was available.
