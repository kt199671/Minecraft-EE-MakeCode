


### @flyoutOnly 1

```template
//
```

# はじめに



# 0. はじめに

## エージェント @unplugged

これは エージェント です。エージェントは マインクラフトの なかで タスクを こなせる ちいさな ロボットです。うごいたり、ブロックを おいたり、ブロックを こわしたり できます。


![Agent](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_0_agent.jpg)

## はじめよう @unplugged

エージェントの つかいかたを れんしゅう しましょう。まず、エージェントを ダイヤモンドブロック から ゴールドブロック まで うごかす コードを かいてみよう。
![Agent moving](https://raw.githubusercontent.com/CausewayDigital/Minecraft-EE-MakeCode/main/tutorials/seymour-island/images/seymour_task_0_move.gif)

この ウィンドウを とじるには **esc** キーを おしてね。エージェントを さがしてみよう。
**C** キーを おすと もういちど ひらけるよ。

## コードを かこう
``||Agent:agent move||`` ブロックを ``||loops:on start||`` ブロックの なかに ドラッグしよう。
つぎに、**forward** を **left** に かえてね。
かずも かえる ひつようが あるかも...

コードを じっこう するには、みぎしたの **さいせい** ボタンを クリックしてね。

```blocks
    agent.move(LEFT, 2)
```

```package
seymour=github:kt199671/Minecraft-EE-MakeCode
```
