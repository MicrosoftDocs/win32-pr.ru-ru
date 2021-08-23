---
description: ObjectToWorld4x3 — матрица для преобразования из объектного пространства в мировое пространство.
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 22ad7bfafae89e33001d1d72878bc268ebfbd44649176b118a447fa16cf97d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608274"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Матрица для преобразования из объектного пространства в мировое пространство. Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.

## <a name="syntax"></a>Синтаксис

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Remarks

Матрица является транспоситион матрицы **ObjectToWorld3x4** .

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)





## <a name="see-also"></a>См. также

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




