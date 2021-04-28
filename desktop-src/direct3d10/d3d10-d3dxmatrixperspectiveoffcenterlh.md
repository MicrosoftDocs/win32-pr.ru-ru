---
description: Функция D3DXMatrixPerspectiveOffCenterLH (D3DX10Math. h) — создает настроенную левую матрицу проекции с левой стороны.
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: Функция D3DXMatrixPerspectiveOffCenterLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1116e24b48c9090739511894d28031ca921ed6ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109052"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a>Функция D3DXMatrixPerspectiveOffCenterLH (D3DX10Math. h)

Создает настроенную левую матрицу проекции с левой стороны.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.

</dd> <dt>

*l* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальное значение x для представления объема.

</dd> <dt>

*r* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Максимальное значение x-значения для представления объема.

</dd> <dt>

*б* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальное значение y для представления объема.

</dd> <dt>

*t* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Максимальное значение y для представления объема.

</dd> <dt>

*ЗН* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальное z-значение отображаемого объема.

</dd> <dt>

*ЗФ* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Максимальное z-значение отображаемого объема.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру D3DXMATRIX, которая является настраиваемой матрицей проекции слева.

## <a name="remarks"></a>Remarks

Все параметры функции D3DXMatrixPerspectiveOffCenterLH — это расстояния в пространстве камеры. Параметры описывают размеры представления объема.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixPerspectiveOffCenterLH может использоваться в качестве параметра для другой функции.

Эта функция использует следующую формулу для вычисления возвращаемой матрицы.


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
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

 

 
