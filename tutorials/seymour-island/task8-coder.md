### @flyoutOnly 1


# めいろ コーダー


## Step 1 @unplugged
![Overhead task](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_8.jpg)
この タスクでは、エージェントを きんの プレッシャープレートまで たどりつかせよう。かんたんそう でしょ？...
でも、じゃまな ブロックが みえないんだ！ それを みるには、うえの ポジションに いる ともだちの ちからが ひつよう。ともだちに あんないして もらおう。
2にんとも じゅんびが できたら「つぎへ」を おしてね。

```template
//
```

## Step 2
エージェントを うごかすには ``||agent:agent move FORWARD||`` コマンドを つかおう。
``||agent:agent turn LEFT||`` コマンドも つかえるよ。

コードを ``||player: on start||`` の なかに おいて、みぎしたの さいせい ボタンで じっこうしてね。

がんばって！

```blocks
agent.move(FORWARD, 1)
```

```ghost
    agent.move(LEFT, 4)
    agent.move(FORWARD, 2)
    agent.move(RIGHT, 2)
    agent.move(LEFT, 2)
    agent.move(BACK, 2)
    agent.move(RIGHT, 8)
    agent.move(FORWARD, 6)
    agent.move(LEFT, 2)
    agent.move(RIGHT, 2)
    agent.move(BACK, 6)
    agent.move(LEFT, 4)
    agent.move(FORWARD, 5)
    agent.move(LEFT, 1)
    agent.move(FORWARD, 1)
    agent.move(BACK, 1)
    agent.move(RIGHT, 1)
    agent.move(BACK, 5)
    agent.move(LEFT, 4)
    agent.move(FORWARD, 3)
    agent.move(RIGHT, 1)
    agent.move(FORWARD, 7)
    agent.move(RIGHT, 4)
    agent.move(BACK, 1)
    agent.move(RIGHT, 3)
    agent.move(FORWARD, 3)
    agent.move(LEFT, 4)
    agent.turn(LEFT)

```

```package
seymour=github:kt199671/Minecraft-EE-MakeCode
```
