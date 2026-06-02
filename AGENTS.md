# AGENTS.md

## 项目定位

本项目用于维护 CC 虚拟个人 IP 的表情包与梗图素材。CC 是一个干净、可爱、友好的年轻办公室职员风格 2D 卡通角色，当前重点是生成可持续复用的表情包素材。

后续代理接手项目时，应优先阅读并遵守这些文件：

- `README.md`：项目方向与目录说明
- `manifest.json`：表情包清单、状态与素材元数据
- `docs/workflow.md`：表情包生产流程
- `docs/qa-checklist.md`：最终素材验收标准
- `references/cc-character-spec.md`：CC 角色设定与一致性规则
- `references/cc-office-environment-spec.md`：默认办公室背景设定
- `prompts/sticker-template.prompt.md`：表情包生成提示词模板

## 表情包生成规范

- 每次只生成一个表情包概念，不生成多格合集、九宫格或表情包 sheet。
- 角色必须保持 CC 的核心识别点：短黑发、黑色矩形眼镜、紧凑柔和的圆角方形 / U 形脸、饱满脸颊、浅灰卫衣或简洁办公室休闲装。
- 风格保持干净可爱的 2D 卡通表情包风格：清晰线条、柔和上色、简单明快的表情、适合小尺寸识别。
- 构图以单角色为主，居中并留足边距；根据表情含义选择半身或全身视角，确保表情、手势和道具清楚。
- 背景优先选择与当前表情包主题相近的场景。例如加班、摸鱼、开会、庆祝、崩溃等主题，应匹配对应语境。
- 如果主题模糊、没有明确场景，或无法判断合适背景，则优先采用 `references/cc-office-environment-spec.md` 描述的标准办公室工位背景，并参考 `assets/cc/reference/cc-office-environment-final.png` 的画面风格。
- 背景不得抢占主体；应保持干净、简洁、低干扰，让 CC 的表情和动作优先被看见。
- 不依赖 AI 生成文字表达含义；如需中文文案，后续人工添加。
- 禁止生成随机文字、乱码、Logo、水印、复杂杂乱背景、额外角色、照片写实风、3D 塑料质感、严重肢体错误或明显跑脸。

## 生产流程规则

- 使用 `prompts/sticker-template.prompt.md` 作为单个表情包生成的基础模板。
- 用表情含义替换 `<emotion_or_action>`，用具体姿态和表情描述替换 `<pose_expression_detail>`。
- 草稿保存到 `assets/cc/drafts/`。
- 通过验收的最终素材保存到 `assets/cc/stickers/`。
- 最终文件名使用 `cc-sticker-###-slug.png` 格式，例如 `cc-sticker-001-happy.png`。
- 每个最终素材通过后，必须同步更新 `manifest.json`，保留 ID、slug、含义、提示词来源、最终路径、状态和必要备注。

## 验收重点

- CC 的短黑发、黑色矩形眼镜、紧凑柔和脸型和干净可爱风格没有跑偏。
- 表情或动作不依赖文字也能读懂。
- 小尺寸下脸部、手势、轮廓和关键道具仍然清楚。
- 没有生成文字、水印、Logo、随机字母、错误手指、破损眼镜、融化道具或明显解剖错误。
- 背景服务于当前主题，并且不干扰角色主体。
- 最终文件路径、命名和 `manifest.json` 记录一致。
