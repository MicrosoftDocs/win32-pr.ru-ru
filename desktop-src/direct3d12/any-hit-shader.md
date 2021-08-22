---
description: Шейдер, который вызывается, если пересечения лучей не являются непрозрачными.
ms.assetid: ''
title: Шейдер любых попаданий
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 127c12c6d87ca76ddac5b5c5e013414c96651e56ee762156e7435811ff275a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124389"
---
# <a name="any-hit-shader"></a>Шейдер любых попаданий

Шейдер, который вызывается, если пересечения лучей не являются непрозрачными. 

Все шейдеры попадания должны объявлять параметр полезной нагрузки, за которым следует параметр attributes. Каждый из этих параметров должен быть определяемым пользователем типом структуры, соответствующим типам, используемым для [**трацерай**](traceray-function.md) и [**репорсит**](reporthit-function.md) соответственно, или [**структурой атрибутов пересечения**](intersection-attributes.md) при использовании пересечения с нефиксированной функцией треугольника.

Любые шейдеры попадания могут выполнять следующие виды операций:

*   Чтение и изменение полезных данных луча: (InOut payload_t Райпайлоад)
*   Чтение атрибутов пересечения: (в атрибутах attr_t)
*   Вызовите метод [**акцепситандендсеарч**](accepthitandendsearch-function.md), который принимает текущее попадание, завершает [любой шейдер попадания](any-hit-shader.md), завершает [шейдер пересечения](intersection-shader.md) , если он имеется, и выполняет [ближайший построитель текстуры](closest-hit-shader.md) на ближайшее попадание, если оно активно.
*   Вызовите [**игнорехит**](ignorehit-function.md), который завершает любой шейдер попадания и сообщает системе, что будет продолжать поиск попаданий, включая возврат управления шейдеру пересечения, если он выполняется в данный момент, возвращая значение false из сайта вызова [**репорсит**](reporthit-function.md)*. 
*   Возвращает, не вызывая ни одну из этих встроенных функций, которая принимает текущее попадание и сообщает системе о необходимости продолжения поиска попаданий, включая возврат управления шейдеру пересечения, если таковой имеется, возвращая значение true на веб-сайте [**репорсит**](reporthit-function.md) Call, чтобы указать, что попадание было принято.

Даже при завершении любого вызова шейдера нажатием [**игнорехит**](ignorehit-function.md) или [**акцепситандендсеарч**](accepthitandendsearch-function.md)любые изменения, внесенные в полезные данные лучей, пока все еще должны быть сохранены.

## <a name="shader-type-attribute"></a>Атрибут типа шейдера

```
[shader("anyhit")]
```

## <a name="example"></a>Пример

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
