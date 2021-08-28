---
description: Функция D3DXPlaneTransform (D3DX10Math. h) — преобразует плоскость на матрицу. Входная матрица является инверсией фактического преобразования.
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Функция D3DXPlaneTransform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b686a0e279a16650a976920ee812b23cfe0345409926fd6c02166cdb4572235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070064"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a>Функция D3DXPlaneTransform (D3DX10Math. h)

Преобразует плоскость на матрицу. Входная матрица является инверсией фактического преобразования.

## <a name="syntax"></a>Синтаксис


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на [**D3DXPLANE**](d3d10-d3dxplane.md) , содержащий полученную преобразованную плоскость. Ознакомьтесь с примером ниже.

</dd> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Указатель на входную структуру D3DXPLANE, которая содержит плоскость, которая будет преобразована. Вектор (a, b, c), описывающий плоскость, должен быть нормализован перед вызовом этой функции. Ознакомьтесь с примером ниже.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая содержит значения преобразования. Эта матрица должна содержать обратную перестановку значений преобразования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на структуру D3DXPLANE, представляющую преобразованную плоскость. Это то же значение, которое возвращается в параметре тоска, чтобы эту функцию можно было использовать в качестве параметра для другой функции.

## <a name="remarks"></a>Remarks

### <a name="examples"></a>Примеры

Этот пример преобразует плоскость, применяя неоднородный масштаб.


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



Плоскость описывается в AX + by + CZ + DW = 0. Первая плоскость создается с (a, b, c, d) = (0, 1, 1, 0), которая является плоскостью, описанной в разделе y + z = 0. После масштабирования новая плоскость содержит (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), которая показывает новую плоскость, которая будет описываться 0.353 y + 0.235 z = 0.

Параметр pM содержит обратную трансформацию матрицы преобразования. Обратная перестановка необходима этому методу, чтобы правильно преобразовать стандартный вектор преобразованной плоскости.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
