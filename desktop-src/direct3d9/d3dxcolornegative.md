---
description: Создает отрицательное значение цвета для значения цвета.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Функция D3DXColorNegative (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c046702b81ce60f2e50817cb98c04686d9a35e964a141d88fd70dd05654e3067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069334"
---
# <a name="d3dxcolornegative-function"></a>Функция D3DXColorNegative

Создает отрицательное значение цвета для значения цвета.

## <a name="syntax"></a>Синтаксис


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
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

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является отрицательным значением цвета для значения цвета.

## <a name="remarks"></a>Remarks

Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция **D3DXColorNegative** может использоваться в качестве параметра для другой функции.

Эта функция возвращает отрицательное значение цвета, вычитая 1,0 из цветовых компонентов структуры [**D3DXCOLOR**](d3dxcolor.md) , как показано в следующем примере.


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




