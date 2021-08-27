---
description: Функция D3DXPlaneIntersectLine (D3dx9math. h) — Находит пересечение между плоскостью и линией.
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: Функция D3DXPlaneIntersectLine (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1b6f3067b25561869f61c70792ed2a242404deca4d65f07d83e331f6f4414d8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096131"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a>Функция D3DXPlaneIntersectLine (D3dx9math. h)

Находит пересечение между плоскостью и линией.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую пересечение между указанной плоскостью и линией.

</dd> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](d3dxplane.md) \***

Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую начальную точку строки.

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую конечную точку строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является пересечением между указанной плоскостью и линией.

## <a name="remarks"></a>Remarks

Если линия параллельна плоскости, возвращается **значение NULL** .

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXPlaneIntersectLine** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




