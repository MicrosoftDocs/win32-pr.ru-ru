---
title: 'Функция Texture2DMSArray:: Жетсамплепоситион'
description: 'Возвращает расположение указанного образца. | Функция Texture2DMSArray:: Жетсамплепоситион'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273644"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Функция Texture2DMSArray:: Жетсамплепоситион

Возвращает расположение указанного образца.

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

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
