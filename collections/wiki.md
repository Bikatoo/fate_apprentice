# Java集合体系-collection(局部)

![collection](collection_frame.jpg)

### Iterable
##### 定义可`for each loop`的对象   
> 提供以下功能接口定义：   
>>+ iterator(): <a href="#iterator">Iterator</a> 返回泛型定义类型的迭代器   
>>+ [JDK8]forEach(Consumer): void (对集合元素)按迭代顺序执行给定的操作
>>+ spliterator(): Spliterator 返回泛型定义类型的拆分器

### Collection
##### 集合框架的根接口，具有最大通用性
> 提供一下功能接口定义：   
>+ size(): int 获取集合中的元素数   
>+ isEmpty(): boolean 集合中是否无元素   
>+ <a name="contains">contains(Object): boolean</a> 集合中是否存在(o == null ? e == null : o.equals(e))给定元素   
>+ toArray(): Object[] 返回包含集合中所有元素的数组，如集合保证迭代顺序，则返回的数组也`保证迭代顺序`；返回的数组为`新数组`(非集合本身底层数据结构)，对数组的操作不影响原集合   
>+ toArray(T[]): T[] 返回包含集合中所有元素的数组，返回数组的元素类型与给定数组元素类型一致；给定数组长度不足时分配新的数组；足够容纳时返回给定数组，空闲位置填充null   
>+ add(E): boolean 添加元素到集合中，集合因此发生变化时返回true；因一些限制而无效更新时返回false    
>+ remove(Object): boolean 从集合中删除给定元素(如果<a herf="#contains">存在</a>多个，删除第一个)

### <a name="iterator">Iterator</a>
##### 迭代器   
>提供了以下功能接口定义：   
>>+ hasNext(): boolean 是否存在下一个元素   
>>+ next(): E 返回下一个元素   
>>+ remove(): void 删除迭代器当前位置的元素   
>>+ [JDK8] forEachRemaining(Consumer): void 按顺序执行给定操作    

