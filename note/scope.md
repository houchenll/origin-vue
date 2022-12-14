## 作用
Add "scoped" attribute to limit CSS to this component only

## 父子节点之间
背景：父子节点各有一个 h1 标签，使用相同样式 scope-title

|  | 都无scope | 子有scope    | 父有scope    | 都有scope |
|--------|---------|------------|------------| --- |
| 都无样式   | 默认样式    | 默认样式       | 默认样式       |默认样式|
| 父节点有样式 | 父样式     | 父样式        | 父父样式，子默认样式 |父父样式，子默认样式|
| 子节点有样式 | 子样式     | 父默认样式，子子样式 | 子样式        |父默认样式，子子样式|
| 都有样式   | 父样式     | 父父样式，子子样式  |父父样式，子子样式|父父样式，子子样式|

总结：  
* 当没有 scope 时，父节点样式可作用在子节点上，子节点样式也可作用在父节点上，父样式覆盖子样式
* 当有 scope 时，父、子节点样式只作用在自身
* scope 样式的优先级高于父、子节点作用来在样式


## 兄弟节点之间
| 都无scope | 左有scope | 右有scope | 都有scope |
|---------|---------|---------|---|
| 都无样式    ||||
| 左节点有样式  ||||
| 右节点有样式  ||||
| 都有样式    ||||