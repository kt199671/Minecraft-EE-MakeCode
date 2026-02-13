### @flyoutOnly 1


# かいろの しゅうり


## Step 1 @unplugged

![Overhead task](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_1_overhead.jpg)
この タスクでは、レッドストーン かいろを なおします。こわれた ところは したの みどりの ブロックで しるしが ついています。
エージェントには しゅうりよう の レッドストーンが たくさん あります。
コードを ``||loops: on start||`` の なかに おいて、じっこうするには みぎしたの **さいせい** ボタンを クリックしてね。
**つぎへ** ボタンで すすもう。

## Step 2
まず、エージェントを こわれた ところ（みどりの しるし）まで うごかそう。
``||agent:agent move forward||`` と ``||agent:agent turn left/right||`` コマンドを つかって、エージェントを みどりの ブロックの うえに いどうさせよう。

```template
//
```

```block
agent.move(FORWARD, 1)
agent.turn(LEFT_TURN)
agent.move(FORWARD, 2)

```


## Step 3
``||agent:agent place down||`` を つかって みどりの ブロックの うえに レッドストーンを おいて、かいろの その ぶぶんを なおそう。
```blocks
agent.place(DOWN)
```


## Step 4
やりかたが わかったね。のこりの 2つの みどりの ブロックにも レッドストーンを おく コードを かこう。
こまったら、でんわの「タスクを リセット」を つかって やりなおせるよ。

```ghost
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
    agent.place(DOWN)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
    agent.place(DOWN)
    agent.turn(RIGHT_TURN)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
    agent.place(DOWN)
```

```package
seymour=github:kt199671/Minecraft-EE-MakeCode
```
