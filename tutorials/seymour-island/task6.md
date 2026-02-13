### @flyoutOnly 1


# マルチプレイヤー かいろ

## Step 1 @unplugged
![Side task](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_6.jpg)
はじめるまえに、この タスクは 2にん ひつようだから、となりに ともだちが いることを たしかめてね！
また、この タスクの まえに かいろしゅうりの 1にんよう タスクを クリアしておくのが おすすめだよ。
じゅんびが できたら「つぎへ」を おしてね。

```template
//
```

## Step 2

この タスクでは、2にんで おおきな かいろを しゅうり するよ。
したの かいろ エリアを みてみよう。4つの くかくが あって、2つは きみが なおして、2つは ともだちが なおすよ。おたがいの かいろは まんなかの むらさきの ブロックで つながっているよ。
レッドストーンは **みどりの エメラルドブロック** の うえにだけ おけるよ。


## Step 3

1つ1つの ブロックに めいれいを かく こともできるけど、エメラルドブロックを ぜんぶ さがして レッドストーンを おく プログラムを つくったほうが いいよね。
まず ``||agent:agent move left/right||`` で エージェントを すみに うごかそう。

```blocks
agent.move(LEFT, 1)
```

## Step 4

つぎに、したの ブロックが エメラルドかどうか チェックしよう。
``||logic:if then||`` を おいて、そのなかに ``||logic:0 = 0||`` ブロックを いれよう。
ひだりがわに ``||agent: agent inspect block down||`` を つかって したの ブロックを しらべよう。
みぎがわで エメラルドブロックと くらべよう。

```blocks
    agent.move(LEFT, 1)
    if (agent.inspect(AgentInspection.Block, DOWN) == EMERALD_BLOCK) {

    }
```

## Step 5

if の なかで、エメラルドが みつかったら ``||agent:agent place down||`` で レッドストーンを おこう。
if の あとに ``||agent:agent move forward by 1||`` で 1つ まえに すすもう。

```blocks
    agent.move(LEFT, 1)
    if (agent.inspect(AgentInspection.Block, DOWN) == EMERALD_BLOCK) {
        agent.place(DOWN)
    }
    agent.move(FORWARD, 1)
```

## Step 6

これで きほんの パーツは そろったよ。コードの りょうを へらすために ``||loops:repeat X times||`` も つかってみてね。そうすると ずっと かんたんに なるよ。
がんばって！


```ghost
    agent.move(LEFT, 1)
    for (let index = 0; index < 9; index++) {
        for (let index = 0; index < 5; index++) {
            if (agent.inspect(AgentInspection.Block, DOWN) == EMERALD_BLOCK) {
                agent.place(DOWN)
            }
            agent.move(FORWARD, 1)
        }
        agent.move(BACK, 5)
        agent.move(RIGHT, 1)
    }
```



```package
seymour=github:kt199671/Minecraft-EE-MakeCode
```
