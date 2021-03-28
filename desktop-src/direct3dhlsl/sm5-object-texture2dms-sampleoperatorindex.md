---
title: 'Texture2DMS:: Sample. Operator, функция'
description: 'Извлекает значение из ресурса в расположении и указанном индексе выборки. | Texture2DMS:: Sample. Operator, функция'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- Следующий. Оператор Function HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273645"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS:: Sample. Operator, функция

Извлекает значение из ресурса в расположении и указанном индексе выборки.

## <a name="syntax"></a>Синтаксис

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*самплеслице* \[ окне\]
</dt> <dd>

Тип: **uint**

Пример индекса среза.

</dd> <dt>

*POS-терминал* \[ окне\]
</dt> <dd>

Тип: **uint2**

Позиция индекса. Компоненты содержат координаты (x, y).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса, доступная только для чтения.

## <a name="remarks"></a>Примечания

### <a name="usage-example"></a>Пример использования


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



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

 

 




