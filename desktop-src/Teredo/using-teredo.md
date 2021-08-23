---
title: Использование Teredo
description: При разработке приложения, использующего Teredo, цель состоит в том, чтобы обеспечить подключение IPv6 и не сосредоточиться на использовании Teredo.
ms.assetid: 043bc826-1387-4994-96b1-115df2f6ea2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ddee98d9ea873b3949dbc45daee7b1d53062a83a4f1454953d0ad75ae786655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139157"
---
# <a name="using-teredo"></a>Использование Teredo

При разработке приложения, использующего [Teredo](about-teredo.md), цель состоит в том, чтобы обеспечить подключение IPv6 и не сосредоточиться на использовании Teredo. например, Windows пространство совещания и удаленный помощник — это два приложения, которые используют преимущества сквозного подключения, предоставляемого протоколом IPv6. Эти приложения могут получать подключения с помощью собственных адресов IPv6, 6to4 или Teredo. Для этих приложений и других компонентов, которые могут быть разработаны для IPv6, Teredo обрабатывается как любой другой протокол, обеспечивающий подключение.

В следующих разделах описаны стандартные сценарии использования, которые возникают при использовании интерфейса Teredo.

-   [Реализация Teredo](implementing-teredo.md)
-   [Реализация модели безопасности Teredo](implementing-the-teredo-security-model.md)
-   [Получение запрошенного трафика через Teredo](receiving-solicited-traffic-over-teredo.md)
-   [Получение незапрошенного трафика через Teredo](receiving-unsolicited-traffic-over-teredo.md)
-   [Использование Teredo с вспомогательным модулем IP](using-teredo-with-ip-helper.md)
-   [использование Teredo в Windows XP](using-teredo-in-windows-xp.md)

 

 




