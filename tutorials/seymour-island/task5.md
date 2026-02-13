### @flyoutOnly 1


# さかな あつめ


## Step 1

```template
//
```

この タスクでは、クマノミと フグを ふねから さんばしに うつします。まず、さかなを あつめに いこう！``||agent:agent move forward 2||`` コマンドで エージェントを さかなの しゅうしゅう ポイントまで うごかそう。
そして ``||agent:agent collect CLOWNFISH||`` コマンドで クマノミだけ あつめよう。
コードを ``||on start||`` の なかに おいて、さいせい ボタンで じっこうしてね。

```blocks
agent.move(FORWARD, 2)
agent.collect(CLOWNFISH)

```

## Step 2
クマノミを あつめたら、のこりの しゅうしゅう ポイントからも クマノミを あつめよう。コードを ``||loops:Repeat 3 times loop||``（Python なら ``||loops:for loop||``）に いれてみよう。

```blocks
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 2)
    agent.collect(CLOWNFISH)
}

```

## Step 3
クマノミが ぜんぶ あつまったら、エージェントを さんばしの ただしい おきば まで うごかして、``||agent:agent drop items one at a time||`` コマンドで さかなを バケツに いれよう。

```ghost
agent.dropAllItemsIndividually(FORWARD)

```

## クマノミ ずけい @unplugged
![Clownfish Diagram](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/master/tutorials/seymour-island/images/task_5_map_clownfish.jpg)
うえの ずを つかって、エージェントが さかなを おとどけするまでの きょりを はかろう！

## Step 4
ぜんぶを ``||loops:Repeat times loop||`` に いれて、さかなの しゅうしゅうと おとどけを くりかえそう。

## Step 5
さいごに、フグも おなじように あつかおう。べつべつに やるのが おすすめだよ。

## フグ ずけい @unplugged
![Pufferfish Diagram](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/master/tutorials/seymour-island/images/task_5_map_pufferfish.jpg)
うえの ずを つかって、エージェントが さかなを おとどけするまでの きょりを はかろう！

```package
causeway-digital-makecode-extension=github:causewaydigital/pxt-causeway-digital-extension
```
