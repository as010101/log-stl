?[heap算法](# heap算法)
# log-stl
# 临时对象的产生与运用

​    临时对象 （易造成效率上的负担   用得当可以使得程序干净清爽）stl最常将此技巧运用于算法与仿函数（for_each 情形   p36）

# increment /decrement / dereference 操作符

 increment /dereference在迭代器的实现上占用非常重要的地位，因为任何一个迭代器都必须实现前进和取值功能(p 37)

# function call 操作符

（p40）

# 优先队列（priority queue）

允许用户以任何次序将任何元素推入容器中，但取出时一定是从优先权最高（也就是数值最高）的元素开始取，binary  max heap 正是具有这样的特性，适合作为priority queue的底层机制（p172）

# heap算法

push_heap  将元素推入堆结构最底层最后，然后执行上溯（percolate up），直至满足堆结构

pop_heap   将堆顶元素推出，然后取堆结构最底层最后元素放入堆顶，执行下溯（percolate down），直至满足堆结构，（侯书中是这样做的，删除后，取被删除元素的字节点中较大者到被删除处，这样子节点的一个位置就空出来了，然后将堆结构最底层最后元素放入空出的位置，执行执行下溯（percolate down），直至满足堆结构，这样的算法对那些，要求共享堆结构数据的或许比较好用）

# stack

stack借由底层container（dequeue）修改其接口，形成另一种风貌，即可得到stack,这种新结构并没有做诸如分配内存这种复杂的操作，因而称作Adapter

因stack只需满足先进后出，及推入弹出功能，无需遍历这种功能，在设计stack结构时便没有提供遍历元素这一接口，故stack,从表层上，不提供走访功能，不提供迭代器	

# set与map键值之区别

set  的键值与元素为相同的值，故其元素值干系到其元素的排列顺序，如果任意更改set值，会严重破坏set组织

map的所有元素都会根据元素的键值自动排序，map的元素类型是pair,不能更改其key，但可更改其value

由于这两种结构的性质决定了其容器类型属于关联性容器，故这两种结构都要有key,将key挂于RB-tree中，依靠RB-tree实现高效的查找、删除， 



# 测试array vector

.1.  array vector元素的访问 a.at(i)  i为int   从0开始

2.  auto对vector来说 测试得出 并未完全遍历
3. sizeof(arr)/sizeof(*arr)
4. std::endl 
5. sort 为排序  默认只有两个参数





