---
description: Функция D3DXVec2TransformCoordArray (D3dx9math. h) — преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: Функция D3DXVec2TransformCoordArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bf8ecfe1eeefa6e7d9af3a01d3a3e222f003b77a16e3d25f200e221c041983d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374284"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a>Функция D3DXVec2TransformCoordArray (D3dx9math. h)

Преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.

</dd> <dt>

*Шаг* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг между векторами в потоке выходных данных.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на исходный массив [**D3DXVECTOR2**](d3dxvector2.md) .

</dd> <dt>

*Встриде* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг между векторами во входном потоке данных.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .

</dd> <dt>

*n* \[ в\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число элементов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Указатель на преобразованный массив [**D3DXVECTOR4**](d3dxvector4.md) .

## <a name="remarks"></a>Remarks

Эта функция преобразует массив *ПС* (x, y, 0, 1) на матрицу *PM*, проецирование результата обратно в w = 1.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXVec2TransformCoordArray** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
