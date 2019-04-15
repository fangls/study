# study记录平时的学习内容
#修改第一次的内容
第二次修改
123
1月8日 15:19

```js
 service {
  #vgroup->rgroup
  vgroup_mapping.my_test_tx_group = "default"
  #配置Client连接TC的地址
  default.grouplist = "127.0.0.1:8091"
  #degrade current not support
  enableDegrade = false
  #disable
  是否启用seata的分布式事务
  disableGlobalTransaction = false
}
```

业务流程
 * 正常流程
   1.business发起购买请求
   2.storage扣减库存
   3.order创建订单
   4.account扣减余额
 * 异常流程
   1.business发起购买请求
   2.storage扣减库存
   3.order创建订单
   4.account`扣减余额异常`
