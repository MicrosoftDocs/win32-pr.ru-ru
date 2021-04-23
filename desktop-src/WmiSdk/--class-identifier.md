---
description: Хорошо известный \_ \_ класс идентификатора относится к псевдо-свойству для каждого объекта WMI, который указывает класс текущего объекта.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: Идентификатор __CLASS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b4db6cacb6943619cf6468cf7f03d4a4c08278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156622"
---
# <a name="__class-identifier"></a><span data-ttu-id="fbbf7-103">\_\_Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="fbbf7-103">\_\_CLASS Identifier</span></span>

<span data-ttu-id="fbbf7-104">Хорошо известный \_ \_ класс идентификатора относится к псевдо-свойству для каждого объекта WMI, который указывает класс текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="fbbf7-104">The well-known identifier \_\_CLASS refers to a pseudo-property on every WMI object that indicates the class of the current object.</span></span>

<span data-ttu-id="fbbf7-105">Используйте \_ \_ класс в предложении [WHERE](where-clause.md) , чтобы отфильтровать все объекты производных классов из результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="fbbf7-105">Use \_\_CLASS in a [WHERE](where-clause.md) clause to filter out any objects of derived classes from your result set.</span></span> <span data-ttu-id="fbbf7-106">Например, результирующий набор следующего запроса содержит не только объекты, класс которых является [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), но также объекты, класс которых является производным от **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="fbbf7-106">For example, the result set of the following query contains not only objects whose class is [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), but also objects whose class is derived from **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk
```



<span data-ttu-id="fbbf7-107">В следующем примере использование \_ \_ класса в предложении **WHERE** отфильтровывает все объекты классов, производных от [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , поскольку их класс не является **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="fbbf7-107">In the following example, the use of \_\_CLASS in the **WHERE** clause filters out all objects of classes derived from [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) because their class is not **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



<span data-ttu-id="fbbf7-108">Используйте \_ \_ класс в поставщиках, которые запросят предоставить экземпляры определенного класса независимо от любых подклассов.</span><span class="sxs-lookup"><span data-stu-id="fbbf7-108">Use \_\_CLASS in providers that are asked to provide instances of a specific class, irrespective of any subclasses.</span></span>

 

 
