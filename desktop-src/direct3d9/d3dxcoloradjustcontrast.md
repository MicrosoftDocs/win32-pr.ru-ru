---
description: Функция D3DXColorAdjustContrast (D3dx9math. h) — регулирует значение контрастности цвета.
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: Функция D3DXColorAdjustContrast (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115882"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a>Функция D3DXColorAdjustContrast (D3dx9math. h)

Корректирует значение контрастности цвета.

## <a name="syntax"></a>Синтаксис


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
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

*c* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Значение контрастности. Этот параметр линейно выполняет интерполяцию между 50% серого и цветом, ПК. Нет ограничений на значение в c. Если этот параметр равен нулю, возвращается цвет 50% серого цвета. Если этот параметр равен 1, то возвращенным цветом будет исходный цвет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом корректировки контрастности.

## <a name="remarks"></a>Remarks

Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, эта функция может использоваться в качестве параметра для другой функции.

Эта функция интерполирует компоненты красного, зеленого и синего цветов структуры [**D3DXCOLOR**](d3dxcolor.md) в диапазоне от 50% серого до указанного значения контраста, как показано в следующем примере.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Если c больше 0 и меньше 1, контрастность уменьшается. Если c больше 1, контрастность увеличивается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustSaturation**](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
