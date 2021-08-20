---
description: Действие Делетесервицес останавливает службу и удаляет ее регистрацию из системы. Это действие запрашивает таблицу ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Действие Делетесервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd00b9d077239402817bdf40dc10ee1de9bdbff4b52998742434933c3e9dd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379120"
---
# <a name="deleteservices-action"></a>Действие Делетесервицес

Действие Делетесервицес останавливает службу и удаляет ее регистрацию из системы. Это действие запрашивает [таблицу ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действия служб должны использоваться в следующей последовательности:

1.  [стопсервицес](stopservices-action.md)
2.  делетесервицес
3.  Любое из следующих действий: [инсталлфилес](installfiles-action.md), [ремовефилес](removefiles-action.md), [дупликатефилес](duplicatefiles-action.md), [мовефилес](movefiles-action.md), [патчфилес](patchfiles-action.md)и [ремоведупликатефилес](removeduplicatefiles-action.md) .
4.  [Действие Инсталлсервицес](installservices-action.md)
5.  [стартсервицес](startservices-action.md)

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия |
|-------|----------------------------|
| \[1\] | Отображаемое имя службы.      |
| \[2\] | Имя службы.              |



 

## <a name="remarks"></a>Remarks

Для выполнения этого действия пользователь должен быть администратором или обладать повышенными привилегиями с разрешением на удаление служб или на то, что приложение является частью управляемой установки.

 

 



