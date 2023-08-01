# 配置

若插件成功安装，你将会在服务端插件目录下看到一个名为 ColdEstiny 的目录，其结构如下

```
ColdEstiny
│  setting.yml ················ 插件配置文件
│  kether.yml ················ Kether 配置文件
│  
├─data ······················· 玩家掉落物品数据
│      
│      
├─lang ······················· 语言文件
│      zh_CN.yml
│      
└─workspace ·················· 工作空间
    │  ExampleConfig.yml ····· 配置组示例
    ├─drop ··················· 掉落组
    │  ExampleDrop.yml ······· 掉落组示例
    ├─redeem ················· 赎回组
    │  ExampleRedeem.yml ······· 赎回组示例
```

## 配置文件

{% code title="setting.yml" lineNumbers="true" fullWidth="false" %}
```yaml
#ColdeEstiny Setting
Options:
  #插件Debug模式开关
  Debug: true
RedeemUI:
  
```
{% endcode %}

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
      Didnt: 0
      Info: 50%
  Item:
    #[lore,nbt]
    Enable: true
    Type: lore
    Info: "本物品死亡不掉落"
```
{% endcode %}

{% code title="ExampleRedeem.yml" lineNumbers="true" %}
```yaml
Options:
  #赎回组Kay
  Key: Example
  #权限配置
  Perm:
    #是否启用
    Enable: true
    #权限
    Info: "ce.redeem.example"
  #时间限制
  RedeemTime:
    #是否启用
    Enable: true
    #时间
    Time: 1day
```
{% endcode %}
