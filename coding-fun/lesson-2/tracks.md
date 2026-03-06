### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# エージェントを プログラムして カメの あしあとを たどろう！

## Step 1
``||agent: agent move forward||`` ブロックを つかって、エージェントを カメの あしあとに そって ゲートまで うごかそう。できたら **さいせい** ボタンを おして コードを じっこうしてね。マインクラフトの なかで コードを うごかすのを わすれないでね。

```ghost
player.onChat("tracks", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {

 }
```
