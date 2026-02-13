### @flyoutOnly 1


# じどう マイナー レベル1


## Step 1 @unplugged

![Side task](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_2.jpg)
このさきの こうざんは きけんで、こうふが はいれません。エージェントなら できるかな？
エージェントを つかって こうどうを ほりましょう。まず、エージェントの まえの ブロックを ``||agent:agent destroy forward||`` で こわしてみよう。
コードを ``||player: on start||`` の なかに おいて、みぎしたの **さいせい** ボタンを クリックしてね。

```template
//
```

```blocks
agent.destroy(FORWARD)
```

## Step 2
つぎは ``||agent:agent move up||`` コマンドと もうひとつの ``||agent:agent destroy forward||`` を くみあわせよう。
エージェントに いしブロック **3つ** の さいしょの れつを こわせるかな？

```blocks
agent.destroy(FORWARD)
agent.move(UP, 1)
agent.destroy(FORWARD)
agent.move(UP, 1)
agent.destroy(FORWARD)
agent.move(UP, 1)
```


## Step 3
おなじ ことを 3かい くりかえすのに、もっと いい ほうほうが あるはず...
こたえは、ループ！
``||loops:Repeat 3 times do||`` コマンドを つかうと、なかの コマンドを 3かい くりかえせるよ。
``||agent:agent destroy forward||`` と ``||agent:agent move up||`` を ``||loops:Repeat 3 times do||`` の なかに いれてみよう。

```blocks
for (let index = 0; index < 3; index++) {
    agent.destroy(FORWARD)
    agent.move(UP, 1)
}

```


## Step 4
さいごに、ここまで ならった ことを つかって、``||loops:Repeat 7 times do||`` で こうどうの おくの ゴールドブロック まで ぜんぶ ほれるかな？


```ghost
    for (let index = 0; index < 7; index++) {
        for (let index = 0; index < 3; index++) {
            agent.destroy(FORWARD)
            agent.move(UP, 1)
        }
        agent.move(DOWN, 3)
        agent.move(FORWARD, 1)
    }
```

```package
seymour=github:kt199671/Minecraft-EE-MakeCode
```
