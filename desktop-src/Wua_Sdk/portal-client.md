---
description: API Центр обновления Windows Agent (WUA) — это набор COM-интерфейсов, которые позволяют системным администраторам и программистам получать доступ к Центр обновления Windows и Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API агента Центр обновления Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808650"
---
# <a name="windows-update-agent-api"></a>API агента Центр обновления Windows

## <a name="purpose"></a>Назначение

API Центр обновления Windows Agent (WUA) — это набор COM-интерфейсов, которые позволяют системным администраторам и программистам получать доступ к Центр обновления Windows и [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)). Сценарии и программы могут быть написаны для проверки того, какие обновления в настоящее время доступны для компьютера, а затем можно установить или удалить обновления.

## <a name="where-applicable"></a>Где применимо

Системные администраторы могут использовать WUA для программного определения того, какие обновления следует применить к компьютеру, загружать эти обновления, а затем устанавливать их без вмешательства пользователя или без него.

Независимые поставщики программного обеспечения (ISV) и разработчики конечных пользователей могут интегрировать функции WUA в систему управления компьютерами или по для управления обновлениями, чтобы обеспечить удобную рабочую среду.

## <a name="developer-audience"></a>Аудитория разработчиков

Вы можете писать приложения WUA на нескольких языках программирования. WUA определяет интерфейсы и объекты, доступные из Visual Basic, Visual Basic Scripting Edition (VBScript), JScript и C и C++. Знание программирования COM полезно для программиста WUA.

## <a name="run-time-requirements"></a>Требования к среде выполнения

WUA поддерживается начиная с Windows XP. WUA поддерживается на сервере, начиная с Windows Server 2003.

## <a name="in-this-section"></a>Содержание раздела

-   [Использование API агента Центр обновления Windows](using-the-windows-update-agent-api.md)
-   [Справочник по API WUA](windows-update-agent--wua--api-reference.md)

 

 
