# Aesth Style Guidelines

## Labels

Environment or Static Variable - `__context__` (for dynamic context parameters) or `__CONTEXT__` (for static context settings)
Constant - `ALL_CAPITALS`
Variable or Property - `camelCase`
Hidden Property - `_camelCase`
Function or Feature - `camelCase`
Hidden Feature - `__camelCase`
Class or Object - `PascalCase`

## Spaces

With both comma (`,`) and (`:`), the spaces comes after and not before.

If there is just one token, keep it inline and add space on both sides, e.g.`( label )` or `[ label ]` or `{ label }`.

If there are many, go multiline and indent, e.g.
```
{
    instructionA,
    instructionB,
    ...
}
```

## _No semi-colon (;) at the end of instructions_, it is UGLY.

