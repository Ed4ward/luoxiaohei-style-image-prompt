# 罗小黑风格图片提示词

`luoxiaohei-style-image-prompt` 是一个 Codex 技能。输入真实地点、人物、动物或日常物件，它会写出一帧手绘二维动画的图片提示词。它也能把短字藏进砖面、店招或小道具，作为放大画面才会留意到的彩蛋。

## 试用

- `用 $luoxiaohei-style-image-prompt，给雨后的北京故宫写一个带藏字彩蛋的提示词，不用出图。`
- `用 $luoxiaohei-style-image-prompt，画一张老街修伞摊的二维动画画面，把「只补晴天」藏在摊位侧边。`
- `用 $luoxiaohei-style-image-prompt，把这张马克杯照片画成二维动画，保留杯身花纹。`

想指定标题、对白或画中的准确字样时，直接在请求里写明内容和位置。想画一张无字图时，可以说「画面不加字」。

## 安装

取得项目后，在仓库根目录执行下面的命令。若已安装同名技能，请先处理已有版本。

```sh
mkdir -p "$HOME/.agents/skills" &&
  test ! -e "$HOME/.agents/skills/luoxiaohei-style-image-prompt" &&
  cp -R skills/luoxiaohei-style-image-prompt "$HOME/.agents/skills/"
```

在 Codex 中输入 `$luoxiaohei-style-image-prompt` 调用。安装路径见 [Codex 技能文档](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)。

## 文件

| 文件 | 内容 |
| --- | --- |
| [`SKILL.md`](skills/luoxiaohei-style-image-prompt/SKILL.md) | 提示词模板、藏字规则与出图流程 |
| [`references/luoxiaohei-visual-style.md`](skills/luoxiaohei-style-image-prompt/references/luoxiaohei-visual-style.md) | 二维动画画法、文字载体和完整示例 |
| [`agents/openai.yaml`](skills/luoxiaohei-style-image-prompt/agents/openai.yaml) | 技能名称、简介与调用示例 |

## 灵感来源（Inspiration）

- **技能结构**。参考 [xiaoTN/zelda-style-image-prompt](https://github.com/xiaoTN/zelda-style-image-prompt) 的组织方式，将简短的提示词模板与独立的视觉参考文档放在一起。
- **动画美术**。参考木头（MTJJ）与寒木春华的《罗小黑战记》的二维画面和日常奇幻质感。关于创作过程，见[导演木头访谈](https://media.people.com.cn/n1/2019/0919/c40606-31361084.html)。
- **画中藏字**。参考番剧把署名藏进砖块、树影等背景，以及电影把玩笑写进道具文字的做法。本技能用原创字样和载体示例演示这一方法。关于藏字位置，见[澎湃号·湃客的番剧回顾](https://www.thepaper.cn/newsDetail_forward_34486074)。
