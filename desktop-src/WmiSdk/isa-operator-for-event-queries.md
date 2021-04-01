---
description: Оператор ISA — это зависящий от WQL оператор, который можно использовать в запросах событий. Когда ISA включается в предложение WHERE запроса события, он запрашивает уведомление о событиях для всех классов в иерархии классов, а не конкретного класса событий.
ms.assetid: 68b7a903-a206-4491-95c4-4a412537f6f5
ms.tgt_platform: multiple
title: Оператор ISA для запросов событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acdd262492bfd876867bdfa7e13fd50e5380270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081209"
---
# <a name="isa-operator-for-event-queries"></a>Оператор ISA для запросов событий

Оператор ISA — это зависящий от WQL оператор, который можно использовать в запросах событий. Когда ISA включается в [предложение WHERE](where-clause.md) запроса события, он запрашивает уведомление о событиях для всех классов в иерархии классов, а не конкретного класса событий.

В следующем примере запрашиваются уведомления каждые 10 минут событий изменения экземпляра для всех экземпляров, являющихся членами любого класса, производного от класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Дополнительные сведения об использовании ISA с запросом событий см. в разделе [Создание события таймера с помощью Win32 \_ LocalTime или Win32 \_ утктиме](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

 

 
