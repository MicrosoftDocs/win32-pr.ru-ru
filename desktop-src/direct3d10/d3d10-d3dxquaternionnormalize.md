---
description: Функция D3DXQuaternionNormalize (D3DX10Math. h) — выдает кватернион, равный единице измерения.
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: Функция D3DXQuaternionNormalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b6664c6f5149066822197dd8ac2f76918c204ec5cb9e479b21c9793c885aeff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991104"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a>Функция D3DXQuaternionNormalize (D3DX10Math. h)

Выдает кватернион для единицы измерения длины.

## <a name="syntax"></a>Синтаксис


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.

</dd> <dt>

*pQ* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на исходную структуру D3DXQUATERNION.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на структуру D3DXQUATERNION, которая является нормальным для кватерниона.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXQuaternionNormalize может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
