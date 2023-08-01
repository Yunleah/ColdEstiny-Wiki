# 配置组

## 配置用法

### 下面是一个ExampleConfig 即 示例配置组 [pei-zhi.md](../../kai-shi/pei-zhi.md "mention")

{% code title="ExampleConfig.yml" lineNumbers="true" %}
```yaml
Options:
  #是否启用该配置组
  Enable: true
  #配置限定世界
  World:
    #是否启用
    Enable: true
    #世界名
    Info: "world"
  #配置限定权限
  Perm:
    #是否启用
    Enable: true
    #权限
    Info: "ce.perm.example"
  #配置掉落组
  Drop:
    #是否启用
    Enable: true
    #绑定掉落组
    Bind: Example
  #配置脚本动作
  Action:
    #在玩家死亡时运行
    Pre:
      #是否启用
      Enable: true
      #脚本
      Script: |-
        tell 'Pre Kether 运行成功'
    #在玩家重生时运行
    Post:
      #是否启用
      Enable: true
      #脚本
      Script: |-
        tell 'Post Kether 运行成功'
  #配置玩家重生
  PlayerSpawn:
    #配置自动重生
    AutoRespawn:
      #是否启用
      Enable: true
      #延迟时间[单位s]
      Time: 1s
    #配置重生点
    Spawn:
      #重生地点类型[death:死亡点,coo：坐标, loc: 重生点]
      Type: death
      Info: 100 100 100 world
  #配置物品赎回
  ItemRedemption:
    #是否启用
    Enable: true
    #绑定赎回组
    Bind: Example
```
{% endcode %}

觉得很复杂？下面我来告诉你每一个的含义与作用.

{% hint style="warning" %}
在开始之前，你应该知道类似`Options.Enable`是什么意思吧？

鼠标放在本行上并点击[^1]
{% endhint %}

### Options.Enable[^2]&#x20;

传入**布尔值**，填 **true** 即此配置组**启用** 反之填 **false** 则此配置**禁用**

### [Options.World.Enable ](#user-content-fn-3)[^3]

同**Options.Enable**，填 **true** 即启用限定世界，反之禁用

### Options.World.Info[^4]

传入字符串，即限定的世界名

{% hint style="success" %}
使用/ce world 即可获得成功被插件读取到的世界名列表&#x20;
{% endhint %}

### Options.Perm.Enable[^5]

讲两遍了，不讲了\~ 填 true 则限定玩家权限，反之禁用

### Options.Perm.Info[^6]

同上面世界判断的Info，不过这个是权限

### Options.Drop.Enable[^7]

同上面的Enable，填true则启用随机掉落

### Options.Drop.Bind[^8]

绑定的掉落组，填的是掉落组的Key值

### Options.Action.Pre.Enable[^9]

同上，若启用则在玩家重生前会先运行Kether脚本，若返回值为false则会停止插件处理

### Options.Action.Pre.Script[^10]

Kether脚本

### Options.Action.Post.Enable[^11]

同上，若启用则在玩家重生后会运行Kether脚本

### Options.Action.Post.Script[^12]

Kether脚本

### Options.PlayerSpawn.AutoRespawn.Enable[^13]

同上，若启用则玩家死亡后自动重生

### Options.PlayerSpawn.AutoRespawn.Time[^14]

重生延迟时间

### Options.PlayerSpawn.Spawn.Type[^15]

你可以点开↑查看Type，可以得知这里有三种类型，如下

* death 玩家死亡地点&#x20;
* coo 下面手动设置的重生点坐标
* loc 玩家重生点

### Options.PlayerSpawn.Spawn.Info[^16]

如果你选择的Type是coo则本配置被实施 Info: \<X坐标> \<Y坐标> \<Z坐标> <世界名>

### Options.ItemRedemption.Enable[^17]

同上，true则启用物品赎回，玩家死亡点不会生成物品，反之不开启赎回则会在死亡点生成物品

### Options.ItemRedemption.Bind[^18]

绑定的赎回组Key

{% hint style="success" %}
看的明白吧？？接下来就是掉落组咯
{% endhint %}

[^1]: 看到这行字了吗？下面也是一样

[^2]: Type: Boolean

[^3]: Type: Boolean

[^4]: Type: String

[^5]: Type: Boolean

[^6]: Type: String

[^7]: Type：Boolean

[^8]: Type: String

[^9]: Type: Boolean

[^10]: Type: String

[^11]: Type: Boolean

[^12]: Type: String

[^13]: Type: Boolean

[^14]: Type: String

[^15]: Type: \[death,loc,coo]

[^16]: Type: String

[^17]: Type: Boolean

[^18]: Type: String
