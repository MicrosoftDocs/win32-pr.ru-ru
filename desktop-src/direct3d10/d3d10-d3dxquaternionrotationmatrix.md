---
description: Функция D3DXQuaternionRotationMatrix (D3DX10Math. h) — создает кватернион на основе матрицы вращения.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Функция D3DXQuaternionRotationMatrix (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cb923c135d436b36fe032d344366fdee687d27a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103152"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a>Функция D3DXQuaternionRotationMatrix (D3DX10Math. h)

Создает кватернион на основе матрицы вращения.

## <a name="syntax"></a>Синтаксис


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на структуру D3DXQUATERNION, построенную из матрицы вращения.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXQuaternionRotationMatrix может использоваться в качестве параметра для другой функции.

Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
