---
description: Функция D3DXPlaneNormalize (D3DX10Math. h) — нормализует коэффициенты плоскости таким образом, чтобы у плоскости была нормальная длина.
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
ms.openlocfilehash: cf4429e324a5ce1554c5c37c929625153c74764cb9d03618f633f35ecd416748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754154"
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

## <a name="remarks"></a>Remarks

Эта функция нормализует плоскость таким образом, чтобы \| a, b, c \| = = 1.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, эта функция может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
