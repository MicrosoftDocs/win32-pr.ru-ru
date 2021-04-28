---
description: Функция D3DXVec2Normalize (D3DX10Math. h) — Возвращает нормализованную версию 2D-вектора.
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: Функция D3DXVec2Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaa7bde759b9023b69204d6cb39259f0905b9928
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108392"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a>Функция D3DXVec2Normalize (D3DX10Math. h)

Возвращает нормализованную версию 2D-вектора.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на исходную структуру D3DXVECTOR2.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Указатель на структуру D3DXVECTOR2, которая является нормализованной версией вектора.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXVec2Normalize может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
