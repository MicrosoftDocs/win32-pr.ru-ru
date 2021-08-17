---
description: API Центр обновления Windows Agent (WUA) — это набор COM-интерфейсов, которые позволяют системным администраторам и программистам получать доступ к Центр обновления Windows и Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows API агента обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e7e2c79a707424128082f8f3123cb5fff506a9fc98203ab1fdf8063393310d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738006"
---
# <a name="windows-update-agent-api"></a>Windows API агента обновления

## <a name="purpose"></a>Назначение

API Центр обновления Windows Agent (WUA) — это набор COM-интерфейсов, которые позволяют системным администраторам и программистам получать доступ к Центр обновления Windows и [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)). Сценарии и программы могут быть написаны для проверки того, какие обновления в настоящее время доступны для компьютера, а затем можно установить или удалить обновления.

## <a name="where-applicable"></a>Где применимо

Системные администраторы могут использовать WUA для программного определения того, какие обновления следует применить к компьютеру, загружать эти обновления, а затем устанавливать их без вмешательства пользователя или без него.

Независимые поставщики программного обеспечения (ISV) и разработчики конечных пользователей могут интегрировать функции WUA в систему управления компьютерами или по для управления обновлениями, чтобы обеспечить удобную рабочую среду.

## <a name="developer-audience"></a>Аудитория разработчиков

Вы можете писать приложения WUA на нескольких языках программирования. WUA определяет интерфейсы и объекты, доступные из Visual Basic, Visual Basic scripting Edition (VBScript), JScript и C и C++. Знание программирования COM полезно для программиста WUA.

## <a name="run-time-requirements"></a>Требования к среде выполнения

WUA поддерживается начиная с Windows XP. WUA поддерживается на сервере, начиная с Windows server 2003.

## <a name="in-this-section"></a>Содержание раздела

-   [использование API агента Центр обновления Windows](using-the-windows-update-agent-api.md)
-   [Справочник по API WUA](windows-update-agent--wua--api-reference.md)

 

 
