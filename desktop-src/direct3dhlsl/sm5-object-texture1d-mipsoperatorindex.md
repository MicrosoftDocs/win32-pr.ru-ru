---
title: 'Texture1D:: MIPS. Operator, функция'
description: Возвращает переменную ресурса, доступную только для чтения, или Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340230"
---
# <a name="texture1dmipsoperator----function"></a>Texture1D:: MIPS. Operator, функция

Возвращает переменную ресурса, доступную только для чтения, или [**Texture1D**](sm5-object-texture1d.md).

## <a name="syntax"></a>Синтаксис

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
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

Тип: **uint**

Позиция индекса. Содержит координату x.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса, доступная только для чтения.

## <a name="remarks"></a>Примечания

### <a name="usage-example"></a>Пример использования


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




