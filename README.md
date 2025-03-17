1.Relative Stability:Anchored or Pegged -$1.00
    1.Chainlink Price feed.
    2.Set a function to exchange ETH BTC -$$
2.Stability Mechanism (Minting):Algorithmic (Decentralized)
1.People can only mint the stablecoin with enough collateral (coded)
3.Collateral:Exogenous (Crypto)
1.WETH（Wrapped Ether 封装的 ETH.通过一个简单的封装过程（将 ETH 转换为 WETH）使 ETH 成为一种符合 ERC-20 标准的代币。）
2.WBTC

    - 计算健康因子
    - 注意稳定币是0的情况

一些知识点：

- 两种测试
  - invariant 测试
    - invariant: 系统 always hold 的 property。（stateful fuzz testing）
  - 模糊测试（stateless fuzz testing）
- 更安全的 OracleLib

待进行：

1. 当外界代币与美元汇率修改时，系统会崩（抵押的资产有可能小于代币价值）怎么办？
   - 自动清算？销毁指定的代币？哇哦，难不成自动平仓
2. 完善测试例。

   - 比如对于 view 类型的 get 方法
   - 完善 DSCEngine 与 DecentralizedStableCoin 的测试覆盖率

3. OracleLib 中方法再了解一下
4. 参考 github，探索对于 continueOnRevert 与 failOnRevert 的写法。
