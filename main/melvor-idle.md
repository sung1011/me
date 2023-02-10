# melvor idle

## console

```js
- coin

    game.gp.add(999999999999) // 金币
    game.slayerCoins.add(999999999999) // 屠杀币：
    game.combat.player.addPrayerPoints(999999999999) // 祈祷点：
    game.raidCoins.add(999999999999) // 哥布林币：
    game.township.availableGameTicksToSpend+=999999999999 // 城镇tick

    game.petManager.unlockPetByID("宠物ID")
    game.summoning.discoverMark(game.summoning.actions.allObjects[召唤编号]) // 召唤印记

符文 runecrafting

    game.bank.addItemByID("melvorD:Rune_Essence", 999999999999, true,true,true) // 符文精华
    game.bank.addItemByID("melvorD:Air_Rune", 99999999, true, true, true) // 大气符文
    game.bank.addItemByID("melvorD:Mind_Rune", 99999999, true, true, true) // 心智符文
    game.bank.addItemByID("melvorD:Water_Rune", 99999999, true, true, true)  // 流水
    game.bank.addItemByID("melvorD:Earth_Rune", 99999999, true, true, true) // 大地
    game.bank.addItemByID("melvorD:Fire_Rune", 99999999, true, true, true) // 火焰
    game.bank.addItemByID("melvorD:Light_Rune", 99999999, true, true, true) // 光明
    game.bank.addItemByID("melvorD:Body_Rune", 99999999, true, true, true) // 躯体
    game.bank.addItemByID("melvorD:Chaos_Rune", 99999999, true, true, true) // 混沌
    game.bank.addItemByID("melvorF:Nature_Rune", 99999999, true, true, true) // 自然
    game.bank.addItemByID("melvorF:Havoc_Rune", 99999999, true, true, true) // 灾祸
    game.bank.addItemByID("melvorD:Death_Rune", 99999999, true, true, true) // 死亡
    game.bank.addItemByID("melvorD:Blood_Rune", 99999999, true, true, true) // 鲜血
    game.bank.addItemByID("melvorF:Spirit_Rune", 99999999, true, true, true) // 灵魂
    game.bank.addItemByID("melvorD:Ancient_Rune", 99999999, true, true, true) // 古代
    game.bank.addItemByID("melvorD:Mist_Rune", 99999999, true, true, true) // （组合符文）迷雾
    game.bank.addItemByID("melvorD:Dust_Rune", 99999999, true, true, true) // （组合符文）沙尘
    game.bank.addItemByID("melvorF:Mud_Rune", 99999999, true, true, true) // （组合符文）泥土
    game.bank.addItemByID("melvorD:Smoke_Rune", 99999999, true, true, true) // （组合符文）烟雾
    game.bank.addItemByID("melvorF:Steam_Rune", 99999999, true, true, true) // （组合符文）蒸汽
    game.bank.addItemByID("melvorF:Lava_Rune", 99999999, true, true, true) // （组合符文）岩浆
    game.bank.addItemByID("melvorTotH:Poison_Rune", 99999999, true, true, true) // 剧毒符文
    game.bank.addItemByID("melvorTotH:Decay_Rune", 99999999, true, true, true) // 衰退
    game.bank.addItemByID("melvorTotH:Infernal_Rune", 99999999, true, true, true) // 炼狱
    game.bank.addItemByID("melvorTotH:Despair_Rune", 99999999, true, true, true) // 无望
    game.bank.addItemByID("melvorTotH:Soul_Rune", 99999999, true, true, true) // 灵魂
    game.bank.addItemByID("melvorTotH:Lightning_Rune", 99999999, true, true, true) // 雷霆
    game.bank.addItemByID("melvorTotH:Archaic_Rune", 99999999, true, true, true) // 远古
    game.bank.addItemByID("melvorTotH:Calamity_Rune", 99999999, true, true, true) // 灾厄

占星 astrology

    game.bank.addItemByID("melvorF:Stardust", 999999999999, true,true,true) // 星尘
    game.bank.addItemByID("melvorF:Golden_Stardust", 999999999999, true,true,true) // 金色星辰
    game.bank.addItemByID("melvorTotH:Travellers_Compass", 999999999999, true,true,true) // 旅行指南针

种子 seed

    game.bank.addItemByID("melvorD:Potato_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Onion_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Cabbage_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Tomato_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Sweetcorn_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Strawberry_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Cherry_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Watermelon_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Snape_Grass_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Carrot_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Pumpkin_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Chilli_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Starfruit_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Snowcress_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Garum_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Sourweed_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Mantalyme_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Lemontyle_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Oxilyme_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorF:Poraxx_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorF:Pigtayle_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorF:Barrentoe_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Bitterlyme_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Moonwort_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Wurmtayle_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Oak_Tree_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Willow_Tree_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Maple_Tree_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Yew_Tree_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorF:Apple_Tree_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Magic_Tree_Seed", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Banana_Tree_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Grove_Tree_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Elderwood_Tree_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Carrion_Tree_Seeds", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Mushroom_Spores", 9999999999, true, true, true)

药草 herb

    game.bank.addItemByID("melvorD:Garum_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Sourweed_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Mantalyme_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Lemontyle_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Oxilyme_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorF:Poraxx_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorF:Pigtayle_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorF:Barrentoe_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Bitterlyme_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Moonwort_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorTotH:Wurmtayle_Herb", 9999999999, true, true, true)
    game.bank.addItemByID("melvorD:Cherry_Seeds", 9999999999, true, true, true)

采矿 mining

    game.bank.addItemByID("melvorD:Coal_Ore", 9999999999, true, true, true)

其他

    game.bank.addItemByID("melvorD:Bones", 9999999999, true, true, true) // 骨头
    game.bank.addItemByID("melvorD:Big_Bones", 9999999999, true, true, true) // 巨骨
    game.bank.addItemByID("melvorF:Holy_Dust", 9999999999, true, true, true) // 灰烬
    game.bank.addItemByID("melvorD:Dragon_Bones", 9999999999, true, true, true) // 魔法骨
    game.bank.addItemByID("melvorD:Dragon_Bones", 9999999999, true, true, true) // 龙骨
    game.bank.addItemByID("melvorF:Goo", 9999999999, true, true, true) // 粘液
    game.bank.addItemByID("melvorF:Wildflower", 9999999999, true, true, true) // 野花
    game.bank.addItemByID("melvorF:Eyeball", 9999999999, true, true, true) // 眼球
    game.bank.addItemByID("melvorF:Large_Horn", 9999999999, true, true, true) // 巨角
    game.bank.addItemByID("melvorD:Amulet_of_Looting", 9999999999, true, true, true) // 财宝护符
    game.bank.addItemByID("melvorD:Mysterious_Stone", 9999999999, true, true, true) // 神秘石
    game.bank.addItemByID("melvorF:Whetstone", 9999999999, true, true, true) // 磨刀石
    game.bank.addItemByID("melvorF:Wizards_Scroll", 9999999999, true, true, true) // 巫师卷轴
    game.bank.addItemByID("melvorF:Prayer_Scroll", 9999999999, true, true, true) // 祝祭卷轴
    game.bank.addItemByID("melvorF:Fishing_Hook", 9999999999, true, true, true) // 鱼钩
    game.bank.addItemByID("melvorF:Basic_Bag", 9999999999, true, true, true) // 普通包裹
    game.bank.addItemByID("melvorF:Runecrafting_Pouch", 9999999999, true, true, true) // 符文袋
    game.bank.addItemByID("melvorF:Seed_Pouch", 9999999999, true, true, true) // 种子袋
    game.bank.addItemByID("melvorF:Thiefs_Moneysack", 9999999999, true, true, true) // 盗贼袋
    game.bank.addItemByID("melvorF:Alchemists_Bag", 9999999999, true, true, true) // 炼金袋
    game.bank.addItemByID("melvorF:Bank_Slot_Token", 9999999999, true, true, true) // 仓库币
    game.bank.addItemByID("melvorTotH:Golden_Reel", 9999999999, true, true, true) // 金色卷轴
    game.bank.addItemByID("melvorTotH:Burning_Reel", 9999999999, true, true, true) // 燃烧卷轴
    game.bank.addItemByID("melvorTotH:Deadly_Toxins_Potion", 9999999999, true, true, true) // 致命毒素
    game.bank.addItemByID("melvorTotH:Golden_Key", 9999999999, true, true, true) // 金色钥匙
    game.bank.addItemByID("melvorTotH:Exotic_Herb_Sack", 9999999999, true, true, true) // 奇异药草袋
    game.bank.addItemByID("melvorTotH:Artisan_Pouch", 9999999999, true, true, true) // 弓匠袋
    game.bank.addItemByID("melvorTotH:Kindling_Pouch", 9999999999, true, true, true) // 火种袋
    game.bank.addItemByID("melvorTotH:Stamina_Pouch", 9999999999, true, true, true) // 耐力袋
    game.bank.addItemByID("melvorTotH:Spirit_Bag", 9999999999, true, true, true) // 灵魂包裹
    game.bank.addItemByID("melvorTotH:Chefs_Bag", 9999999999, true, true, true) // 大厨包裹
    game.bank.addItemByID("melvorTotH:Summoners_Bag", 9999999999, true, true, true) // 召唤师包裹
    game.bank.addItemByID("melvorTotH:Ectoplasm", 9999999999, true, true, true) // 虚无质
```

## wiki

- <https://wiki.melvoridle.com/w/Main_Page>