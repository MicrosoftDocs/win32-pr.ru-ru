---
description: Действие Стартсервицес запускает системные службы. Это действие запрашивает таблицу ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Действие Стартсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673559"
---
# <a name="startservices-action"></a>Действие Стартсервицес

Действие Стартсервицес запускает системные службы. Это действие запрашивает [таблицу ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действия служб должны использоваться в следующей последовательности:

-   [стопсервицес](stopservices-action.md)
-   [делетесервицес](deleteservices-action.md)

Любое из следующих действий:

-   [инсталлфилес](installfiles-action.md)
-   [ремовефилес](removefiles-action.md)
-   [дупликатефилес](duplicatefiles-action.md)
-   [мовефилес](movefiles-action.md)
-   [патчфилес](patchfiles-action.md)
-   [ремоведупликатефилес](removeduplicatefiles-action.md)
-   [инсталлсервицес](installservices-action.md)
-   стартсервицес

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия |
|-------|----------------------------|
| \[1\] | Отображаемое имя службы.      |
| \[2\] | Имя службы.              |



 

## <a name="remarks"></a>Комментарии

Для выполнения этого действия необходимо, чтобы пользователь был администратором или иметь повышенные привилегии с разрешением на управление службами или что приложение является частью управляемой установки.

 

 



