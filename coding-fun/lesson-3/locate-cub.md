### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# こぐまを みつけよう！

## Step 1
``||loops:while||`` と ``||agent:agent detect||`` コマンドを つかって、エージェントに みちを ほらせよう。どこまで つづくか わからない みちでも だいじょうぶ！エージェントは ``||agent:destroy forward & up||`` で ゆきを こわして とおれるように するよ。できたら **さいせい** ボタンを おして コードを じっこうしてね。マインクラフトの なかで コードを うごかすのを わすれないでね。

#### ~ tutorialhint
コードの ブロックを くっつける かたちを よく みてね。``||agent:agent move forward||`` を つかおう。

```template
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {

    }
})
```

```ghost
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

```
