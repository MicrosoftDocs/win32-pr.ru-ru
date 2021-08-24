---
description: Функция D3DXQuaternionMultiply (D3dx9math. h) умножает два кватерниона.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Функция D3DXQuaternionMultiply (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4fe5c7f6d95bef19ce77e7ea7815e6808eae63e7643bbfc40e6b0fa1bb45767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750074"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a>Функция D3DXQuaternionMultiply (D3dx9math. h)

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

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.

</dd> <dt>

*pQ1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .

</dd> <dt>

*pQ2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является произведением двух кватернионов.

## <a name="remarks"></a>Remarks

Результат представляет собой поворот Q1, за которым следует поворот Q2 (out = Q2 \* Q1). Это делается так, что **D3DXQuaternionMultiply** поддерживает ту же семантику, что и [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) , поскольку единичные кватерниона можно рассматривать как другой способ представления матриц вращения.

Преобразования объединяются в одном и том же порядке для функций **D3DXQuaternionMultiply** и [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) . Например, предположим, что mX и mY представляют те же вращения, что и ККС и Ки, и m, и q будут представлять одни и те же повороты.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



Умножение кватернионов не коммутативной.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXQuaternionMultiply** может использоваться в качестве параметра для другой функции.

Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




