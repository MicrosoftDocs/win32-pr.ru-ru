---
description: WorldToObject3x4 — матрица для преобразования из мирового пространства в объектно-пространство.
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: 5818e579076dc94a5d42003aa0af93f012e779a69e4ca78988e5c62b518a2d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631754"
---
# <a name="worldtoobject3x4"></a>WorldToObject3x4

Матрица для преобразования из мирового пространства в объектно-пространство. Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.

## <a name="syntax"></a>Синтаксис

```
void WorldToObject3x4();

```




## <a name="remarks"></a>Remarks

Матрица является транспоситион матрицы **WorldToObject4x3** .

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)





## <a name="see-also"></a>См. также

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




