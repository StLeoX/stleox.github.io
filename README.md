## StLeoX's HomePage

### Why "StLeoX"?

"StLeoX" stands for "St.Leo.X", which means "Always seeking for inner peace."

### Branch Managing

#### `local/ign` branch

`local/ign` 是 `main` 的超集，包含了一些非公开内容，该分支需要定期合入 `main` 的内容。
由于非 `ign-*` 的变更统一提交到 `main` 分支，所以该合并过程是单向的，不应该存在冲突。

#### `local/wip` branch

`local/wip` 的内容是 `main` 的预备状态，`wip-*` 的变更统一提交到 `local/wip`
分支，再合入 `main` 分支，该过程也不应该存在冲突。