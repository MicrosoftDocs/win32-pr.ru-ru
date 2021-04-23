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
# <a name="object"></a><span data-ttu-id="2226e-103">OBJECT</span><span class="sxs-lookup"><span data-stu-id="2226e-103">OBJECT</span></span>

<span data-ttu-id="2226e-104">Тип данных OBJECT — это объект класса WMI, который используется для объявления слабо типизированных взаимосвязей и внедренных объектов.</span><span class="sxs-lookup"><span data-stu-id="2226e-104">The OBJECT data type is a WMI class object use to declare weakly typed associations and embedded objects.</span></span> <span data-ttu-id="2226e-105">Не следует определять определенный класс для слабо типизированного объекта, пока не будет создан экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="2226e-105">You do not define the specific class for a weakly typed object until you create an instance of the class.</span></span> <span data-ttu-id="2226e-106">Внедренные объекты, определенные с типом данных OBJECT, могут содержать экземпляры любого класса WMI.</span><span class="sxs-lookup"><span data-stu-id="2226e-106">Embedded objects defined with the OBJECT data type can contain instances of any WMI class.</span></span> <span data-ttu-id="2226e-107">Дополнительные сведения см. в разделе [внедренные объекты](embedded-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2226e-107">For more information, see [Embedded Objects](embedded-objects.md).</span></span>

<span data-ttu-id="2226e-108">В следующем примере определяются и создаются экземпляры двух классов, один из которых содержит внедренный объект типа OBJECT:</span><span class="sxs-lookup"><span data-stu-id="2226e-108">The following example defines and creates instances of two classes, one of which contains an embedded object of type OBJECT:</span></span>

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

 

 



