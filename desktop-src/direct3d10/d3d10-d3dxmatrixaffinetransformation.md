---
description: Формирует матрицу трехмерного преобразования. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Функция D3DXMatrixAffineTransformation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694277"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>Функция D3DXMatrixAffineTransformation (D3DX10Math. h)

Формирует матрицу трехмерного преобразования. Аргументы **null** обрабатываются как преобразования Identity.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
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

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), указывающий центр вращения. Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.

</dd> <dt>

 \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , указывающий поворот. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>r</sub> .

</dd> <dt>

*птранслатион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру D3DXVECTOR3, представляющую перевод. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру D3DXMATRIX, которая является матрицей аффинного преобразования.

## <a name="remarks"></a>Комментарии

Эта функция вычисляет матрицу аффинных преобразований с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:

M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT

где:

M<sub>out</sub> = выходная матрица (Тоска)

MS = матрица масштабирования (масштабирование)

M<sub>RC</sub> = центр матрицы вращения (протатионцентер)

M<sub>r</sub> = матрица вращения (расведение)

MT = матрица перевода (Птранслатион)

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixAffineTransformation может использоваться в качестве параметра для другой функции.

Для двумерных преобразований 2D используйте D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
