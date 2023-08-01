# 掉落组

## 配置用法

### 下面是一个ExampleDrop 即 示例掉落组 [pei-zhi.md](../../kai-shi/pei-zhi.md "mention")

{% code title="ExampleDrop.yml" lineNumbers="true" %}
```yaml
Options:
  #掉落组Key
  Key: Example
  #配置掉落组
  Drop:
    Pack:
      #[Type: per, order, range, ap, ALL, NULL]
      Type: per
      Info: 50%
      Protected: 1,2,3,4,5,6,7,8
    Exp:
      #[Type: per, order, range]
      Type: per
      Info: 50%
  Item:
    #[lore,nbt]
    Enable: true
    Type: lore
    Info: "本物品死亡不掉落"
```
{% endcode %}

### Options.Key[^1]

就是你刚刚设置的Drop下的Bind绑定的Key

### Options.Drop.Pack.Type[^2]

点开，自己看

* per 百分比掉落 去掉保护格 Info: 50%
* order 指定掉落数量 去掉保护格 Info: 144514
* range 范围掉落 去掉保护格 Info: 1\~3
* ap 指定格掉落 去掉保护格 Info: 1,2,3,4
* ALL 全部掉落 去掉保护格 Info: ALL
* NULL 全不掉落 Info: NULL

### Options.Drop.Pack.Protected[^3]

类似上面的 Type：ap， 也是1,2,3,4这种

### Options.Drop.Exp.Type[^4]

和上面类似，不过少了指定格，毕竟你经验怎么指定格？？？

### Options.Drop.Exp.Info[^5]

一样的

### Options.Item.Enable[^6]

一样，是否启用，启用的话满足条件的就不会掉落 （你运气好说不定刚好啥也不掉，懂我意思吗

### Options.Item.Type[^7]

用nbt判断还是lore

### Options.Item.Info[^8]

判断的字符串

***

{% hint style="success" %}
有在认真看？下一个赎回组
{% endhint %}

[^1]: Type: String

[^2]: Type: #\[Type: per, order, range, ap, ALL, NULL]

[^3]: Type: String

[^4]: Type: #\[Type: per, order, range, ALL, NULL]

[^5]: Type：String

[^6]: Type: Boolean

[^7]: Type: \[lore,nbt]

[^8]: Type: String
