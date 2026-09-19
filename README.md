# mincrade-edu-hacks
hacks for minecraft education tutorial: https://youtu.be/z0mhGEiWTFQ 


## Copy
```typescript
player.onChat("barrier", function () {
    player.execute(
    "give @s barrier 64"
    )
})
player.onChat("stopscaffold", function () {
    Scaffoldhack = 0
    player.say("Scaffold off.")
})
player.onChat("BOOM", function () {
    shapes.sphere(
    TNT,
    pos(10, 0, 0),
    3,
    ShapeOperation.Replace
    )
})
player.onChat("dia", function () {
    player.say("Gave you 10 diamonds.")
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND,
    10
    )
})
player.onChat("gmc", function () {
    gameplay.setGameMode(
    CREATIVE,
    mobs.target(LOCAL_PLAYER)
    )
})
player.onChat("jail", function (enchant) {
    shapes.sphere(
    BEDROCK,
    posCamera(0, 0, 6),
    3,
    ShapeOperation.Outline
    )
})
player.onChat("food", function () {
    player.say("Gave you 16 steak.")
})
player.onChat("sblock", function (enchant) {
    Blockid = enchant
})
player.onChat("day", function () {
    player.say("Set time to day.")
    gameplay.timeSet(gameplay.time(DAY))
    gameplay.setWeather(CLEAR)
})
player.onChat("GMC", function () {
    mobs.clearEffect(mobs.target(NEAREST_PLAYER))
})
player.onChat("give", function (item, Amount) {
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    blocks.blockById(item),
    Amount
    )
})
player.onChat("gms", function () {
    gameplay.setGameMode(
    SURVIVAL,
    mobs.target(LOCAL_PLAYER)
    )
})
player.onChat("help3", function () {
    player.say("xp amount - gives you xp")
    player.say("day - sets time to day")
})
player.onChat("OP", function () {
    mobs.enchant(
    mobs.target(LOCAL_PLAYER),
    "thorns",
    3
    )
    mobs.enchant(
    mobs.target(LOCAL_PLAYER),
    "protection",
    4
    )
})
player.onChat("help", function () {
    player.say("cx number - teleport on the x axis ")
    player.say("cy number - same as cx but on the y axis")
    player.say("cz number - same as cx but on the z axis")
    player.say("scaffold - places blocks under you")
    player.say("stopscaffold - stops scaffold")
    player.say("give itemid amount - gives you any item")
    player.say("link to id list: https://www.digminecraft.com/lists/item_id_list_edu.php")
    player.say("sblock blockid - changes scaffold block")
    player.say("dia - gives you 10 diamonds")
    player.say("type help2 for next page")
})
player.onChat("UNSTUCK", function () {
    shapes.line(
    AIR,
    pos(0, 0, 0),
    pos(0, 25, 0)
    )
    mobs.applyEffect(LEVITATION, mobs.target(NEAREST_PLAYER), 5, 3)
    mobs.applyEffect(NAUSEA, mobs.target(NEAREST_PLAYER), 5, 3)
})
player.onChat("help2", function () {
    player.say("food - gives you 16 cooked beef")
    player.say(".")
    player.say("cw - clear weather")
    player.say("portal - gives you 16 obsidian and 1 flint and steel")
    player.say("kit - gives you full diamond armor and tools")
    player.say("gmc - sets gamemode to creative")
    player.say("gms - sets gamemode to survival")
    player.say("bedrock - gives you a stack of bedrock")
    player.say("barrier - gives you a stack of barrier blocks")
    player.say("type help3 for next page")
})
player.onChat("OP2", function () {
    mobs.enchant(
    mobs.target(LOCAL_PLAYER),
    "sharpness",
    5
    )
})
player.onChat("WARDEN", function (WARDEN2) {
    for (let index = 0; index < WARDEN2; index++) {
        mobs.spawn(mobs.monster(WARDEN), posCamera(0, 0, 3))
    }
})
player.onChat("cy", function (item) {
    player.teleport(pos(0, item, 0))
})
player.onChat("scaffold", function () {
    if (Scaffoldhack == 1) {
        Scaffoldhack = 0
        player.say("Scaffold off")
    } else {
        Scaffoldhack = 1
        player.say("Scaffold on.")
    }
    while (Scaffoldhack == 1) {
        blocks.place(Blockid, pos(0, -1, 0))
    }
})
player.onChat("cw", function () {
    gameplay.setWeather(CLEAR)
})
// https://www.youtube.com/watch?v=IIJM3S9H5m0
player.onChat("kit", function () {
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND_SWORD,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND_PICKAXE,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND_AXE,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND_CHESTPLATE,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND_HELMET,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND_BOOTS,
    1
    )
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    DIAMOND_LEGGINGS,
    1
    )
})
player.onChat("cx", function (item) {
    player.teleport(pos(item, 0, 0))
})
player.onChat("xp", function (num1) {
    gameplay.xp(num1, mobs.target(LOCAL_PLAYER))
    player.say("gave you " + num1 + " xp")
})
player.onChat("bedrock", function () {
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    BEDROCK,
    64
    )
})
player.onChat("cz", function (item) {
    player.teleport(pos(0, 0, item))
})
player.onChat("portal", function () {
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    OBSIDIAN,
    16
    )
    loops.pause(50)
    mobs.give(
    mobs.target(LOCAL_PLAYER),
    FLINT_AND_STEEL,
    1
    )
})
player.onChat("gm", function () {
    mobs.applyEffect(RESISTANCE, mobs.target(NEAREST_PLAYER), 600, 33)
    mobs.applyEffect(SPEED, mobs.target(NEAREST_PLAYER), 600, 33)
    mobs.applyEffect(STRENGTH, mobs.target(NEAREST_PLAYER), 600, 33)
    mobs.applyEffect(HEALTH_BOOST, mobs.target(NEAREST_PLAYER), 600, 33)
    mobs.applyEffect(WATER_BREATHING, mobs.target(NEAREST_PLAYER), 600, 33)
    mobs.applyEffect(JUMP_BOOST, mobs.target(NEAREST_PLAYER), 600, 1)
    mobs.applyEffect(ABSORPTION, mobs.target(NEAREST_PLAYER), 600, 33)
    mobs.applyEffect(HASTE, mobs.target(NEAREST_PLAYER), 600, 33)
    mobs.applyEffect(NIGHT_VISION, mobs.target(NEAREST_PLAYER), 600, 33)
})
let Scaffoldhack = 0
let Blockid = 0
let item = DIRT
Blockid = 3
Scaffoldhack = 0
player.say("Commands, jail, op(2), GM(c)[GODMODE] ,boom,WARDEN, UNSTUCK TYPE HELP FOR MORE")
```

