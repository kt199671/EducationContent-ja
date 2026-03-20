### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false
### @explicitHints 1


# たかい ところに のぼろう！

## Step 1
エージェントに **オークのいた** で **10だん** の タワーを つくらせよう。まず ``||agent:set block or item||`` コマンドで エージェントの もちものに **オークのいた** を **64こ** いれてね。``||agent:agent place||`` ブロックを つかって オークのいたを **まえ**、**ひだり**、**みぎ** に おこう。ブロックを おいたら エージェントは **うえに うごく** よ。

#### ~ tutorialhint
``||loops:repeat||`` ブロックを つかって かずを **10** に してみよう。

## Step 2
エージェントを タワーから **おりさせて**、**10だん** の **はしご** を つくらせよう。のぼれるように はしごが ひつようだよ！

#### ~ tutorialhint
``||agent: agent set block||`` で エージェントの もちものに **はしご** を **64こ** いれるのを わすれないでね。


```ghost
player.onChat("tower", function () {
    agent.move(FORWARD, 1)
    agent.setItem(LADDER, 64, 1)
    for (let index = 0; index < 10; index++) {
        agent.place(FORWARD)
        agent.move(UP, 1)
    }
    agent.move(DOWN, 10)
})

```


