---
description: Действие Унрегистеркомплус удаляет приложения COM+ из реестра.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Действие Унрегистеркомплус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999678"
---
# <a name="unregistercomplus-action"></a>Действие Унрегистеркомплус

Действие Унрегистеркомплус удаляет приложения COM+ из реестра.

## <a name="sequence-restrictions"></a>Ограничения последовательности

[Действие регистеркомплус](registercomplus-action.md) должно следовать за [действием инсталлфилес](installfiles-action.md) и действием унрегистеркомплус.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Идентификатор приложения удаляемого приложения COM+. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Действие Регистеркомплус](registercomplus-action.md)
</dt> <dt>

[Таблица ComPlus](complus-table.md)
</dt> <dt>

[Установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



