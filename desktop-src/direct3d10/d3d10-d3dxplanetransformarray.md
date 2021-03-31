---
description: Преобразует массив плоскостей по матрице. Векторы, описывающие каждую плоскость, должны быть нормализованы.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Функция D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081902"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>Функция D3DXPlaneTransformArray (D3DX10Math. h)

Преобразует массив плоскостей по матрице. Векторы, описывающие каждую плоскость, должны быть нормализованы.

## <a name="syntax"></a>Синтаксис


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на структуру [**D3DXPLANE**](d3d10-d3dxplane.md) , содержащую полученную преобразованную плоскость. См. пример.

</dd> <dt>

*Шаг* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг каждой преобразованной плоскости.

</dd> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Указатель на входную структуру D3DXPLANE, содержащую массив плоскостей для преобразования. Вектор (a, b, c), описывающий плоскость, должен быть нормализован перед вызовом этой функции. См. пример.

</dd> <dt>

*Пстриде* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг для каждой непреобразованной плоскости.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая содержит обратное преобразование значений преобразования.

</dd> <dt>

*n* \[ в\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число преобразуемых плоскостей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на структуру D3DXPLANE, представляющую преобразованную плоскость. Это то же значение, которое возвращается в параметре тоска, чтобы эту функцию можно было использовать в качестве параметра для другой функции.

## <a name="remarks"></a>Комментарии

Этот пример преобразует одну плоскость, применяя неоднородный масштаб.


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



Плоскость описывается в AX + by + CZ + DW = 0. Первая плоскость создается с (a, b, c, d) = (0, 1, 1, 0), которая является плоскостью, описанной в разделе y + z = 0. После масштабирования новая плоскость содержит (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), которая показывает новую плоскость, которая будет описываться 0.353 y + 0.235 z = 0.

Параметр pM содержит обратную перестановку матрицы преобразования. Обратная перестановка необходима этому методу, чтобы правильно преобразовать стандартный вектор преобразованной плоскости.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
