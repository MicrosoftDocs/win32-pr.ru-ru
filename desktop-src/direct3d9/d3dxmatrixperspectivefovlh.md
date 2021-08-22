---
description: Функция D3DXMatrixPerspectiveFovLH (D3dx9math. h) — формирует матрицу левой проекции перспективы на основе поля представления.
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Функция D3DXMatrixPerspectiveFovLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc530d4e0d977bac7df89f040d63552a4f0ca852c4e04ba0724f408daef10829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122894"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a>Функция D3DXMatrixPerspectiveFovLH (D3dx9math. h)

Строит левовинтовую матрицу перспективной проекции на основании поля зрения.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
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

*ФОВИ* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Поле представления в направлении y (в радианах).

</dd> <dt>

*Аспект* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Пропорции, определенные как ширина представления, деленная на высоту.

</dd> <dt>

*ЗН* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Z-значение ближней плоскости просмотра.

</dd> <dt>

*ЗФ* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Z-значение дальней плоскости просмотра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей перспективной проекции влево.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXMatrixPerspectiveFovLH** может использоваться в качестве параметра для другой функции.

Чтобы изменить ось пропорций, используйте формулу вычисления: ФОВИ = 2 * Math. ATAN (Math. Tan (ФОВИ * 0,5)/аспект). Кроме того, добавьте в структуру переменные пропорций X и Y, чтобы масштабировать вертикальное пространство представления: ФОВИ = 2 * Math. ATAN (Math. Tan (ФОВИ * 0,5)/пропорции), аспект = Аспекткс * аспект Y.

Эта функция вычислит возвращаемую матрицу, как показано ниже.


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
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

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
