---
description: Тип данных OBJECT — это объект класса WMI, который используется для объявления слабо типизированных взаимосвязей и внедренных объектов.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808285"
---
# <a name="object"></a>OBJECT

Тип данных OBJECT — это объект класса WMI, который используется для объявления слабо типизированных взаимосвязей и внедренных объектов. Не следует определять определенный класс для слабо типизированного объекта, пока не будет создан экземпляр класса. Внедренные объекты, определенные с типом данных OBJECT, могут содержать экземпляры любого класса WMI. Дополнительные сведения см. в разделе [внедренные объекты](embedded-objects.md).

В следующем примере определяются и создаются экземпляры двух классов, один из которых содержит внедренный объект типа OBJECT:

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

class CompositeClass
{
    [key] string aKey;   
    object EmbObj;       // Weakly typed
};

class EmbClass

{
  [key] string aKey;
};

instance of CompositeClass
{
    aKey = "CompositeClass Key";
    EmbObj = 
        instance of EmbClass
        {
           aKey = "key for embedded object";
        };
};
```

 

 



