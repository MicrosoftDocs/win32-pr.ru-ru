---
description: Использует линейную интерполяцию для создания значения цвета.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Функция D3DXColorLerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914744"
---
# <a name="d3dxcolorlerp-function"></a>Функция D3DXColorLerp

Использует линейную интерполяцию для создания значения цвета.

## <a name="syntax"></a>Синтаксис


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
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

*pC1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .

</dd> <dt>

*pC2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .

</dd> <dt>

*s* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Параметр, который линейно выполняет интерполяцию между цветами, pC1 и pC2, рассматривая их как векторы 4D. Ограничения на значение s отсутствуют.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом линейной интерполяции.

## <a name="remarks"></a>Комментарии

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция **D3DXColorLerp** может использоваться в качестве параметра для другой функции.

Эта функция выполняет интерполяцию красного, зеленого, синего и альфа-компонентов структуры [**D3DXCOLOR**](d3dxcolor.md) между двумя цветами, как показано в следующем примере.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Если линейная интерполяция между цветами A и B и s равна 0, то результирующим цветом будет. Если параметр s имеет значение 1, то полученный цвет будет иметь цвет B.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
