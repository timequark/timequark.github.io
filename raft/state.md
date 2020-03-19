# Raft源码分析（一） - State

State 是 raft 的核心类，封装了框架性的性重要操作，持有Node (server.py)、Log、FileStorage、StateMachine对象；以及  Role 	角色，完成 Leader/Follower/Candidate 之间的转换。

BaseRole的构造方法，将传入State对象。

State 是上下文，将网络、Role转换、Log、FileStorage、StateMachine串联起来。

以下是**State类图**:

![](https://timequark.github.io/raft/img/state.jpg)

（可以下载看大图~）



可以看出，State 是整个系统中的核心引擎类，衔接了Network、Node、Role（包括Leader/Follower/Candidate）、Log、StateMachine、FileStorage 等各个对象之前的联系。



## State源码分析

##### state.py





[下一篇](https://timequark.github.io/raft/role )
