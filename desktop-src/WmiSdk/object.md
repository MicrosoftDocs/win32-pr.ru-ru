---
description: Тип данных OBJECT — это объект класса WMI, который используется для объявления слабо типизированных взаимосвязей и внедренных объектов.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c26b8b6ff77f788aeed607057541d19d80fea4c105b53d492c1f1e8468b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554934"
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

 

 



