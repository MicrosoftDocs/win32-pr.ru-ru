---
description: Преобразует двумерный вектор по заданной матрице, проецирование результата обратно в w = 1.
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Функция D3DXVec2TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0d7e93c2b3a78160f2f1f1ad3342575b4369a057
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703913"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a>Функция D3DXVec2TransformCoord (D3DX10Math. h)

Преобразует двумерный вектор по заданной матрице, проецирование результата обратно в w = 1.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
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

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Указатель на структуру D3DXVECTOR2, которая является преобразованным вектором.

## <a name="remarks"></a>Комментарии

Эта функция преобразует вектор, НЗ (x, y, 0, 1), по матрице, в проекцию результата обратно в w = 1.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXVec2TransformCoord может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
