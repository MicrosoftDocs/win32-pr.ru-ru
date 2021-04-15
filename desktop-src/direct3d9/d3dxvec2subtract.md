---
description: Вычитает два двумерных вектора.
ms.assetid: e5a693e9-b143-41d5-923d-3f3f71461a42
title: Функция D3DXVec2Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c12f41da7594f3eff9743eed7a1b0780f36c5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547871"
---
# <a name="d3dxvec2subtract-function"></a>Функция D3DXVec2Subtract

Вычитает два двумерных вектора.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR2* D3DXVec2Subtract(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является разностью двух векторов.

## <a name="remarks"></a>Комментарии

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXVec2Subtract** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Add**](d3dxvec2add.md)
</dt> <dt>

[**D3DXVec2Scale**](d3dxvec2scale.md)
</dt> </dl>

 

 




