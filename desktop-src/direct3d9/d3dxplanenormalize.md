---
description: Функция D3DXPlaneNormalize (D3dx9math. h) — нормализует коэффициенты плоскости таким образом, чтобы у плоскости была нормальная длина.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Функция D3DXPlaneNormalize (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a8a5a80526e013c85caf59b3a6a3d6c595a3c10a6e29687882c7789765368d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952314"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>Функция D3DXPlaneNormalize (D3dx9math. h)

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

Тип: **[ **D3DXPLANE**](d3dxplane.md)\***

Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.

</dd> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](d3dxplane.md) \***

Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXPLANE**](d3dxplane.md)\***

Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , представляющую нормальную плоскость плоскости.

## <a name="remarks"></a>Remarks

Эта функция нормализует плоскость таким образом, чтобы \| a, b, c \| = = 1.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, эта функция может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




