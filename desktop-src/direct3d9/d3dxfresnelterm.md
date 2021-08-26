---
description: Функция D3DXFresnelTerm (D3dx9math. h) — вычисляет термин Френелю.
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: Функция D3DXFresnelTerm (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15f0c5bac66d0c1b43bf3938e4ecb1f2fffd8dd235532b5dddc27eb5923ef5f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027654"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>Функция D3DXFresnelTerm (D3dx9math. h)

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
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
