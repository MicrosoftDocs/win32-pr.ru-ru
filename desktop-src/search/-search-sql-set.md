---
description: Инструкция SET задает значения PROPERTYNAME и РАНКМЕСОД для запроса.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Инструкция SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144071"
---
# <a name="set-statement"></a>Инструкция SET

Инструкция SET задает значения PROPERTYNAME и РАНКМЕСОД для запроса.

## <a name="propertyname"></a>PROPERTYNAME

Можно связать свойство с понятным псевдонимом для запроса, используя следующий синтаксис:


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a>ранкмесод

Можно указать метод ранжирования для запросов с термином «ABOUT», используя следующий синтаксис:


```
SET RANKMETHOD <rankmethod>      
```



Методы РАНКМЕСОД, которые могут быть заданы с помощью инструкции SET: ДЖАККАРДА коэффициент, коэффициент КОСТей и внутренний продукт.

 

 



