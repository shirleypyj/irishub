# iriscli stake

## 介绍

Stake模块提供了一系列查询staking状态和发送staking交易的命令

## 用法

```
iriscli stake [subcommand]
```

打印子命令和flags：
```
iriscli stake --help
```

## 子命令

| 子命令                                                          | 功能                                                          |
| ------------------------------------------------------------- | --------------------------------------------------------------|
| [validator](validator.md)                                     | 查询某个验证者 |
| [validators](validators.md)                                   | 查询所有的验证者 |
| [delegation](delegation.md)                                   | 基于委托者和验证者地址查询委托交易 |
| [delegations](delegations.md)                                 | 查询某个委托者发起的所有委托记录 |
| [unbonding-delegation](unbonding-delegation.md)               | 基于委托者地址和验证者地址的unbonding-delegation记录查询 |
| [unbonding-delegations](unbonding-delegations.md)             | 基于委托者地址的所有unbonding-delegation记录查询 |
| [unbonding-delegations-from](unbonding-delegations-from.md)   | 基于验证者地址的所有unbonding-delegation记录查询|
| [redelegations-from](redelegations-from.md)                   | 基于某一验证者的所有转委托查询  |
| [redelegation](redelegation.md)                               | 基于委托者地址，原验证者地址和目标验证者地址的转委托记录查询 |
| [redelegations](redelegations.md)                             | 基于委托者地址的所有转委托记录查询 |
| [pool](pool.md)                                               | 查询最新的权益池 |
| [parameters](parameters.md)                                   | 查询最新的权益参数信息 |
| [signing-info](signing-info.md)                               | 查询验证者签名信息 |
| [create-validator](create-validator.md)                       | 以自委托的方式创建一个新的验证者 |
| [edit-validator](edit-validator.md)                           | 编辑已存在的验证者信息 |
| [delegate](delegate.md)                                       | 委托一定token到某个验证者 |
| [unbond](unbond.md)                                           | 从指定的验证者解绑一定的token份额 |
| [redelegate](redelegate.md)                                   | 从一个验证者转委托一定的token到另一个验证者 |
| [unjail](unjail.md)                                           | 恢复之前由于宕机被惩罚的验证者的身份 |

