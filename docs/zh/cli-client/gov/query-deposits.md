# iriscli gov query-deposits

## 描述

查询指定提议的押金详细情况

## 使用方式

```
iriscli gov query-deposits [flags]
```
打印帮助信息:

```
iriscli gov query-deposits --help
```
## 标志

| 名称, 速记       | 默认值                      | 描述                                                                                                                                                 | 是否必须  |
| --------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| --proposal-id   |                            | [string] 提议ID                                                                                                        | Yes      |

## 示例

### 查询所有押金

```shell
iriscli gov query-deposits --chain-id=test --proposal-id=1
```

你可以查询到指定提议所有抵押的token，包括每个抵押人的充值详情。

```txt
[
  {
    "depositor": "faa1c4kjt586r3t353ek9jtzwxum9x9fcgwetyca07",
    "proposal_id": "1",
    "amount": [
      {
        "denom": "iris-atto",
        "amount": "35000000000000000000"
      }
    ]
  }
]
```
