# Golden_Number
## 比赛规则
* 假设有M个玩家，P1,P2,…Pm
* 在 (0-100) 开区间内，所有玩家自由选择两个正有理数数字提交（可以相同或者不同）给服务器，假设N11,N12,N21,N22,Nm1,Nm2
* 等M*2个数字都提交后，服务器做如下计算 (N11+N12+N21+N22+…+Nm1+Nm2)/(M*2)*0.618 = GN
* 由此得到黄金点数字GN
* 查看所有玩家提交的数字与GN的算术差的绝对值，值最小者得分，值最大者扣分。其它玩家不得分
* 此回合结束，进行下一回合，多回合后，累计得分高者获胜
## 计分规则
* M个玩家比赛时，每轮离GN最近的玩家得M分，最远的扣2分，其它玩家不得分
* 如果一个玩家在一轮内提交两个相同的数字并得分时，只计一次分
* 多个玩家在一轮内同时离GN最近时，每个玩家都得M分
## 程序要求
输入格式：
Bot程序需从标准输入读取数据，第一行两个数表示下面有两行数据，每行数据有5个值。后面每行代表一轮比赛的数据，最后一行是最新一轮的数据。行中第一个数据是该轮的黄金点值，后面第2N个数和第2N+1个数是第N个bot输出的预测值，数据之间以制表符分隔。如果某个值为0，表示该bot在该轮超时未提交数据或输出数据非法，不在(0,100)之间​
格式举例：
2 5
18.07 30 30 17 40
24.87 18.08 18.08 99.9 25
 
输出格式：
输出（0, 100）中的两个数，以制表符\t分割。格式非法或5秒内没有输出，即认为此玩家放弃本轮比赛，只在剩余玩家中计算G值
格式举例：
12.34 56.78
