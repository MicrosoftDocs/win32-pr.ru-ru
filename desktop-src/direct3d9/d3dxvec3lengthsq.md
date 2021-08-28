---
description: Возвращает квадрат длины трехмерного вектора.
ms.assetid: 25dc50cc-542b-4989-a858-9b37603393a0
title: Функция D3DXVec3LengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bfb57d8275231ed02d696abe0d6886dcc9efc788b912fe1f57a70ebfaa020380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803879"
---
# <a name="d3dxvec3lengthsq-function"></a>Функция D3DXVec3LengthSq

Возвращает квадрат длины трехмерного вектора.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXVec3LengthSq(
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

[**D3DXVec3Length**](d3dxvec3length.md)
</dt> </dl>

 

 
