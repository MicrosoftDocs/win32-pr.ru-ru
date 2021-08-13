---
description: Вызывается шейдером пересечения для сообщения пересечения лучей.
ms.assetid: ''
title: Функция ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 8714cabc02f70ca12bcc78493de3a61482ba5aed5490087d309f6ec091cecf75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528112"
---
# <a name="reporthit-function"></a>Функция ReportHit

Вызывается [шейдером пересечения](intersection-shader.md) для сообщения пересечения лучей.

## <a name="syntax"></a>Синтаксис
Это встроенное определение функции эквивалентно следующему шаблону функции:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Параметры

`THit`

Значение с плавающей запятой, задающее параметр параметрической расстояния пересечения.

`HitKind`

Целое число без знака, определяющее тип произошедших попаданий.  Это заданное пользователем значение в диапазоне 0-127.  Значение может быть считано [любыми](any-hit-shader.md) [ближайшими шейдерами попадания](closest-hit-shader.md) с встроенной функцией **хиткинд** .

`Attributes`

Определяемая пользователем структура [**структуры атрибута пересечения**](intersection-attributes.md) , указывающая атрибуты пересечения.  

## <a name="return-value"></a>Возвращаемое значение

**bool (логическое** ) Значение true, если попадание было принято.  Попадание отклоняется, если *сит* находится за пределами текущего интервала лучей или любой шейдер попадания вызывает [**игнорехит**](ignorehit-function.md).  Текущий интервал лучей определяется **райтмин** и **райткуррент**.

## <a name="remarks"></a>Remarks

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер пересечения**](intersection-shader.md)





## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




