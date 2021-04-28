---
description: ObjectToWorld3x4 — матрица для преобразования из объектного пространства в мировое пространство.
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107742"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Матрица для преобразования из объектного пространства в мировое пространство. Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.

## <a name="syntax"></a>Синтаксис

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Remarks

Матрица является транспоситион матрицы **ObjectToWorld4x3** .

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)





## <a name="see-also"></a>См. также

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




