---
title: 'Texture2DArray:: MIPS. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture2DArray:: MIPS. Operator, функция'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
keywords:
- MIPS. Оператор Function HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820789"
---
# <a name="texture2darraymipsoperator----function"></a>Texture2DArray:: MIPS. Operator, функция

Возвращает переменную ресурса, доступную только для чтения.

## <a name="syntax"></a>Синтаксис

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*мипслице* \[ окне\]
</dt> <dd>

Тип: **uint**

Индекс среза MIP.

</dd> <dt>

*POS-терминал* \[ окне\]
</dt> <dd>

Тип: **uint3**

Позиция индекса. Первый и второй компоненты содержат координаты (x, y). Третий компонент указывает нужный срез массива.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса, доступная только для чтения.

## <a name="remarks"></a>Примечания

### <a name="usage-example"></a>Пример использования


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




