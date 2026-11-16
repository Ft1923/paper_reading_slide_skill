# Claude Skills

## paper-deep-read-slides

把一篇学术论文 PDF 做成逐段中英对照的精读幻灯片：

- 每段：英文原文 + 中文译文 + 解读，长段落按意群拆页
- 每张图：在图上加色带、箭头、编号标注，并分步骤讲“怎么看”
- 最后：全文串讲、因果链、证据表、背景扩展、批判性阅读、关键数字速查
- 发布后可根据评论追加补充图解页

### 使用

把 `paper-deep-read-slides/` 文件夹放进 Claude 的技能目录（或在 Claude 中上传该技能），然后上传论文 PDF，说“精读这篇论文、做成 PPT”。

### 文件

- `paper-deep-read-slides/SKILL.md`：技能说明（工作流程、页面类型、图表标注方法、检查与迭代规则）
- `paper-deep-read-slides/figure-guides/`：电化学/电池论文常见图的读法库，一种图一份：
  CV/LSV、RDE/Levich/K–L、Tafel、EIS/DRT、XPS、XRD（含 2D-XRD 与织构）、SEM、镀剥库伦效率、全电池性能。
  每份包含：测什么、坐标轴、读图步骤、特征→含义对照表、标注建议、常见陷阱、案例库。
  读新论文后把经验追加到对应文件的“案例库”；新图类型用 `_TEMPLATE.md` 新建。
