---
description: Возвращает значение, передаваемое в качестве параметра Хиткинд в Репорсит.
ms.assetid: ''
title: хиткинд
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647145"
---
# <a name="hitkind"></a>хиткинд

Возвращает значение, передаваемое в качестве параметра **хиткинд** в [**репорсит**](reporthit-function.md).

## <a name="syntax"></a>Синтаксис

```
uint HitKind();

```



## <a name="remarks"></a>Примечания

Если пересечение было сообщено пересечением треугольника с фиксированной функцией, **хиткинд** будет одной из сторон, **\_ \_ \_ лицевой \_ стороной** треугольника (254) или координатами **типа курсора \_ \_ \_ \_** (255).

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)





## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




