---
description: Действие Стопсервицес останавливает системные службы. Это действие запрашивает таблицу ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Действие Стопсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee0082d1588c3a1486b51bd4f06869374e1f6babfa71d309d65512e1ff1b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627384"
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



 

## <a name="remarks"></a>Remarks

Для выполнения этого действия необходимо, чтобы пользователь был администратором или иметь повышенные привилегии с разрешением на управление службами или что приложение является частью управляемой установки.

 

 



