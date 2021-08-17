---
title: 'Texture3D:: MIPS. Operator, функция'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Texture3D:: MIPS. Operator, функция'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: 18ad563041c8ad0b601240f4353dad5bbc44ef418c267f72d07f0f753d12d993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724504"
---
# <a name="texture3dmipsoperator----function"></a>Texture3D:: MIPS. Operator, функция

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

Позиция индекса. Содержит координаты (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса, доступная только для чтения.

## <a name="remarks"></a>Remarks

### <a name="usage-example"></a>Пример использования


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




