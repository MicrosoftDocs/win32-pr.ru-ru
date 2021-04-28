---
description: Функция D3DXQuaternionMultiply (D3DX10Math. h) умножает два кватерниона.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Функция D3DXQuaternionMultiply (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4f84ecac1eb910f4b3c97aba6ed42691c70b5b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103162"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>Функция D3DXQuaternionMultiply (D3DX10Math. h)

Умножает два кватерниона.

## <a name="syntax"></a>Синтаксис


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.

</dd> <dt>

*pQ1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) .

</dd> <dt>

*pQ2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на структуру [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , которая является произведением двух кватернионов.

## <a name="remarks"></a>Remarks

Результат представляет собой поворот Q1, за которым следует поворот Q2 (out = Q2 \* Q1). Это делается так, что **D3DXQuaternionMultiply** поддерживает ту же семантику, что и [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) , поскольку единичные кватерниона можно рассматривать как другой способ представления матриц вращения.

Преобразования объединяются в одном и том же порядке для функций **D3DXQuaternionMultiply** и [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) . Например, предположим, что mX и mY представляют те же вращения, что и ККС и Ки, и m, и q будут представлять одни и те же повороты.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



Умножение кватернионов не коммутативной.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция **D3DXQuaternionMultiply** может использоваться в качестве параметра для другой функции.

Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
