---
description: Строит матрицу двумерных преобразований в плоскости x-y. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: Функция D3DXMatrixAffineTransformation2D (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 40666e4fc74f834d6333259636f9953281d534570eedabf37a3d99590ec2e1ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070164"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a>Функция D3DXMatrixAffineTransformation2D (D3DX10Math. h)

Строит матрицу двумерных преобразований в плоскости x-y. Аргументы **null** обрабатываются как преобразования Identity.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , который является результатом операции.

</dd> <dt>

*Масштабирование* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент масштабирования.

</dd> <dt>

*протатионцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md), указывающий центр вращения. Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.

</dd> <dt>

*Вращение* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Угол поворота.

</dd> <dt>

*птранслатион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md), представляющий перевод. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру D3DXMATRIX, которая является матрицей аффинного преобразования.

## <a name="remarks"></a>Remarks

Эта функция вычисляет матрицу аффинных преобразований с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:

M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT

где:

M<sub>out</sub> = выходная матрица (Тоска)

MS = матрица масштабирования (масштабирование)

M<sub>RC</sub> = центр матрицы вращения (протатионцентер)

M<sub>r</sub> = матрица вращения (вращение)

MT = матрица перевода (Птранслатион)

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixAffineTransformation2D может использоваться в качестве параметра для другой функции.

Для трехмерных преобразований используйте D3DXMatrixAffineTransformation.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
