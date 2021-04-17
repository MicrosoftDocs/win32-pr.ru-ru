---
description: Возвращает текущее расположение в пределах ширины, высоты и глубины, полученное с помощью встроенного системного значения [**диспатчрайсдименсионс**](dispatchraysdimensions.md) .
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "105691706"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Возвращает текущее расположение в пределах ширины, высоты и глубины, полученное с помощью встроенного системного значения [**диспатчрайсдименсионс**](dispatchraysdimensions.md) .

## <a name="syntax"></a>Синтаксис

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Примечания

Эту функцию можно вызвать из следующих типов шейдеров райтраЦинг.

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Вызываемый шейдер**](callable-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)
* [**Шейдер создания лучей**](ray-generation-shader.md)

## <a name="see-also"></a>См. также раздел

* [Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
