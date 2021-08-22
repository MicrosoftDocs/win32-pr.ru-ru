---
title: 'Texture2DMSArray:: Sample. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture2DMSArray:: Sample. Operator, функция'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: 09ac18e7830dfe6b18718deed56e8495ba476dcedcb8290eab4e16aa0d7f24fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508329"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray:: Sample. Operator, функция

Возвращает переменную ресурса, доступную только для чтения.

## <a name="syntax"></a>Синтаксис

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
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

Тип: **uint3**

Позиция индекса. Первый и второй компоненты содержат координаты (x, y). Третий компонент указывает нужный срез массива.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса, доступная только для чтения.

## <a name="remarks"></a>Remarks

### <a name="usage-example"></a>Пример использования


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




