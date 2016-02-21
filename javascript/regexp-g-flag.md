# The RegExp g flag

The `g` flag is evil. It makes a `RegExp` instance inpure. When you `RegExp.exec` on such a `RegExp` it'll set a `lastIndex` property inside the instance. The next time you `exec` on it, the engine will start searching the passed string from `lastIndex`. This is pretty bad IMO. So **dont't use the `RegExp` `g` flag**.

