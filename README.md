# zh-natural-writing

一个 Codex skill，用来把中文内容改得自然、直接，少一点 AI 味、翻译腔和套话。

它适合处理 README、技术文档、产品文案、UI 文案、提交信息、PR 描述、PPT 文案、公众号文章、社交媒体内容和 prompt。目标不是把文字伪装成“非 AI”，而是删掉没信息量的表达，把观点说清楚。

## 适合处理什么

- 去掉“首先、其次、综上所述”这类作文式结构
- 去掉“值得注意的是、不难发现”这类报告腔
- 去掉“充分体现、全面赋能、持续助力”这类自证式表达
- 减少“对于……而言、在……方面具有重要意义”这类翻译腔
- 把“提升体验、降低门槛、打造闭环”改成具体行为
- 保留必要术语、事实、约束和原本语气

## 目录

```text
skills/
  zh-natural-writing/
    SKILL.md                # skill 主说明
    agents/openai.yaml      # Codex 展示名和默认提示
    references/patterns.md  # 常见问题、替代表达和场景样例
```

## 安装

把 `skills/zh-natural-writing` 复制到 Codex 的 skills 目录：

```bash
mkdir -p ~/.codex/skills
cp -R skills/zh-natural-writing ~/.codex/skills/
```

然后在 Codex 里直接提到这个 skill，或用类似下面的说法触发：

```text
用 zh-natural-writing 帮我把这段 README 改自然一点。
```

也可以直接说：

```text
这段中文去一下 AI 味儿，别太翻译腔。
```

## 使用方式

只要给出中文文本和目标场景即可。比如：

```text
帮我把这段 PR 描述改得自然一点：

本 PR 主要对 Step 模块进行了优化，进一步提升了代码可维护性和整体稳定性。
```

输出会尽量直接给成品，不加“优化如下”“我帮你改成”这类前置说明。用户要求解释时，才会简短说明改了哪里。

## 维护建议

- 常见句式和替代表达放在 `references/patterns.md`
- 场景规则放在 `SKILL.md`
- 新增规则时尽量写成“什么时候删、什么时候改、改成什么方向”
- 不建议做机械替换表，同一个词在不同语境里可能该删，也可能该保留

## License

MIT
