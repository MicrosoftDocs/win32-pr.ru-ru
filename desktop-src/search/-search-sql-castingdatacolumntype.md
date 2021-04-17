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
# <a name="casting-the-data-type-of-a-column"></a><span data-ttu-id="8b5ae-103">Приведение типа данных столбца</span><span class="sxs-lookup"><span data-stu-id="8b5ae-103">Casting the Data Type of a Column</span></span>

<span data-ttu-id="8b5ae-104">Иногда может потребоваться привести строковые данные, извлеченные из документов, в качестве другого типа данных, чтобы можно было выполнить соответствующее сравнение.</span><span class="sxs-lookup"><span data-stu-id="8b5ae-104">At times you may need to cast string data extracted from documents as another data type, so that an appropriate comparison can be made.</span></span> <span data-ttu-id="8b5ae-105">Приведите идентификатор или литерал в качестве другого типа данных, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="8b5ae-105">Cast an identifier or literal as another data type using the following syntax:</span></span>


```
CAST (<identifier> | <literal> AS <datatype>)
```



<span data-ttu-id="8b5ae-106">Пример:</span><span class="sxs-lookup"><span data-stu-id="8b5ae-106">For example:</span></span>


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a><span data-ttu-id="8b5ae-107">См. также</span><span class="sxs-lookup"><span data-stu-id="8b5ae-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b5ae-108">Сопоставления типов данных</span><span class="sxs-lookup"><span data-stu-id="8b5ae-108">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



