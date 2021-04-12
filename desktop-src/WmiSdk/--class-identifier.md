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
# <a name="__class-identifier"></a>\_\_Идентификатор класса

Хорошо известный \_ \_ класс идентификатора относится к псевдо-свойству для каждого объекта WMI, который указывает класс текущего объекта.

Используйте \_ \_ класс в предложении [WHERE](where-clause.md) , чтобы отфильтровать все объекты производных классов из результирующего набора. Например, результирующий набор следующего запроса содержит не только объекты, класс которых является [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), но также объекты, класс которых является производным от **Win32 \_ LogicalDisk**.


```sql
SELECT * FROM Win32_LogicalDisk
```



В следующем примере использование \_ \_ класса в предложении **WHERE** отфильтровывает все объекты классов, производных от [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , поскольку их класс не является **Win32 \_ LogicalDisk**.


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Используйте \_ \_ класс в поставщиках, которые запросят предоставить экземпляры определенного класса независимо от любых подклассов.

 

 
