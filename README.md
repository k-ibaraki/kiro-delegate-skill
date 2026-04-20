# kiro-delegate

AI エージェント向けスキル。`kiro-cli` にタスクを委譲して実行させます。

## 概要

ユーザーが「kiroに投げて」「kiroで実装して」など明示的に委譲を指示した場合のみ動作します。
一般的なコーディングタスクで自動発動することはありません。

## インストール

### GitHub CLI（推奨）

```bash
# プレビュー
gh skill preview k-ibaraki/kiro-delegate-skill

# インストール
gh skill install k-ibaraki/kiro-delegate-skill
```

`--agent` と `--scope` でインストール先を指定できます：

```bash
# Claude Code にユーザースコープでインストール
gh skill install k-ibaraki/kiro-delegate-skill --agent claude-code --scope user
```

### 手動

```bash
git clone https://github.com/k-ibaraki/kiro-delegate-skill.git /tmp/kiro-delegate-skill
cp -r /tmp/kiro-delegate-skill/kiro-delegate ~/.claude/skills/
```

## 前提条件

- [kiro-cli](https://kiro.dev) がインストール済みであること（v2.0.0 以上）
- `kiro-cli login` でログイン済みであること

## 使い方

以下のように指示するだけです：

```
この機能を kiro に実装してもらって
```

```
use kiro to fix this bug
```

スキルが自動的に kiro-cli を呼び出し、タスクを委譲します。

## ライセンス

MIT
