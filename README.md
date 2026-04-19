# kiro-delegate

Claude Code のスキル。`kiro-cli` にタスクを委譲して実行させます。

## 概要

ユーザーが「kiroに投げて」「kiroで実装して」など明示的に委譲を指示した場合のみ動作します。
一般的なコーディングタスクで自動発動することはありません。

## インストール

```bash
mkdir -p ~/.claude/skills/kiro-delegate
cp SKILL.md ~/.claude/skills/kiro-delegate/
```

または `git clone` して配置：

```bash
git clone https://github.com/k-ibaraki/kiro-delegate-skill.git ~/.claude/skills/kiro-delegate
```

## 前提条件

- [kiro-cli](https://kiro.dev) がインストール済みであること（v2.0.0 以上）
- `kiro-cli login` でログイン済みであること

## 使い方

Claude Code で以下のように指示するだけです：

```
この機能を kiro に実装してもらって
```

```
use kiro to fix this bug
```

スキルが自動的に kiro-cli を呼び出し、タスクを委譲します。

## ライセンス

MIT
