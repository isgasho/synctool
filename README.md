# synctool

#一个p2p的多节点的文件同步程序

    使用golang实现的同步程序,该程序以p2p的架构运行,在集群中的节点定期交换文件元数据,
    以此来保证程序运行中，每个节点都可以保证自己本地的数据都是最新的
  
#程序中使用的技术:
    基于libp2p实现节点间的通信
    数据的序列化和反序列化使用的是protocol buffer 
    程序使用额外的逻辑层在监视文件时，并为文件生成index ,和一系列的
    indexUpdate ,来描述文件的变化.
    
    使用golang的http包来实现与用户进行交互的功能

