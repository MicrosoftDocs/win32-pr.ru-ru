---
description: Конструирует плоскость из трех точек.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Функция D3DXPlaneFromPoints (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713458"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a>Функция D3DXPlaneFromPoints (D3dx9math. h)

Конструирует плоскость из трех точек.

## <a name="syntax"></a>Синтаксис


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXPLANE**](d3dxplane.md)\***

Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.

</dd> <dt>

*pV3* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXPLANE**](d3dxplane.md)\***

Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , созданную из заданных точек.

## <a name="remarks"></a>Комментарии

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXPlaneFromPoints** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneFromPointNormal**](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




