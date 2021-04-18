---
description: Создает настроенную левую матрицу проекции с левой стороны.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: Функция D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713477"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a>Функция D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)

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

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.

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

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является настраиваемой матрицей проекции слева.

## <a name="remarks"></a>Комментарии

Все параметры функции **D3DXMatrixPerspectiveOffCenterLH** — это расстояния в пространстве камеры. Параметры описывают размеры представления объема.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXMatrixPerspectiveOffCenterLH** может использоваться в качестве параметра для другой функции.

Эта функция использует следующую формулу для вычисления возвращаемой матрицы.


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
