# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## sessions_send 入参示例

```json
{
  "sessionKey": "agent:project_manager:feishu:project_manager:direct:ou_86e05fde861d65cbcc06f6e732d0b11d",
  "message": "任务描述内容...",
  "label": "可选的会话标签"
}
```

**关键要点**：
- 优先使用 `sessionKey` 精确指定目标智能体，**不要依赖 `label` 查找**
- `sessionKey` 格式：`agent:<agent_name>:<platform>:<agent_type>:<mode>:<ou_id>`
- `message` 字段传递实际任务内容
- `label` 为可选，仅用于会话标识

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

---

Add whatever helps you do your job. This is your cheat sheet.
