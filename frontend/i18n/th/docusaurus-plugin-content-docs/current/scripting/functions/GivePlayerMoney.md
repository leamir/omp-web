---
title: GivePlayerMoney
sidebar_label: GivePlayerMoney
description: Give money to or take money from a player.
tags: ["player"]
---

## คำอธิบาย

Give money to or take money from a player.

| Name     | Description                                                              |
| -------- | ------------------------------------------------------------------------ |
| playerid | The ID of the player to give money to or take money from.                |
| money    | The amount of money to give the player. Use a minus value to take money. |

## ส่งคืน

1: The function was executed successfully.

0: The function failed to execute. This means the player is not connected.

## ตัวอย่าง

```c
public OnPlayerDeath(playerid, killerid, WEAPON:reason)
{
    if (killerid != INVALID_PLAYER_ID)
    {
       // Award $1000 to the killer
       GivePlayerMoney(killerid, 1000);
       SendClientMessage(killerid, -1, "You have been awarded $1000 for the kill.");
    }

    // Take $500 from the player who died.
    GivePlayerMoney(playerid, -500);
}
```

## ฟังก์ชั่นที่เกี่ยวข้องกัน

- ResetPlayerMoney: Set the money of a player to \$0.
- GetPlayerMoney: Check how much money a player has.
