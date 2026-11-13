# 业务资料约定

revenue单位百万元，null代表未提供而非0；needs是类别集合。group为企业集团隔离与稳定性抽样键，不是已有服务组答案。constraints中的same/different是必须满足的人工业务约束。

每行id在该表内唯一，文件顺序不代表业务事件顺序。清单schema=1，各表登记文件名、字节长度、SHA256、行数及完整字段集合，未知版本或内容变化应重新登记。金额及测量数值均为独立资料，不代表任何现实机构的经营数据。

- customers：id、group、revenue、sector、needs。
- constraints：id、left、right、kind。
- capacity：id、min_groups、max_groups、min_members、max_members。

normal与boundary是相互独立的资料包，不能直接拼接重复id。引用字段按本项目domain.py的REFERENCES登记。读取检查只检查完整性、身份及这些直接引用，不替代领域分析中的可识别性、时点可见性或可行性判断。
