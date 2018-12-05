# iriscli stake redelegation

## 描述

基于委托者地址，源验证者地址和目标验证者地址的转委托记录查询 

## 用法

```
iriscli stake redelegation [flags]
```
打印帮助信息
```
iriscli stake redelegation --help
```

## 特有的flags

| 名称, 速记                  | 默认值                      | 描述                                                                | 必需     |
| -------------------------- | -------------------------- | ------------------------------------------------------------------- | -------- | 
| --address-delegator        |                            | [string] 委托者bech地址                                              | Yes      |
| --address-validator-dest   |                            | [string] 目标验证者bech地址                                          | Yes      |
| --address-validator-source |                            | [string] 源验证者bech地址                                            | Yes      |

## 示例

查询转委托记录
```
iriscli stake redelegation --address-validator-source=SourceValidatorAddress --address-validator-dest=DestinationValidatorAddress --address-delegator=DelegatorAddress
```

运行成功以后，返回的结果如下：

```txt
Redelegation
Delegator: faa10s0arq9khpl0cfzng3qgxcxq0ny6hmc9sytjfk
Source Validator: fva1dayujdfnxjggd5ydlvvgkerp2supknthajpch2
Destination Validator: fva1h27xdw6t9l5jgvun76qdu45kgrx9lqede8hpcd
Creation height: 1130
Min time to unbond (unix): 2018-11-16 07:22:48.740311064 +0000 UTC
Source shares: 0.1000000000
Destination shares: 0.1000000000
```
