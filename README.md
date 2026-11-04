# tani2shell

Black-box pentest labs, one exploit story per repo — every lab is **home-grown, battle-tested by an autonomous AI pentest agent, and shipped with a full write-up** (challenge brief → solution walk-through → difficulty calibration, in English / 日本語 / 中文).

## The *2Shell series

| Lab | Exploit story | Difficulty (calibrated) | Solved by AI agent |
|---|---|---|---|
| [node2shell-lab](https://github.com/tani2shell/node2shell-lab) | Node.js `zlib` brotli crash chain (CVE-2026-111497), crash-gated double flag | 3.5/5 | full chain, factory-measured |
| [php2shell-lab](https://github.com/tani2shell/php2shell-lab) | PHP2Shell-era heap-disclosure chain (CVE-2026-109618/109619) + SUID symlink privesc | 4/5 nominal · 3.5/5 live-fire | both flags, ~15 min best run |

## The lab lineup

| Lab | Exploit story | Difficulty (calibrated) | Solved by AI agent |
|---|---|---|---|
| [egresslock-lab](https://github.com/tani2shell/egresslock-lab) | Blind SSTI → DNS egress exfiltration → Docker socket escape, three knowledge domains in one chain | 3.5/5 | both flags |
| [timing-gate-lab](https://github.com/tani2shell/timing-gate-lab) | Timing side-channel with zero error feedback — recover a secret from HTTP codes and milliseconds | 3.5/5 | held across two live runs |
| [actions-lab](https://github.com/tani2shell/actions-lab) | CI/CD trust chain: script injection in a commit message → shared-runner credential → queue-box master key | 2.5–3/5 | both flags |
| [verdant-onboarding-lab](https://github.com/tani2shell/verdant-onboarding-lab) | AI-agent flavored portal: guardrail bypass → retrieval dominance → argv smuggling → sudo config-hook privesc | 3.5/5 | both flags |
| [voltmart-lab](https://github.com/tani2shell/voltmart-lab) | E-commerce + multi-tenant merge-mayhem: mass assignment, command injection, SQLi → SSRF `file://` cross-container reads | 3/5 | both flags |
| [drill-web-lab](https://github.com/tani2shell/drill-web-lab) | Five flags, five weapon classes: SQLi, reflected XSS, stored XSS + admin bot, command injection, custom-protocol metrics | 2.5/5 | 7/7 flags (joint run) |
| [drill-kernel-lab](https://github.com/tani2shell/drill-kernel-lab) | arm64 kernel privesc as a real VM (UTM/QEMU): one frozen vulnerable kernel, the kernel *is* the target | 3/5 | both flags |
| [xbow-ammobox-lab](https://github.com/tani2shell/xbow-ammobox-lab) | Suite: five single-issue web-vuln rounds, one app + one port + one flag each — an ammo box for drilling agents | 2/5 (hint-on) | 5/5 first blood |

## What makes a tani2shell lab different

- **CHALLENGE.md** — true black-box brief, zero spoiler.
- **SOLUTION.md** — complete kill chain with every command, offsets, and the actual flag values (a write-up without the flag is a write-up without the ending).
- **DIFFICULTY.md** — nominal rating vs. live-fire calibration, with the reasoning behind it.
- **RESET.sh** — one command back to factory state.
- Every lab was attacked by an AI pentest agent before it was published; if the agent couldn't break it (or broke it in a way we didn't design), we fixed the lab, not the story.

## The rules

1. Only labs built from scratch get published — no repackaged upstream CTF images.
2. Every lab must be broken end-to-end by an autonomous agent before it ships.
3. Fix the lab before you blame the player.

*New labs land here as soon as they survive first contact — watch this space.*

---

## 中文

黑盒渗透靶场，一个仓库讲透一条漏洞利用链——每个靶场都是**自研建造、由自主 AI 渗透 agent 实战打穿后出厂，并附完整题解**（挑战简报 → 解题全过程 → 难度校准，英日中三语）。

### *2Shell 系列

| 靶场 | 漏洞利用链 | 难度（实测校准） | AI agent 通关记录 |
|---|---|---|---|
| [node2shell-lab](https://github.com/tani2shell/node2shell-lab) | Node.js `zlib` brotli 崩溃链（CVE-2026-111497），崩溃门控双 flag | 3.5/5 | 全链通关，工厂实测 |
| [php2shell-lab](https://github.com/tani2shell/php2shell-lab) | PHP2Shell 时代堆内存泄露链（CVE-2026-109618/109619）+ SUID 符号链接提权 | 标称 4/5 · 实弹 3.5/5 | 双 flag，最快约 15 分钟 |

### 靶场矩阵

| 靶场 | 漏洞利用链 | 难度（实测校准） | AI agent 通关记录 |
|---|---|---|---|
| [egresslock-lab](https://github.com/tani2shell/egresslock-lab) | 盲注 SSTI → DNS 出网外带 → Docker socket 逃逸，一条链吃三个知识域 | 3.5/5 | 双 flag |
| [timing-gate-lab](https://github.com/tani2shell/timing-gate-lab) | 零报错反馈计时侧信道——只靠 HTTP 状态码和毫秒数恢复密钥 | 3.5/5 | 两轮实弹均破 |
| [actions-lab](https://github.com/tani2shell/actions-lab) | CI/CD 信任链：commit message 注参 → 共享 runner 凭据 → 队列机主密钥 | 2.5–3/5 | 双 flag |
| [verdant-onboarding-lab](https://github.com/tani2shell/verdant-onboarding-lab) | AI agent 风入职门户：护栏绕过 → 检索主导 → argv 走私 → sudo 配置钩子提权 | 3.5/5 | 双 flag |
| [voltmart-lab](https://github.com/tani2shell/voltmart-lab) | 电商+多租户合并灾难：批量赋值、命令注入、SQLi → SSRF `file://` 跨容器读取 | 3/5 | 双 flag |
| [drill-web-lab](https://github.com/tani2shell/drill-web-lab) | 五旗五武器：SQLi、反射 XSS、存储 XSS+管理员 bot、命令注入、自定义协议 metrics | 2.5/5 | 7/7 旗（联合靶场） |
| [drill-kernel-lab](https://github.com/tani2shell/drill-kernel-lab) | arm64 内核提权真 VM（UTM/QEMU）：一颗冻结的易受攻击内核，内核就是靶 | 3/5 | 双 flag |
| [xbow-ammobox-lab](https://github.com/tani2shell/xbow-ammobox-lab) | 套件：五个单漏洞 web 回合，一应用一口一旗——agent 刷题弹药箱 | 2/5（带类别提示） | 5/5 首破 |

### 每个仓库标配

- **CHALLENGE.md** — 真黑盒简报，零剧透
- **SOLUTION.md** — 完整击杀链：每条命令、偏移量、真实 flag 值（不给 flag 的题解等于没写结局）
- **DIFFICULTY.md** — 标称难度 vs 实弹校准，附定级依据
- **RESET.sh** — 一条命令恢复出厂状态
- 每个靶场发布前都先被 AI 渗透 agent 打了一遍；agent 打不穿（或用我们没设计到的方式打穿了），改的是靶场，不是故事。

### 发布三准则

1. 只发从零自建的靶场——不收上游 CTF 镜像换皮。
2. 每个靶场出厂前必须被自主 agent 端到端打穿。
3. 先修靶场，再怪玩家。

*新靶场经受住首波打击后即上线——敬请期待。*

---

## 日本語

ブラックボックス型pentestラボ。1リポジトリ＝1本のエクスプロイトストーリー。すべてのラボは**自作構築・自律AI pentestエージェントによる実戦撃破検証済み・完全書き下ろし解答付き**（チャレンジ概要 → 攻略フルウォークスルー → 難易度キャリブレーション、日英中3言語対応）。

### *2Shell シリーズ

| ラボ | エクスプロイト概要 | 難易度（実測補正） | AIエージェント攻略記録 |
|---|---|---|---|
| [node2shell-lab](https://github.com/tani2shell/node2shell-lab) | Node.js `zlib` brotli クラッシュチェーン（CVE-2026-111497）、クラッシュ連動ダブルフラグ | 3.5/5 | フルチェーン攻略、工場計測 |
| [php2shell-lab](https://github.com/tani2shell/php2shell-lab) | PHP2Shell時代のヒープ情報漏洩チェーン（CVE-2026-109618/109619）＋SUIDシンボリックリンク権限昇格 | 公称4/5・実戦3.5/5 | フラグ両方、最速約15分 |

### ラボラインナップ

| ラボ | エクスプロイト概要 | 難易度（実測補正） | AIエージェント攻略記録 |
|---|---|---|---|
| [egresslock-lab](https://github.com/tani2shell/egresslock-lab) | ブラインドSSTI → DNSエグレス持ち出し → Docker socketエスケープ、1本のチェーンに3つの知識ドメイン | 3.5/5 | フラグ両方 |
| [timing-gate-lab](https://github.com/tani2shell/timing-gate-lab) | エラーフィードバックゼロのタイミング側チャネル——HTTPステータスとミリ秒だけで秘密を復元 | 3.5/5 | 2回の実戦で攻略 |
| [actions-lab](https://github.com/tani2shell/actions-lab) | CI/CD信頼チェーン：commit message引数注入 → 共有runner認証情報 → キューボックスのマスターキー | 2.5–3/5 | フラグ両方 |
| [verdant-onboarding-lab](https://github.com/tani2shell/verdant-onboarding-lab) | AIエージェント風オンボーディングポータル：ガードレール迂回 → 検索支配 → argvスマグリング → sudo設定フック権限昇格 | 3.5/5 | フラグ両方 |
| [voltmart-lab](https://github.com/tani2shell/voltmart-lab) | ECサイト＋マルチテナント統合の悲鳴：mass assignment、コマンドインジェクション、SQLi → SSRF `file://` コンテナ間読み取り | 3/5 | フラグ両方 |
| [drill-web-lab](https://github.com/tani2shell/drill-web-lab) | 5フラグ5武器：SQLi・リフレクトXSS・ストレージXSS＋管理者ボット・コマンドインジェクション・独自プロトコルmetrics | 2.5/5 | 7/7フラグ（合同演習） |
| [drill-kernel-lab](https://github.com/tani2shell/drill-kernel-lab) | arm64カーネル権限昇格の実VM（UTM/QEMU）：凍結された脆弱カーネル1発、ターゲットはカーネルそのもの | 3/5 | フラグ両方 |
| [xbow-ammobox-lab](https://github.com/tani2shell/xbow-ammobox-lab) | スイート：単一脆弱性Webラウンド×5、1アプリ1ポート1フラグ——エージェント演習用弾薬箱 | 2/5（クラスヒントあり） | 5/5ファーストブラッド |

### 全リポジトリ共通の定番構成

- **CHALLENGE.md** — 真のブラックボックス概要、ネタバレゼロ
- **SOLUTION.md** — 完全キルチェーン：全コマンド・オフセット・実際のフラグ値まで（フラグなしの解説は結びのない小説と同じ）
- **DIFFICULTY.md** — 公称難易度 vs 実戦補正、格付け根拠付き
- **RESET.sh** — 1コマンドで工場状態に復元
- 公開前に必ずAI pentestエージェントに殴らせています。エージェントが破れない（または設計外の壊し方をした）場合、直すのはストーリーではなくラボの方。

### 公開三原則

1. 自作構築のラボのみ公開——上流CTFイメージの着せ替えはなし。
2. 全ラボは自律エージェントによるエンドツーエンド攻略検証を通過してから出荷。
3. プレーヤーを責める前に、ラボを直せ。

*新ラボはファーストコンタクトを生き延び次第、随時公開——お楽しみに。*
