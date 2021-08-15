---
description: Подмножество .NET 2,0 теперь в Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Подмножество .NET 2,0 теперь в Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9da259186f0eaea7999df6dde6d42d972484c35eee24c9b9efb7fc6a5d882b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994634"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Подмножество .NET 2,0 теперь в Server Core

## <a name="platform"></a>Платформа

**серверы** — Windows Server 2008 R2  



## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** -низкая  





## <a name="description"></a>Описание

вариант установки server Core для Windows server 2008 R2 теперь включает подмножество платформа .NET Framework 2,0. Подмножество — это функциональность в .NET 2,0, которая соответствует функциональным возможностям в Server Core; в базу Server Core не были добавлены двоичные файлы, чтобы разрешить функционирование любой части .NET 2,0.

в варианте установки server Core для Windows server 2008 не поддерживалась поддержка .net.

## <a name="manifestation-of-impact"></a>Влияние на манифесты

это позволяет запускать некоторые приложения на основе .net 2,0 в server Core в Windows server 2008 R2.

## <a name="testing"></a>Тестирование

Убедитесь, что используемые в коде классы .NET входят в ядро сервера. Также протестируйте все приложения, которые запускают этот код в Server Core.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Блог Server Core](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *см. также* раздел server Core *пакета SDK Windows server 2008 R2* , когда он станет доступен

> [!Note]  
> Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.

 

 

 
