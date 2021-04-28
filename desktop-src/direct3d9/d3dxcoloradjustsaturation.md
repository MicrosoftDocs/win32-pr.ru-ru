---
description: Функция D3DXColorAdjustSaturation (D3dx9math. h) — регулирует значение насыщенности цвета.
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: Функция D3DXColorAdjustSaturation (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115872"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a>Функция D3DXColorAdjustSaturation (D3dx9math. h)

Регулирует значение насыщенности цвета.

## <a name="syntax"></a>Синтаксис


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.

</dd> <dt>

*ПК* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .

</dd> <dt>

*s* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Значение насыщенности. Этот параметр линейно выполняет интерполяцию цвета, преобразованного в градации серого, и исходного цвета, ПК. Ограничения на значение s отсутствуют. Если параметр s имеет значение 0, то возвращается цвет оттенков серого. Если параметр s имеет значение 1, возвращается исходный цвет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом корректировки насыщенности.

## <a name="remarks"></a>Remarks

Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, эта функция может использоваться в качестве параметра для другой функции.

Эта функция интерполирует компоненты красного, зеленого и синего цветов структуры [**D3DXCOLOR**](d3dxcolor.md) между ненасыщенным цветом и цветом, как показано в следующем примере.


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



Если параметр s больше 0 и меньше 1, насыщенность уменьшается. Если параметр s больше 1, увеличивается насыщенность.

Цвет оттенков серого вычисляются следующим образом:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustContrast**](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
