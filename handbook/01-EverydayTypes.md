# EverydayTypes

-   基础数据类型 `string` `number` `boolean`

    ```typescript
    const name: string = '迷心whylost'
    const age: number = 25
    const male: boolean = true
    ```

-   数组 e.g. `string[]` **_or_** `Array<string>`

    ```typescript
    const heroes: string[] = ['法外狂徒张三', '电瓶神偷窃格瓦拉']
    const heroes: Array<string> = ['法外狂徒张三', '电瓶神偷窃格瓦拉']
    ```

-   顶级类型 `any` **and** `unknown`
-   函数的类型 函数参数与返回值的类型注释

    ```typescript
    function greet(name: string): string {
        return name.toUpperCase()
    }
    ```

-   对象类型

    ```typescript
    function printCoord(pt: { x: number; y: number }) {
        console.log("The coordinate's x value is " + pt.x)
        console.log("The coordinate's y value is " + pt.y)
    }
    printCoord({ x: 3, y: 7 })
    ```

-   可选属性

    ```typescript
    function printName(obj: { first: string; last?: string }) {
        // ...
    }
    printName({ first: 'Bob' })
    printName({ first: 'Alice', last: 'Alisson' })
    ```

-   联合类型

    ```typescript
    function printId(id: number | string) {
        console.log('Your ID is: ' + id)
    }
    // OK
    printId(101)
    // OK
    printId('202')
    ```

## 接口 Interface & 类型别名 Type

>除了关键字不一样，其他剩下的效果基本上是一模一样的
>
>不同点
>
>1. type 是写死的,不可同名
>2. interface 可同名扩展

- type

    > 类型别名就是——任何类型的名称, 可以使用类型别名为任何类型提供名称，而不仅仅是对象类型

    ```typescript
    type Point = {
        x: number
        y: number
    }
    type ID = number | string
    let id: ID = 10086
    function printCoord(pt: Point) {
        console.log("The coordinate's x value is " + pt.x)
        console.log("The coordinate's y value is " + pt.y)
    }
    id = '123'
    printCoord({ x: 100, y: 100 })
    ```

- interface

    > 接口声明是命名对象类型的另一种方式

    ```typescript
    interface Point {
        x: number
        y: number
    }
    
    function printCoord(pt: Point) {
        console.log("The coordinate's x value is " + pt.x)
        console.log("The coordinate's y value is " + pt.y)
    }
    
    printCoord({ x: 100, y: 100 })
    ```
