# Vue3

## vue3响应式
推荐使用ref 而不是reactive

#### reactive和 ref 对比

| reactive                                | ref                                                       |
|-----------------------------------------|-----------------------------------------------------------|
| X 只支持对象和数组(引用数据类型)         | √ 支持基本数据类型+引用数据类型                            |
| √ 在script 和 template 中无差别使用    | X 在 script 和 template 使用方式不同(script中要 .value) |
| X 重新分配一个新对象会丢失响应性          | √ 重新分配一个新对象不会失去响应                            |
| 能直接访问属性                          |  需要使用 .value 访问属性                                  |
| X 将对象传入函数时,失去响应              | √ 传入函数时,不会失去响应                                  |
| X 解构时会丢失响应性,需使用toRefs        | X 解构对象时会丢失响应性,需使用toRefs                      |