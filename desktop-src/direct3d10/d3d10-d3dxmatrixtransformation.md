---
description: Формирует матрицу преобразования. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: Функция D3DXMatrixTransformation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: db1d88ad04e4aaa51232cfdba3168779805b22c3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720961"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a>Функция D3DXMatrixTransformation (D3DX10Math. h)

Формирует матрицу преобразования. Аргументы **null** обрабатываются как преобразования Identity.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.

</dd> <dt>

*пскалингцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий центральную точку масштабирования. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица Identity M <sub>SC</sub> .

</dd> <dt>

*пскалингротатион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , указывающий поворот масштабирования. Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>SR</sub> .

</dd> <dt>

*пскалинг* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру D3DXVECTOR3, вектор масштабирования. Если этот аргумент имеет **значение NULL**, к формуле в примечаниях применяется удостоверение MS Matrix.

</dd> <dt>

*протатионцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру D3DXVECTOR3 — точку, определяющую центр вращения. Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.

</dd> <dt>

 \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на структуру D3DXQUATERNION, указывающую поворот. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>r</sub> .

</dd> <dt>

*птранслатион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру D3DXVECTOR3, представляющую перевод. Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру D3DXMATRIX, которая является матрицей преобразования.

## <a name="remarks"></a>Комментарии

Эта функция вычисляет матрицу преобразования с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* M<sub>SR</sub> \* M<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

где:

M<sub>out</sub> = выходная матрица (Тоска)

M<sub>SC</sub> = матрица центра масштабирования (пскалингцентер)

M<sub>SR</sub> = матрица вращения масштабирования (пскалингротатион)

Матрица MS = масштабирования (Пскалинг)

M<sub>RC</sub> = центр матрицы вращения (протатионцентер)

M<sub>r</sub> = матрица вращения (расведение)

MT = матрица перевода (Птранслатион)

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixTransformation может использоваться в качестве параметра для другой функции.

Для двумерных преобразований используйте [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
