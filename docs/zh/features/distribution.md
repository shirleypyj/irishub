# distribution模块的用户手册

## 简介

该模块负责将收集的交易费和虚增的token分发给所有验证人和委托人。为了减少计算压力，引入了一种惰性分配策略。`惰性`意味着不会直接向贡献者自动支付利益。委托人或者验证人必须手动发送交易以取回其收益，否则，他们的收益将保留在全局收益池中。

## 使用场景

1. 设置收益取回地址

	委托人可能有多个irishub钱包地址。假设其中一个钱包(标记为`B`)有许多token，并且一部分token已被委托给验证人。委托人可能希望所得收益可以支付给另一个钱包，因此委托人可以清楚明白的知道有多少收益。但是，默认情况下，收益将支付给发送委托交易的钱包。如果要将另一个钱包(标记为`B`)设置为支付收益的地址，委托人需要从钱包`A`发送另一个交易。参考命令：
	```bash
    iriscli distribution set-withdraw-addr [address of wallet B] --fee=0.004iris --from=[key name of wallet A] --chain-id=[chain-id]
    ```  
    如果想验证设置取回地址是否成功，可以查询一下收益地址：参考命令：
    ```bash
    iriscli distribution withdraw-address [address of wallet A]
    ```
    如果返回结果就是钱包`B`的地址，那么设置取回地址成功。
	
2. 取回收益

	根据之前的叙述，我们的收益不会自动支付给我们的钱包，我们必须发送交易以提取收益。假设一个委托人自己有一个一个验证节点(标记为`validatorA`)，也就是说这个委托人也是验证人；此外，它在其它两个验证人上还有委托(两个验证人标记为`validatorB`和`validatorC`)。所有委托均由钱包A创建。
	1. 仅取回在验证人`validatorA`上的委托收益:
        ```bash
        iriscli distribution withdraw-rewards --only-from-validator [address of validatorA] --from [key name of wallet A] --fee=0.004iris --chain-id=[chain-id]
        ```
    2. 取回在所有验证人上的委托收益:
        ```bash
        iriscli distribution withdraw-rewards --from [key name of wallet A] --fee=0.004iris --chain-id=[chain-id]
        ```
    3. 取回所有委托产生的收益和自己验证人赚取的佣金:
        ```bash
        iriscli distribution withdraw-rewards --is-validator=true --from [key name of wallet A] --fee=0.004iris --chain-id=[chain-id]
        ```

3. 查询收益

    Execute the command to get the earned tokens:
    ```bash
    iriscli bank account [withdraw address]
    ```
