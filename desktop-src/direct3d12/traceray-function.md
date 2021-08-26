---
description: Отправляет луч в поиск на предмет попаданий в структуре ускорения.
ms.assetid: ''
title: Функция TraceRay
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: 4e22a26d7bd2fd91029c106133667bce98c163d90d99f0700dac7f2bdf0796fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027984"
---
# <a name="traceray-function"></a>Функция TraceRay

Отправляет луч в поиск на предмет попаданий в структуре ускорения.

## <a name="syntax"></a>Синтаксис
Это встроенное определение функции эквивалентно следующему шаблону функции:

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a>Параметры

`AccelerationStructure`

Используемая структура ускорения верхнего уровня. Указание НУЛЕВой структуры ускорения приводит к неудаче.

`RayFlags`

Допустимое сочетание значений [ray_flag](ray_flag.md) . Только определенные флаги лучей передаются системой, т. е. являются видимыми для встроенного шейдера [райфлагс](rayflags.md) .

`InstanceInclusionMask`

Целое число без знака, 8 нижних бит, которые используются для включения или отклонения экземпляров геометрических объектов на основе Инстанцемаск в каждом экземпляре. Например:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Целое число без знака, указывающее смещение, которое добавляется в вычисления адресации в таблицах шейдеров для индексирования групп попаданий.  Используются только 4 нижних бита этого значения.

`MultiplierForGeometryContributionToHitGroupIndex`

Целое число без знака, указывающее шаг для умножения на *жеометриконтрибутионтохитграупиндекс*, который является просто индексом, основанным на 0. геометрический объект был передан приложением в структуру ускорения нижнего уровня. Используются только нижние 16 бит этого значения множителя.

`MissShaderIndex`

Целое число без знака, указывающее индекс незашифрованного шейдера в таблице шейдеров.

`Ray`

Объект [**райдеск**](raydesc.md) , представляющий луча для трассировки.

`Payload`

Определяемые пользователем полезные данные луча, доступные как для ввода, так и для вывода с помощью шейдеров, которые вызываются во время райтраЦинг.  После завершения [**трацерай**](traceray-function.md) вызывающий объект может также получить доступ к полезной нагрузке.

## <a name="return-value"></a>Возвращаемое значение

**void**

## <a name="remarks"></a>Remarks

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)
* [**Шейдер создания лучей**](ray-generation-shader.md)



## <a name="see-also"></a>См. также

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




