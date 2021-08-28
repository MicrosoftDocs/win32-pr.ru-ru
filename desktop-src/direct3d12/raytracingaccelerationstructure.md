---
title: RaytracingAccelerationStructure
description: Тип ресурса, который может быть объявлен в HLSL и передан в Трацерай для указания ресурса ускорения верхнего уровня, созданного с помощью БуилдрайтраЦингакцелератионструктуре.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 4728e167fe9fbc353c51accaa92d9b9d4086a0bfff3f098f43b93523cd63a792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123622"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Тип ресурса, который может быть объявлен в HLSL и передан в [**трацерай**](traceray-function.md) для указания ресурса ускорения верхнего уровня, созданного с помощью **буилдрайтраЦингакцелератионструктуре**. Он привязан как необработанный буфер SRV в таблице дескрипторов или корневом дескрипторе SRV.  Объявление в HLSL выглядит следующим образом:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

В этом примере показан массив неограниченного размера структур ускорения, который подразумевает выход из кучи дескрипторов, так как не удается индексировать корневые дескрипторы.

**РайтраЦингакцелератионструктуре** — это непрозрачный ресурс без методов, доступных для шейдеров.


 

 




