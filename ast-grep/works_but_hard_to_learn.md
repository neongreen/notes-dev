# works but hard to learn


Testing patterns:

    sg run --pattern 'import Foo(Bar)' --debug-query --lang=haskell X

This will show how a piece of code is parsed.

Even using ast-grep as a simple grep is impossible (?) without writing patterns in yaml,
because patterns are parsed as AST and smth like 'Bar' will not match Bar in type signatures
etc.

Example of what I came up with:

```
sg scan --inline-rules '
id: _
language: haskell
rule:
  any:
    - pattern:  # Find all mentions of Bar in signatures
        selector: name
        context: "x :: X.Bar"
    - kind: name  # Find all imports of Bar
      regex: "^Bar$"
      inside:
        kind: import_list
        stopBy: end
' **/*.hs
```

And you have to run this with the cmd+enter 'send to terminal' and iterate on it.

The docs document everything *but* are not helpful.
