---
description: Возвращает нормализованную версию вектора 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Функция D3DXVec4Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38d97f337711375d1d414eb78fb317672bc7c5cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081957"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a>Функция D3DXVec4Normalize (D3dx9math. h)

Возвращает нормализованную версию вектора 4D.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является нормализованной версией вектора.

## <a name="remarks"></a>Комментарии

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXVec4Normalize** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




