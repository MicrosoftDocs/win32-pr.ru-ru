---
description: Регулирует значение насыщенности цвета.
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: Функция D3DXColorAdjustSaturation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6cfa4dd2af6e4a4ac3772af80ba11b8189405f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000464"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>Функция D3DXColorAdjustSaturation (D3DX10Math. h)

Регулирует значение насыщенности цвета.

## <a name="syntax"></a>Синтаксис


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Указатель на [**D3DXCOLOR**](d3d10-d3dxcolor.md) , который является результатом операции.

</dd> <dt>

*ПК* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Указатель на исходную структуру D3DXCOLOR.

</dd> <dt>

*s* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Значение насыщенности. Этот параметр линейно выполняет интерполяцию цвета, преобразованного в градации серого, и исходного цвета, ПК. Ограничения на значение s отсутствуют. Если параметр s имеет значение 0, то возвращается цвет оттенков серого. Если параметр s имеет значение 1, возвращается исходный цвет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Эта функция возвращает указатель на структуру D3DXCOLOR, которая является результатом корректировки насыщенности.

## <a name="remarks"></a>Комментарии

Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, эта функция может использоваться в качестве параметра для другой функции.

Эта функция интерполирует компоненты красного, зеленого и синего цветов структуры D3DXCOLOR между ненасыщенным цветом и цветом, как показано в следующем примере.


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



Если параметр s больше 0 и меньше 1, насыщенность уменьшается. Если параметр s больше 1, увеличивается насыщенность.

Цвет оттенков серого вычисляются следующим образом:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
