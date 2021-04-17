---
description: Нормализует коэффициенты плоскости, чтобы у плоскости была нормальная длина единицы.
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Функция D3DXPlaneNormalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44d5e9d810653b2cdae233dec803383c74563d08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720951"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a>Функция D3DXPlaneNormalize (D3DX10Math. h)

Нормализует коэффициенты плоскости, чтобы у плоскости была нормальная длина единицы.

## <a name="syntax"></a>Синтаксис


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на [**D3DXPLANE**](d3d10-d3dxplane.md) , который является результатом операции.

</dd> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Указатель на исходную структуру D3DXPLANE.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на структуру D3DXPLANE, представляющую нормальную плоскость плоскости.

## <a name="remarks"></a>Комментарии

Эта функция нормализует плоскость таким образом, чтобы \| a, b, c \| = = 1.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, эта функция может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
