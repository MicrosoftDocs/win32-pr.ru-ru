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
ms.openlocfilehash: 1b40987c76f42d41d74b7cb3d41f35cc20bd5a6ac1414ae9b010cedcfa7ef9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124170"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Возвращает текущее расположение в пределах ширины, высоты и глубины, полученное с помощью встроенного системного значения [**диспатчрайсдименсионс**](dispatchraysdimensions.md) .

## <a name="syntax"></a>Синтаксис

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Remarks

Эту функцию можно вызвать из следующих типов шейдеров райтраЦинг.

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Вызываемый шейдер**](callable-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)
* [**Шейдер создания лучей**](ray-generation-shader.md)

## <a name="see-also"></a>См. также раздел

* [Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
