# (1)minibus的任务编号？
## (1.1)event的分库分表
在分布式系统中，分库分表会经常被使用到，那么就会导致minibus依赖的事件表（minibus_event）也可能是分库分表的，比如
> * minibus_event_0000
> * minibus_event_0002
> * minibus_event_0003
> * minibus_event_xxxx
> * minibus_event_0511

## (1.2)任务编号
通过对分库分表的定义，抽象下minibus_event分表的编码如下：
> * 0
> * 1
> * 2
> * 3
> * x
> * 511

# (2)编号管控的解决方案？
## (2.1)轻量级解决方案：利用DB乐观锁按序管控任务编号


## (2.2)