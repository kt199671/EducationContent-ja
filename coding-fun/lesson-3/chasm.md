### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# おおきな われめを わたろう！

## Step 1
エージェントに **はしを つくらせて** こおりの われめを わたろう。``||agent:set block or item||`` を つかって エージェントの もちものに ざいりょうを いれてね。ざいりょうは **オークのいた** を えらんで、**64こ** いれよう。``||loops:while||`` エージェントが したに ブロックを かんち **しない** あいだ、オークのいたを **した** に おいて **まえ** に すすんで はしを つくろう。


```template
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 1, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, DOWN))) {

    }
})
```

```ghost
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})

```

