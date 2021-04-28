---
description: Функция D3DXMatrixTransformation2D (D3DX10Math. h) — строит матрицу 2D-преобразования, представляющую преобразования в плоскости XY. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Функция D3DXMatrixTransformation2D (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ef112c346fd222f5e25935740e47ab62273628f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103362"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>Функция D3DXMatrixTransformation2D (D3DX10Math. h)

Формирует матрицу 2D-преобразования, представляющую преобразования в плоскости XY. Аргументы **null** обрабатываются как преобразования Identity.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
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

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , содержащую результат преобразований.

</dd> <dt>

*пскалингцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md), указывающий центр масштабирования. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица Identity M <sub>SC</sub> .

</dd> <dt>

*Скалингротатион* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Указатель на коэффициент поворота масштабирования.

</dd> <dt>

*пскалинг* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на структуру D3DXVECTOR2 — точку, определяющую масштаб. Если этот аргумент имеет **значение NULL**, к формуле в примечаниях применяется удостоверение MS Matrix.

</dd> <dt>

*протатионцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на структуру D3DXVECTOR2 — точку, определяющую центр вращения. Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.

</dd> <dt>

*Вращение* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Угол поворота в радианах.

</dd> <dt>

*птранслатион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на структуру D3DXVECTOR2, идентифицирующую перевод. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру D3DXMATRIX, содержащую матрицу преобразования.

## <a name="remarks"></a>Remarks

Эта функция вычисляет матрицу преобразования с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* M<sub>SR</sub> \* M<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

где:

M<sub>out</sub> = выходная матрица (Тоска)

M<sub>SC</sub> = матрица центра масштабирования (пскалингцентер)

M<sub>SR</sub> = матрица вращения масштабирования (пскалингротатион)

Матрица MS = масштабирования (Пскалинг)

M<sub>RC</sub> = центр матрицы вращения (протатионцентер)

M<sub>r</sub> = матрица вращения (вращение)

MT = матрица перевода (Птранслатион)

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixTransformation2D может использоваться в качестве параметра для другой функции.

Для трехмерных преобразований используйте [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
