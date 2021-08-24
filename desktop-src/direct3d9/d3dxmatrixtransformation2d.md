---
description: Функция D3DXMatrixTransformation2D (D3dx9math. h) — строит матрицу 2D-преобразования, представляющую преобразования в плоскости XY. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Функция D3DXMatrixTransformation2D (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 754ea3124f5c2433e459331d4ebc7727a9c2519a982d1def09c7e16e794e6ae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750104"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>Функция D3DXMatrixTransformation2D (D3dx9math. h)

Формирует матрицу 2D-преобразования, представляющую преобразования в плоскости XY. Аргументы **null** обрабатываются как преобразования Identity.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , содержащую результат преобразований.

</dd> <dt>

*пскалингцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) — точку, определяющую центр масштабирования. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица Identity M <sub>SC</sub> .

</dd> <dt>

*пскалингротатион* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент поворота масштабирования.

</dd> <dt>

*пскалинг* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) — точку, определяющую масштаб. Если этот аргумент имеет **значение NULL**, к формуле в примечаниях применяется удостоверение MS Matrix.

</dd> <dt>

*протатионцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) — точку, определяющую центр вращения. Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.

</dd> <dt>

*Вращение* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Угол поворота в радианах.

</dd> <dt>

*птранслатион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , идентифицирующую перевод. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , содержащую матрицу преобразования.

## <a name="remarks"></a>Remarks

Эта функция вычисляет матрицу преобразования с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* M<sub>SR</sub> \* M<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

где:

M <sub>out</sub> = выходная матрица (*тоска*)

M <sub>SC</sub> = матрица центра масштабирования (*пскалингцентер*)

M <sub>SR</sub> = матрица вращения масштабирования (*пскалингротатион*)

Матрица MS = масштабирования (*пскалинг*)

M <sub>RC</sub> = центр матрицы вращения (*протатионцентер*)

M <sub>r</sub> = матрица вращения (*вращение*)

MT = матрица перевода (*птранслатион*)

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция **D3DXMatrixTransformation2D** может использоваться в качестве параметра для другой функции.

Для трехмерных преобразований используйте [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Преобразования (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
