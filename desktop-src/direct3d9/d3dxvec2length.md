---
description: Возвращает длину 2D-вектора.
ms.assetid: 376fd2ca-c89d-41e7-a15c-a79d7281d010
title: Функция D3DXVec2Length (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bddfbb617b05212b04977965fc4d9497df8b839757aa137e43962072f3ed2226
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676054"
---
# <a name="d3dxvec2length-function"></a>Функция D3DXVec2Length

Возвращает длину 2D-вектора.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXVec2Length(
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

Длина вектора.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2LengthSq**](d3dxvec2lengthsq.md)
</dt> </dl>

 

 
