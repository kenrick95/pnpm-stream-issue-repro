# pnpm stream issue

##  this is ok

```
pnpm --stream --filter alfa --filter beta lint
```

Expected & actual:

```
Scope: 2 of 3 workspace projects
packages/alfa lint$ echo 'ok'
packages/alfa lint: ok
packages/alfa lint: Done
```

## this is not ok

```
pnpm --stream --filter alfa lint
```

Expected:

```
Scope: 1 of 3 workspace projects
packages/alfa lint$ echo 'ok'
packages/alfa lint: ok
packages/alfa lint: Done
```

Actual:

```

> alfa@1.0.0 lint /path/to/repo/packages/alfa
> echo 'ok'

ok
```
