# 攻击技能
攻击技能定义在[CommonSpellData]中。将攻击技能配置在单位的[AttackSkill]中，单位就可以使用它进行攻击。

#### active_cd
激活冷却

* 参数
    * max_cd (number) - 冷却上限(秒)

```lua
    attack:active_cd(max_cd)
```

#### get_cd
获取冷却

* 返回
    * cd (number) - 冷却(秒)

```lua
    local cd = attack:get_cd()
```

#### get_name
获取攻击名

* 返回
    * name (string) - 攻击名

```lua
    local name = attack:get_name()
```

#### is_common_attack
是否是攻击技能

* 返回
    * result (boolean) - 结果

总是返回 `true` 。区别于[skill:is_common_attack]。

```lua
    local result = attack:is_common_attack()
```

#### is_skill
是否是技能对象

* 返回
    * result (boolean) - 结果

总是返回 `false` 。区别于[skill:is_skill]。

```lua
    local result = attack:is_skill()
```

#### set_cd
设置冷却

* 参数
    * cd (number) - 冷却(秒)

对不在冷却的攻击技能无效。冷却的有效范围是[0, 当前冷却上限]

```lua
    attack:set_cd(cd)
```

#### stop
打断攻击

```lua
    attack:stop()
```

[skill:is_skill]: /ac/API/skill?id=is_skill
[skill:is_common_attack]: /ac/API/skill?id=is_common_attack
[CommonSpellData]: 404
[AttackSkill]: 404