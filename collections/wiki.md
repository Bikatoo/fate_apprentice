# Java集合体系-collection(局部)

![collection](collection_frame.jpg)

### Iterable
> 定义可`for each loop`的对象   
> 提供以下功能接口定义   
> iterator(): <a href="#iterator">Iterator</a> 返回泛型定义类型的迭代器   
> [JDK8]forEach(Consumer action): void (对集合元素)按迭代顺序执行给定的操作
> spliterator(): Spliterator 返回泛型定义类型的拆分器

### <a name="iterator">Iterator</a>
> 迭代器   
> 提供了一下功能接口定义   
> hasNext(): boolean 是否存在下一个元素   
> next(): E 返回下一个元素   
> remove(): void 删除迭代器当前位置的元素   
> [JDK8] forEachRemaining(Consumer action): void 按顺序执行给定操作    

