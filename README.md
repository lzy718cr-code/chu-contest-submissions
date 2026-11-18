# CHU 点歌台 · 参赛任务分配与提交

2026 Qoder 高校创造力大赛（天池 532536）· 建议赛道 **LifeHack**（校园生活场景）
**论坛发帖截止：2026-11-30 18:00（硬性）**，内部节点提前留缓冲。

## 任务分配

| # | 任务 | 负责人 | 内部截止 | 交付物 | 文档 |
|---|---|---|---|---|---|
| 1 | 搭建 Supabase 演示数据库 | 队友 A | 11-20 | 演示库 + Project URL / anon key | [tasks/队友任务1-Supabase演示库.md](tasks/队友任务1-Supabase演示库.md) |
| 2 | Qoder Sites 部署 + 公网验收 | 队友 B | 11-23 | 公网网址 + 验收截图 | [tasks/队友任务2-Sites部署验收.md](tasks/队友任务2-Sites部署验收.md) |
| 3 | 天池论坛参赛帖 | 负责人（Qoder 辅助起草） | 11-28 | 已发布的帖子链接 | 发帖要求见下方 |

依赖关系：**任务 2 必须等任务 1 完成**（需要演示库的 URL / anon key / service key）。
任务 1 的 service key 由队友 A **私下**交给队友 B，不走群聊。

## 提交流程（写完交到这里）

1. 负责人在仓库 **Settings → Collaborators** 添加你的 GitHub 账号（或者你 fork 本仓库）。
2. 克隆：
   ```bash
   git clone https://github.com/lzy718cr-code/chu-contest-submissions.git
   ```
3. 在 `submissions/对应任务/` 下建一个**你的名字**文件夹，把该任务的 `提交模板.md` 复制进去改名 `完成报告-你的名字.md`，填写内容，截图放同一文件夹。
4. 提交推送：
   ```bash
   git add submissions/
   git commit -m "任务1完成报告-你的名字"
   git push
   ```
   fork 的同学推到自己 fork 后提 Pull Request。
5. 群里说一声，负责人验收。

## 安全红线（全员必读）

- ❌ **service_role / secret key** 不进群聊、不进代码、不进截图、不进本仓库。只在 Supabase Dashboard 和 Qoder Sites Settings → Secrets 两处出现。
- ❌ 任何 SQL **不得在正式站项目** `aiblivjuhccwcwwrwxsl.supabase.co` 运行（会清空正式数据）。演示库是新建的 `chu-contest-demo`。
- ✅ Project URL 和 anon key 是设计公开的值，可以写进报告和代码配置。
- ✅ 演示账号密码 `ChuDemo#2026` 是故意公开的（参赛帖要写给评委），不算泄密。

## 任务 3 发帖要求（负责人）

天池论坛帖必须包含：自我介绍 / 作品说明 / 怎么用（≤5 步）/ 用 Qoder 做出来的过程（**截图凭证**）/ 作品链接。
素材来源：任务 2 的部署过程截图 + 验收截图 + 公网网址 + 演示账号（judge@chu.demo / ChuDemo#2026）。
Qoder 开发过程截图从任务 1、2 执行时就注意留存。

## 相关仓库

- 参赛代码（`contest-demo` 分支）：https://github.com/lzy718cr-code/Chu-xiaomai/tree/contest-demo
- 本提交仓库：https://github.com/lzy718cr-code/chu-contest-submissions
- 正式站代码（只读参考，勿动）：https://github.com/chd-avril/Chu-xiaomai