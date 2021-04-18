---
title: RaytracingAccelerationStructure
description: Тип ресурса, который может быть объявлен в HLSL и передан в Трацерай для указания ресурса ускорения верхнего уровня, созданного с помощью БуилдрайтраЦингакцелератионструктуре.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105703425"
---
# <a name="raytracingaccelerationstructure"></a><span data-ttu-id="a9830-103">RaytracingAccelerationStructure</span><span class="sxs-lookup"><span data-stu-id="a9830-103">RaytracingAccelerationStructure</span></span>

<span data-ttu-id="a9830-104">Тип ресурса, который может быть объявлен в HLSL и передан в [**трацерай**](traceray-function.md) для указания ресурса ускорения верхнего уровня, созданного с помощью **буилдрайтраЦингакцелератионструктуре**.</span><span class="sxs-lookup"><span data-stu-id="a9830-104">A resource type that can be declared in HLSL and passed into [**TraceRay**](traceray-function.md) to indicate the top-level acceleration resource built using **BuildRaytracingAccelerationStructure**.</span></span> <span data-ttu-id="a9830-105">Он привязан как необработанный буфер SRV в таблице дескрипторов или корневом дескрипторе SRV.</span><span class="sxs-lookup"><span data-stu-id="a9830-105">It is bound as a raw buffer SRV in a descriptor table or root descriptor SRV.</span></span>  <span data-ttu-id="a9830-106">Объявление в HLSL выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a9830-106">The declaration in HLSL is as follows:</span></span>


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

<span data-ttu-id="a9830-107">В этом примере показан массив неограниченного размера структур ускорения, который подразумевает выход из кучи дескрипторов, так как не удается индексировать корневые дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="a9830-107">This example shows an unbounded size array of acceleration structures, which implies coming from a descriptor heap since root descriptors can’t be indexed.</span></span>

<span data-ttu-id="a9830-108">**РайтраЦингакцелератионструктуре** — это непрозрачный ресурс без методов, доступных для шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a9830-108">**RaytracingAccelerationStructure** is an opaque resource with no methods available to shaders.</span></span>


 

 




