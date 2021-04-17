---
description: Действие Стопсервицес останавливает системные службы. Это действие запрашивает таблицу ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Действие Стопсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673437"
---
# <a name="stopservices-action"></a>Действие Стопсервицес

Действие Стопсервицес останавливает системные службы. Это действие запрашивает [таблицу ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действия служб должны использоваться в следующей последовательности:

-   стопсервицес
-   [делетесервицес](deleteservices-action.md)

Любое из следующих действий:

-   [инсталлфилес](installfiles-action.md)
-   [ремовефилес](removefiles-action.md)
-   [дупликатефилес](duplicatefiles-action.md)
-   [мовефилес](movefiles-action.md)
-   [патчфилес](patchfiles-action.md)
-   [ремоведупликатефилес](removeduplicatefiles-action.md)
-   [инсталлсервицес](installservices-action.md)
-   [стартсервицес](startservices-action.md)

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия |
|-------|----------------------------|
| \[1\] | Отображаемое имя службы.      |
| \[2\] | Имя службы.              |



 

## <a name="remarks"></a>Комментарии

Для выполнения этого действия необходимо, чтобы пользователь был администратором или иметь повышенные привилегии с разрешением на управление службами или что приложение является частью управляемой установки.

 

 



