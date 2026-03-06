### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# エージェントを プログラムして じゃまな ものを こわそう！

## Step 1
エージェントを つかって、じゃまな **きのみき** を こわそう。``||agent: agent destroy||`` と ``||agent:agent collect all||`` ブロックを つかってね。``||loops:repeat||`` ブロックを つかうと コードが みじかくなるよ。できたら **さいせい** ボタンを おして コードを じっこうしてね。マインクラフトの なかで コードを うごかすのを わすれないでね。


```ghost
player.onChat("path", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```
