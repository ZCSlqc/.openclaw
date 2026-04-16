# Memory

## 2026-04-15

### 智能体协作规则（2026-04-15 15:58）

- **开发任务分派原则**：
  - 下发开发类任务时，**默认不新建临时智能体**。
  - 优先通过 `sessions_send` 将任务分派给已有的 `project_manager` 和 `full_stack_engineer` 智能体协作处理。
  - `project_manager`（项目经理）：负责进度管理、人员协调、风险控制，保障项目按时交付。
  - `full_stack_engineer`（全栈工程师）：负责前后端代码开发、功能实现与技术问题解决。
  - 只有在目标智能体不存在或用户明确要求新开会话时，才使用 `sessions_spawn`。

- **SessionKey 固定映射**：
  - `project_manager` → `agent:project_manager:feishu:project_manager:direct:ou_86e05fde861d65cbcc06f6e732d0b11d`
  - `full_stack_engineer` → `agent:full_stack_engineer:feishu:full_stack_engineer:direct:ou_5e976f1bebfd947610b5550fa70ef381`

- **调用优先级**：
  - 默认优先使用 `sessions_send(sessionKey=...)`，**不要使用 label 查找**。
