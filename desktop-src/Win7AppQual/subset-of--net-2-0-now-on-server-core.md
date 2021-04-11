---
description: .
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Подмножество .NET 2,0 теперь в Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e0f836ca7afaef920429df17ef8be845ce92e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273087"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Подмножество .NET 2,0 теперь в Server Core

## <a name="platform"></a>Платформа

**Серверы** — Windows Server 2008 R2  



## <a name="feature-impact"></a>Воздействие на функции

 **Серьезность** — низкая  
**Частота** -низкая  





## <a name="description"></a>Описание

Вариант установки Server Core для Windows Server 2008 R2 теперь включает подмножество платформа .NET Framework 2,0. Подмножество — это функциональность в .NET 2,0, которая соответствует функциональным возможностям в Server Core; в базу Server Core не были добавлены двоичные файлы, чтобы разрешить функционирование любой части .NET 2,0.

В варианте установки Server Core для Windows Server 2008 не поддерживалась поддержка .NET.

## <a name="manifestation-of-impact"></a>Влияние на манифесты

Это позволяет запускать в Windows Server 2008 R2 некоторые приложения на основе .NET 2,0.

## <a name="testing"></a>Тестирование

Убедитесь, что используемые в коде классы .NET входят в ядро сервера. Также протестируйте все приложения, которые запускают этот код в Server Core.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Блог Server Core](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *См. также* раздел Server Core *пакета SDK для Windows Server 2008 R2* , когда он станет доступен

> [!Note]  
> Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.

 

 

 
