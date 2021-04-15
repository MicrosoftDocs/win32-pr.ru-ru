---
description: Оператор ISA — это зависящий от WQL оператор, который может использоваться в запросах данных, событий и схем.
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: Оператор ISA для запросов схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb50146e4bd1219712c84bc1acec7fc7d50146b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683892"
---
# <a name="isa-operator-for-schema-queries"></a>Оператор ISA для запросов схемы

Оператор ISA — это зависящий от WQL оператор, который может использоваться в запросах данных, событий и схем.

Когда ISA включается в [предложение WHERE](where-clause.md) запроса схемы, он запрашивает применение запроса ко всем подклассам указанного класса.

Например, следующая инструкция запрашивает уведомление каждые 10 минут событий изменения экземпляра для всех экземпляров, являющихся членами любого класса, производного от класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Следующий запрос возвращает определение для класса [**\_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor) и определений для всех его подклассов.


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



**\_ Класс meta** класса определяет это как запрос схемы, свойство, именуемое, **\_ \_** определяет целевой класс запроса, а оператор ISA запрашивает определения для подклассов целевого класса.

 

 
