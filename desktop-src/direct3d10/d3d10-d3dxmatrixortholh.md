---
description: Функция D3DXMatrixOrthoLH (D3DX10Math. h) — строит матрицу левой ортогональной проекции.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Функция D3DXMatrixOrthoLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b8b1b64818f4c0903897dc5b1de83b1aaa963461e909edbbfc9ba8dc4a1f10f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282964"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a>Функция D3DXMatrixOrthoLH (D3DX10Math. h)

Формирует матрицу левой ортогональной проекции.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).

</dd> <dt>

*w* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Ширина объема представления.

</dd> <dt>

*ч* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Высота представления объема.

</dd> <dt>

*ЗН* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальное z-значение отображаемого тома, называемое z-NEAR.

</dd> <dt>

*ЗФ* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Максимальное z-значение объема представления, которое называется z-далеко.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).

## <a name="remarks"></a>Remarks

Все параметры функции D3DXMatrixOrthoLH — это расстояния в пространстве камеры. Параметры описывают размеры представления объема.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixOrthoLH может использоваться в качестве параметра для другой функции.

Эта функция использует следующую формулу для вычисления возвращаемой матрицы.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
