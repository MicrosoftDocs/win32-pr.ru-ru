---
description: Функция D3DXMatrixOrthoOffCenterRH (D3dx9math. h) — создает настраиваемую, правую, расположенную справа матрицу проекции.
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Функция D3DXMatrixOrthoOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8519dca07a4475ff043491802ae173ecc61c0bd3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107462"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a>Функция D3DXMatrixOrthoOffCenterRH (D3dx9math. h)

Создает настроенную правую матрицу ортогональной проекции.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
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

Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).

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

Минимальное значение y для параметра "Показать том".

</dd> <dt>

*t* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Максимальное значение y для параметра "Показать том".

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

Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).

## <a name="remarks"></a>Remarks

Функция [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) является особым случаем функции **D3DXMatrixOrthoOffCenterRH** . Чтобы создать ту же проекцию с помощью **D3DXMatrixOrthoOffCenterRH**, используйте следующие значения: l =-w/2, r = w/2, b =-h/2 и t = h/2.

Все параметры функции **D3DXMatrixOrthoOffCenterRH** — это расстояния в пространстве камеры. Параметры описывают размеры представления объема.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXMatrixOrthoOffCenterRH** может использоваться в качестве параметра для другой функции.

Эта функция использует следующую формулу для вычисления возвращаемой матрицы.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md)
</dt> <dt>

[**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterLH**](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
