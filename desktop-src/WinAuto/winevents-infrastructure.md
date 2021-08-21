---
title: Инфраструктура Виневентс
description: операционная система Microsoft Windows включает в себя функцию с именем виневентс, которая позволяет процессам и приложениям, работающим на рабочем столе Windows, обмениваться определенными сведениями.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8662cdcbfa9546ce04dc787e7089f68ba1c03137c41067c20792f7da111cf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563289"
---
# <a name="winevents"></a>WinEvents

операционная система Microsoft Windows включает в себя функцию с именем *виневентс*, которая позволяет процессам и приложениям, работающим на рабочем столе Windows, обмениваться определенными сведениями. Специальные средства, использующие Microsoft UI Automation и Microsoft Active Accessibility, являются основными пользователями Виневентс.

В контексте доступности поставщики автоматизации пользовательского интерфейса и серверы Microsoft Active Accessibility используют Виневентс для уведомления клиентов об изменениях в пользовательском интерфейсе приложения, например при создании или удалении элемента пользовательского интерфейса или изменении имени, состояния или значения элемента.

В этом разделе приводятся рекомендации, рекомендации и примеры, помогающие клиентам справляться с Виневентс и помочь серверам определить, когда следует активировать соответствующий WinEvent.

## <a name="in-this-section"></a>Содержание раздела

-   [Что такое Виневентс?](what-are-winevents.md)
-   [Регистрация функции-обработчика](registering-a-hook-function.md)
-   [События системного уровня и Object-Level](system-level-and-object-level-events.md)
-   [Функции-обработчики в контексте и вне контекста](in-context-and-out-of-context-hook-functions.md)
-   [Защита от повторного входа в функции-ловушки](guarding-against-reentrancy-in-hook-functions.md)
-   [Выделение идентификаторов WinEvent](allocation-of-winevent-ids.md)

Общие сведения о процессе уведомления о событиях в Microsoft Active Accessibility см. в разделе [виневентс](winevents-overview.md) в [техническом обзоре](technical-overview.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Общая инфраструктура](common-infrastructure.md)
</dt> </dl>

 

 




