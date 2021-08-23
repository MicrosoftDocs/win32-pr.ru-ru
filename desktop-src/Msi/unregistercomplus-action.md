---
description: Действие Унрегистеркомплус удаляет приложения COM+ из реестра.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Действие Унрегистеркомплус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3ed5e8e4afd853294e7f5832662e9aaf1eb122d3573e7c384115c86d994588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499854"
---
# <a name="unregistercomplus-action"></a>Действие Унрегистеркомплус

Действие Унрегистеркомплус удаляет приложения COM+ из реестра.

## <a name="sequence-restrictions"></a>Ограничения последовательности

[Действие регистеркомплус](registercomplus-action.md) должно следовать за [действием инсталлфилес](installfiles-action.md) и действием унрегистеркомплус.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Идентификатор приложения удаляемого приложения COM+. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Действие Регистеркомплус](registercomplus-action.md)
</dt> <dt>

[Таблица ComPlus](complus-table.md)
</dt> <dt>

[установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



