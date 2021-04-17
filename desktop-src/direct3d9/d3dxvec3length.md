---
description: Возвращает длину трехмерного вектора.
ms.assetid: 78da506c-3169-48e9-934c-cc09271a10d4
title: Функция D3DXVec3Length (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 653e53fb22961c858c7649f95e4453fec08087fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703718"
---
# <a name="d3dxvec3length-function"></a>Функция D3DXVec3Length

Возвращает длину трехмерного вектора.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXVec3Length(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Длина вектора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
</dt> </dl>

 

 
