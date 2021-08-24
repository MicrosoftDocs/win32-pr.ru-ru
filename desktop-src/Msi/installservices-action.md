---
description: Действие Инсталлсервицес регистрирует службу для системы. Это действие запрашивает таблицу Сервицеинсталл.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Действие Инсталлсервицес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e37ea0a80050d6e9ab624ff878a352f96bbc0854fd64d6a1f563f277f1ea6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787024"
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

## <a name="remarks"></a>Remarks

Для выполнения этого действия пользователь должен быть администратором или обладать повышенными привилегиями с разрешением на установку служб или на то, что приложение является частью управляемой установки.

 

 



