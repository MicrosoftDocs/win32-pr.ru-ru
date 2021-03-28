---
title: 'Функция Texture2DMS:: Жетсамплепоситион'
description: Возвращает расположение образца для указанного индекса.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- Функция Жетсамплепоситион HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533710"
---
# <a name="texture2dmsgetsampleposition-function"></a>Функция Texture2DMS:: Жетсамплепоситион

Возвращает расположение образца для указанного индекса.

## <a name="syntax"></a>Синтаксис

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*sampleindex* \[ окне\]
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый от нуля индекс образца расположения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **float2**

Пример расположения.

## <a name="remarks"></a>Примечания

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
