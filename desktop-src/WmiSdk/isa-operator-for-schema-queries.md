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
# <a name="isa-operator-for-schema-queries"></a><span data-ttu-id="d173d-103">Оператор ISA для запросов схемы</span><span class="sxs-lookup"><span data-stu-id="d173d-103">ISA Operator for Schema Queries</span></span>

<span data-ttu-id="d173d-104">Оператор ISA — это зависящий от WQL оператор, который может использоваться в запросах данных, событий и схем.</span><span class="sxs-lookup"><span data-stu-id="d173d-104">The ISA operator is a WQL-specific operator that can be used in data, event, and schema queries.</span></span>

<span data-ttu-id="d173d-105">Когда ISA включается в [предложение WHERE](where-clause.md) запроса схемы, он запрашивает применение запроса ко всем подклассам указанного класса.</span><span class="sxs-lookup"><span data-stu-id="d173d-105">When ISA is included in the [WHERE clause](where-clause.md) of an schema query, it requests that the query be applied to all subclasses of the class you specify.</span></span>

<span data-ttu-id="d173d-106">Например, следующая инструкция запрашивает уведомление каждые 10 минут событий изменения экземпляра для всех экземпляров, являющихся членами любого класса, производного от класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="d173d-106">For example, the following statement requests notification every 10 minutes of instance modification events for all instances that are members of any class deriving from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="d173d-107">Следующий запрос возвращает определение для класса [**\_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor) и определений для всех его подклассов.</span><span class="sxs-lookup"><span data-stu-id="d173d-107">The following query returns the definition for the [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor) class and definitions for all of its subclasses.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



<span data-ttu-id="d173d-108">**\_ Класс meta** класса определяет это как запрос схемы, свойство, именуемое, **\_ \_** определяет целевой класс запроса, а оператор ISA запрашивает определения для подклассов целевого класса.</span><span class="sxs-lookup"><span data-stu-id="d173d-108">The class **meta\_class** identifies this as a schema query, the property called **\_\_this** identifies the target class of the query, and the ISA operator requests definitions for the subclasses of the target class.</span></span>

 

 
