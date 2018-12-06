# iriscli gov query-votes

## 描述

查询指定提议的投票情况

## 使用方式

```
iriscli gov query-votes [flags]
```
打印帮助信息:

```
iriscli gov query-votes --help
```

## 标志

| 名称, 速记       | 默认值                      | 描述                                                                                                                                                 | 是否必须  |
| --------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| --proposal-id   |                            | [string] 提议ID                                                                                                        | Yes      |

## 示例

### 查询投票

```shell
iriscli gov query-votes --chain-id=test --proposal-id=1
```

查询指定提议的所有投票情况。
 
```txt
[
  {
    "voter": "faa14q5rf9sl2dqd2uxrxykafxq3nu3lj2fp9l7pgd",
    "proposal_id": "1",
    "option": "Yes"
  }
]
```
