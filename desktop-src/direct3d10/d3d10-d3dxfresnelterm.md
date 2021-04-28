---
description: Функция D3DXFresnelTerm (D3DX10Math. h) — вычисляет термин Френелю.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Функция D3DXFresnelTerm (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9efa557d44451674d2ae4c48a58370e939760a03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113272"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>Функция D3DXFresnelTerm (D3DX10Math. h)

Вычислите термин Френелю.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Коссета* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Оно должно находиться в диапазоне от 0 до 1.

</dd> <dt>

*Рефрактиониндекс* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Индекс передробки материала. Значение должно быть больше 1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Эта функция возвращает термин Френелю для неполярного источника. Коссета — это косинус угла инцидента.

## <a name="remarks"></a>Remarks

Чтобы найти термин Френелю (F), сделайте следующее:

Если значение равно «Angle», а «B» — угол дроби, то


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Затем, развернув с помощью тригонометрических удостоверений и упростите, вы получаете:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
