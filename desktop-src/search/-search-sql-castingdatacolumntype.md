---
description: 'Дополнительные сведения: приведение типа данных столбца'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Приведение типа данных столбца
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710911"
---
# <a name="casting-the-data-type-of-a-column"></a>Приведение типа данных столбца

Иногда может потребоваться привести строковые данные, извлеченные из документов, в качестве другого типа данных, чтобы можно было выполнить соответствующее сравнение. Приведите идентификатор или литерал в качестве другого типа данных, используя следующий синтаксис:


```
CAST (<identifier> | <literal> AS <datatype>)
```



Пример:


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Сопоставления типов данных](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



