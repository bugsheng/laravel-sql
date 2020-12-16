## laravel-sql

> 因为目前laravel框架中没有自带的完整输出sql语句的封装方法，查阅资料后决定封装成扩展，嫁接到系统项目中

### 用法

```php
// 示例查询语句
User::where('name', 'like', '%test%')->get();
// 完整sql获取 
User::where('name', 'like', '%test%')->select(['*'])->sql();

// 示例查询语句
DB::table('users')->where('name', 'like', '%test%')->get();
// 完整sql获取
DB::table('users')->where('name', 'like', '%test%')->select(['*'])->sql();
```

- 上述示例中直接的**get()**方法获取数据 实际上缺省了参数**['*']**

## 框架要求

Laravel >= 5.5

