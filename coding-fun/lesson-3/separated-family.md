### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# はなればなれの かぞく！

## Step 1
エージェントに こおりの われめに はしを かけさせよう。エージェントの もちものに **オークのいた** を **64こ** いれてね。

#### ~ tutorialhint
``||loops:while||`` ループに **not** を つかうのを わすれないでね。エージェントに どこに ブロックを おかせたいか かんがえてみよう。


```ghost
player.onChat("family", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
})

```
