---
description: Значение типа float, представляющее текущую отправную точку параметрической для луча.
ms.assetid: ''
title: райтмин
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 5429574480cfda071dfec93cea771211bab578bdaecb4513c76f43c4d820b22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989484"
---
# <a name="raytmin"></a>райтмин

Значение типа float, представляющее текущую отправную точку параметрической для луча. 

## <a name="syntax"></a>Синтаксис

```
float RayTMin();

```

## <a name="remarks"></a>Remarks

**Райтмин** определяет начальную точку луча в соответствии со следующей формулой: источник + (направление * райтмин).  *Источник* и *направление* могут находиться в любом мире или объектном пространстве, что приводит к отправной точке мира или объектного пространства.

**Райтмин** указывается в вызове [**трацерай**](traceray-function.md)и является константой в течение этого вызова.




Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)





## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




