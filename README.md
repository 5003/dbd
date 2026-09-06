# delegate-by-design

AI に仕事を任せる仕組みを「人が設計し続ける」ための 2 つの Agent Skill。スキル名の接頭辞 `dbd-` は delegate-by-design の略で、一覧で所属が分かるようにしている。

| 名前 | 役割 |
|---|---|
| `skills/dbd-design-delegation` | 中身: AI に業務を任せる仕組みを設計・実装・レビューするときの 6 原則と一線、リポジトリの 7 つの置き場所と置き場所ごとの命名 |
| `skills/dbd-write-skill` | 形: SKILL.md を書く・直す・レビューするときの技術仕様 (フロントマター、9 ブロック、モード、不変条件、受け入れ条件、evals) |

2 つのスキルは分担して働く。形の不適合は `dbd-write-skill`、中身の不適合は `dbd-design-delegation` が指摘し、evals の実行と description の最適化は `skill-creator` に任せる。

## 使い方

Claude Code の場合、`skills/` 以下をプロジェクトの `.claude/skills/` にコピーする。

```sh
cp -r skills/* <your-project>/.claude/skills/
```

各スキルは `evals/evals.json` (生成 / レビュー / 不可侵 / 非発火) を持つ。実行は skill-creator の手順に従う。

## 前提

AI に任せた仕事の失敗は、モデルの能力不足よりも、渡した文脈の設計不良から起きることのほうが多い。だから品質は、モデルを選ぶことではなく、仕事の切り方・文脈の渡し方・完了の決め方で作る。

## ライセンス

MIT (LICENSE)

## 著者

Yas — https://github.com/5003
