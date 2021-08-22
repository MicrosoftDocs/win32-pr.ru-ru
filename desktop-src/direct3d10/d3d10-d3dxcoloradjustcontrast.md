---
description: Функция D3DXColorAdjustContrast (D3DX10Math. h) — регулирует значение контрастности цвета.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: Функция D3DXColorAdjustContrast (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 90c36ee9c414b6ae34058b255ad2e7a642f13ef49ee91b586ca974009d4e6b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498494"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a>Функция D3DXColorAdjustContrast (D3DX10Math. h)

Корректирует значение контрастности цвета.

## <a name="syntax"></a>Синтаксис


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

\[в указатель out \] на [**D3DXCOLOR**](d3d10-d3dxcolor.md) , который является результатом операции.

</dd> <dt>

*ПК* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Указатель на исходную структуру D3DXCOLOR.

</dd> <dt>

*c* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Значение контрастности. Этот параметр линейно выполняет интерполяцию между 50% серого и цветом, ПК. Нет ограничений на значение в. Если этот параметр равен нулю, возвращается цвет 50% серого цвета. Если этот параметр равен 1, то возвращенным цветом будет исходный цвет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Эта функция возвращает указатель на структуру D3DXCOLOR, которая является результатом корректировки контрастности.

## <a name="remarks"></a>Remarks

Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, эта функция может использоваться в качестве параметра для другой функции.

Эта функция интерполирует компоненты красного, зеленого и синего цветов структуры D3DXCOLOR в диапазоне от 50% серого до указанного значения контраста, как показано в следующем примере.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Если c больше 0 и меньше 1, контрастность уменьшается. Если c больше 1, контрастность увеличивается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
