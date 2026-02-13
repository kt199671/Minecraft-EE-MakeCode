


### @flyoutOnly 1

```template
//
```

# しゅうり

# 1. しゅうり

## しゅうり @unplugged

しゅうりよう の き が てに はいったよ。エージェントを しゅうりする ばしょまで うごかそう。
![Agent repair](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_0_place_move.gif)

## うごかそう
まず、エージェントを おくの エメラルド（みどり）ブロックの うえまで うごかそう。
できたら「つぎへ」を おしてね。

```blocks
agent.move(LEFT, 3)

```

## しゅうり @unplugged
エージェントが ただしい ばしょに ついたよ。きの ブロックを おいて ふねの せんたいを しゅうり しよう。
![Agent repair](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_0_place.gif)

## しゅうり
``||Agent:agent place left||`` コマンドを つかって、あつめた きの ブロックで ふねの せんたいを しゅうり しよう。

```blocks

agent.move(LEFT, 3)
agent.place(LEFT)


```


```package
seymour=github:kt199671/Minecraft-EE-MakeCode
```
