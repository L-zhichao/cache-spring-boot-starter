# cache-spring-boot-starter
封装redis缓存查询组件

 > 该组件是基于springboot实现于redis查询过程的二次分装。将二重判断、缓存穿透等一些常见问题直接进行封装，来业务此操作中重视业务逻辑而无需进行关注这些重复代码操作






## Feature
  * 内置布隆过滤器实现安全读取数据，防止缓存穿透问题。
  * 利用CacheLoader参数在获取数据时直接传入数据sql查询，在缓存不存在时直接做查询并添加缓存。





## How To Use
  1. 将组件下载到本地后以模块的形式导入到项目中。
  2. 在业务模块中需要的类中直接将`DistributedCache`对象注入进来。
  3. 调用`DistributedCache`#getInstance()方法获取对象。
