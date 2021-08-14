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
ms.openlocfilehash: 9da6727120dcb19d9dd51c83d62f85d842036edb2197d33e298259480b248642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508420"
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

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
