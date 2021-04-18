---
description: Действие Инсталлсервицес регистрирует службу для системы. Это действие запрашивает таблицу Сервицеинсталл.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Действие Инсталлсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684355"
---
# <a name="installservices-action"></a>Действие Инсталлсервицес

Действие Инсталлсервицес регистрирует службу для системы. Это действие запрашивает [таблицу сервицеинсталл](serviceinstall-table.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие служб должно использоваться в следующей последовательности.

[стопсервицес](stopservices-action.md)

[делетесервицес](deleteservices-action.md)

Любое из следующих действий: [инсталлфилес](installfiles-action.md), [ремовефилес](removefiles-action.md), [дупликатефилес](duplicatefiles-action.md), [мовефилес](movefiles-action.md), [патчфилес](patchfiles-action.md)и [ремоведупликатефилес](removeduplicatefiles-action.md) .

инсталлсервицес

[стартсервицес](startservices-action.md)

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Комментарии

Для выполнения этого действия пользователь должен быть администратором или обладать повышенными привилегиями с разрешением на установку служб или на то, что приложение является частью управляемой установки.

 

 



