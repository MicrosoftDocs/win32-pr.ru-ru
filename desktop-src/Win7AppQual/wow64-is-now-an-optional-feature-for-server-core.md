---
description: Подсистема WoW64 теперь является дополнительным компонентом для Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Состояние WoW64 в Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f836d361e172527bf23c7e51ea0071790d3857d6611d8a12ff62185226d3f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994474"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>Подсистема WoW64 теперь является дополнительным компонентом для Server Core

## <a name="affected-platforms"></a>Затронутые платформы

**серверы** — Windows Server 2008 R2  



## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** -низкая  





## <a name="description"></a>Описание

вариант установки server Core для Windows server 2008 R2 позволяет удалить WoW64. WoW64 теперь является необязательным компонентом, который можно удалить, если не требуется выполнять 32-разрядный код.

кроме того, для работы в Windows Server 2008 R2 ролям Active Directory и службы Active Directory облегченного доступа к каталогам требуется WoW64.

## <a name="manifestation-of-impact"></a>Влияние на манифесты

При удалении WoW64 администраторы, выполняющие 32-разрядный код в Server Core, получат сообщение об ошибке, которое не может быть выполнено. Если администраторы пытаются запустить Active Directory и службы Active Directory облегченного доступа к каталогам, они получат сообщение об ошибке.

## <a name="mitigation"></a>Меры по снижению риска

Установите WoW64.

## <a name="solution"></a>Решение

Предпочтительное решение — предоставить 64-разрядную версию кода, чтобы ее можно было использовать в Server Core без необходимости WoW64.

Как минимум, предоставьте документацию пользователя, указывая, что для запуска 32-разрядного кода они должны установить WoW64.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Совместимость, производительность, надежность и тестирование на удобство использования

Убедитесь, что весь используемый код является 64-битным.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [Сведения о реализации WOW64](../winprog64/wow64-implementation-details.md)
-   [Отладка WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
