### @flyoutOnly 1


# じどう マイナー レベル2


## Step 1 @unplugged
![Side task](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_3.jpg)
この タスクでは、エージェントを つかって **てっこうせき だけ** を ほりだそう！
まわりの いしを ほると、こうざんが くずれるかも しれないから きを つけてね...

じゅんびが できたら「つぎへ」を おしてね。

```template
//
```

## Step 2

まず てっこうせきを みつけよう。エージェントの したの ブロックを チェックするところから はじめるよ。
``||logic:if then||`` を おいて、そのなかに ``||logic:0 = 0||`` ブロックを いれよう。
ひだりがわに ``||agent: agent inspect block down||`` を つかって したの ブロックを しらべよう。
みぎがわで てっこうせき ブロックと くらべよう。
if の なかに ``||agent:agent destroy down||`` を いれよう。
コードを ためしてみてね。でんわを つかえば いつでも タスクを リセットできるよ。

```blocks
if (agent.inspect(AgentInspection.Block, DOWN) == IRON_ORE) {
            agent.destroy(DOWN)
        }
```

## Step 3

まえの ステップで つくった コードを つかって、かべの のこりも チェックして こわせるかな？
この コードを ``||loops:repeat 3 times||`` の なかに いれて、まいかい エージェントを 1つ うえに うごかそう。
エージェントを さいごに したに もどすのも わすれずにね。
コードを ためしてみてね。でんわを つかえば いつでも タスクを リセットできるよ。

```blocks
    if (agent.inspect(AgentInspection.Block, DOWN) == IRON_ORE) {
        agent.destroy(DOWN)
    }
    for (let index = 0; index < 3; index++) {
        if (agent.inspect(AgentInspection.Block, LEFT) == IRON_ORE) {
            agent.destroy(LEFT)
        }
        agent.move(UP, 1)
    }
    agent.move(DOWN, 2)

```

## Step 4

さいごに、ぜんたいの コードを もうひとつの ``||loops:repeat X times||`` の なかに いれよう。エージェントが まえに すすむ かいすうを かぞえてね。
ここからは じぶんで がんばってね！

（でんわの「エージェントを リセット」ボタンで いつでも エージェントを もどして やりなおせるよ）


```ghost
    for (let index = 0; index < 8; index++) {
        if (agent.inspect(AgentInspection.Block, DOWN) == IRON_ORE) {
            agent.destroy(DOWN)
        }
        for (let index = 0; index < 3; index++) {
            if (agent.inspect(AgentInspection.Block, LEFT) == IRON_ORE) {
                agent.destroy(LEFT)
            }
            agent.move(UP, 1)
        }
        agent.move(DOWN, 2)
        agent.move(FORWARD, 1)
    }

```

```package
seymour=github:kt199671/Minecraft-EE-MakeCode
```
