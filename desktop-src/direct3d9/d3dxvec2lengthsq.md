---
description: Возвращает квадрат длины 2D-вектора.
ms.assetid: 0ecc40bb-7613-463a-a8a0-5e184feb441f
title: Функция D3DXVec2LengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b05ad62f1a7ee26cfb25251b43c3df9dfe87314c5b1d92ac19f65e19416d3ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804064"
---
# <a name="d3dxvec2lengthsq-function"></a>Функция D3DXVec2LengthSq

Возвращает квадрат длины 2D-вектора.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXVec2LengthSq(
  _In_ const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Длина квадрата вектора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Length**](d3dxvec2length.md)
</dt> </dl>

 

 
