# MagicSea

MagicSea Game From War3 Map

=======
## 目录结构

- **Doc/**
- **UE4_Project/**
  - **Config/**
  - **Content/**
    - **Blueprints/**
    - **Effects/**
    - **Levels/**
    - **Models/**
    - **Textures/**
  - **Source/**
  - **Plugins/**
  - MagicSea.sln
  - MagicSea.uproject
- README.md
- 

```mermaid
graph TD

	GameInit["游戏初始化"] --设定BOSS数量--> RoleGrow
	subgraph GameCycleTitle["游戏循环"]
		RoleGrow["角色成长"] --等待时间结束--> BattleBoss["打BOSS"]
		--还有剩余的BOSS--> RoleGrow
	end
	BattleBoss --杀死所有BOSS--> GameWin["游戏胜利"]
	BattleBoss --杀不死Boss--> GameOver["游戏失败"]
```