---
description: Шейдер, который вызывает Трацерай для создания лучей.
ms.assetid: ''
title: Шейдер создания лучей
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701289"
---
# <a name="ray-generation-shader"></a>Шейдер создания лучей

Шейдер, который вызывает [**трацерай**](traceray-function.md) для создания лучей. Начальные пользовательские полезные данные лучей для каждого луча предоставляются на сайт вызова **трацерай** .  [**Каллшадер**](callshader-function.md) также можно использовать в шейдерах создания лучей для вызова [вызываемых шейдеров](callable-shader.md).

**Диспатчрайс** вызывает сетку вызовов шейдера создания лучей.  Каждый вызов (поток) шейдера создания лучей знает его расположение в общей сетке, может создавать произвольные лучи через [**трацерай**](traceray-function.md)и работать независимо от других вызовов. Не существует определенного порядка выполнения потоков по отношению друг к другу.

## <a name="shader-type-attribute"></a>Атрибут типа шейдера


```
[shader("raygeneration")]
```



## <a name="example"></a>Пример

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




