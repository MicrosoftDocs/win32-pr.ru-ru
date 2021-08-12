---
description: Возвращает длину вектора 4D.
ms.assetid: cb332160-3e3d-41b9-bfb0-e3b743d2eafd
title: Функция D3DXVec4Length (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 253f352016c042f9ddb310ebe0cbe4ac3af216b29963de4d30f91786b632b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297588"
---
# <a name="d3dxvec4length-function"></a>Функция D3DXVec4Length

Возвращает длину вектора 4D.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXVec4Length(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Длина вектора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4LengthSq**](d3dxvec4lengthsq.md)
</dt> </dl>

 

 
