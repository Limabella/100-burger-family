# 100 Burger Family

100 Burger Family is being rebuilt as an Unreal Engine 5 cooking simulation MVP.

The previous Unity project is preserved under `legacy-unity/` for reference only.

## Story and Session Goal

Families wind MaAM's great spring to bring a restaurant's peak-time service to life. The target is a 5–10 minute session, with family cooperation shortening completion time for the same set of orders.

[The First Peak-Time Spring — story and cooperative play design (Korean)](docs/PEAK_TIME_WINDING_STORY.md)

This is a design target, not a claim that the winding or family co-op features are implemented.

## Direction

```text
Engine: Unreal Engine 5
Workflow: Blueprint-first
Template: Top Down Template
Target: Windows playable MVP first
```

## Core Loop

```text
Harvest -> Cook -> Serve -> Score
```

## MVP Scope

- top-down player movement
- interact key
- farm station
- cook station
- serve counter
- score HUD
- timer HUD
- one playable map

## Repository Layout

```text
100-burger-family/
  README.md
  AGENTS.md
  PROJECT_CONTEXT.md
  TODO.md
  docs/
    UE5_MIGRATION_PLAN.md
  unreal-game/
    100BurgerFamily.uproject
  legacy-unity/
    unity-game/
    My project/
    100-burger-family.sln
```

## UE5 Content Plan

```text
Content/
  BurgerFamily/
    Blueprints/
      Core/
      Player/
      Stations/
      UI/
    Data/
    Maps/
    Materials/
    Art/
    Input/
```

## Initial Blueprint Classes

```text
BP_PlayerCharacter
BP_InteractableBase
BP_FarmStation
BP_CookStation
BP_ServeCounter
BP_OrderManager
BP_GameMode_BurgerFamily
WBP_HUD
DA_Ingredient
DA_Recipe
```

## Development Rules

- gameplay first
- Blueprint-first
- minimal C++ only when needed
- prefer UE5 templates and Fab assets
- keep the first playable map simple
- avoid production-scale systems before the MVP works

## Legacy Unity

The Unity version is archived in:

```text
legacy-unity/
```

Use it only for:
- gameplay reference
- old loop reference
- UI/flow notes
- asset reference

Do not continue Unity implementation unless explicitly requested.
