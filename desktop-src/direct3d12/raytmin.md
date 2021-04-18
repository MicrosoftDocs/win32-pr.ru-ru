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
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701245"
---
# <a name="raytmin"></a>райтмин

Значение типа float, представляющее текущую отправную точку параметрической для луча. 

## <a name="syntax"></a>Синтаксис

```
float RayTMin();

```

## <a name="remarks"></a>Примечания

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

 

 




