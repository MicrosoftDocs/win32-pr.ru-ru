---
title: Функция D3DX_UINT4_to_R8G8B8A8_UINT
description: Упаковывает заданный XMUINT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ uint.
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- Функция D3DX_UINT4_to_R8G8B8A8_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef8128d2d1989e986d8ff11e2d7e42e85f1fbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998393"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a>D3DX \_ UINT4 \_ to \_ R8G8B8A8 \_ uint, функция

Упаковывает заданный XMUINT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ uint.

## <a name="syntax"></a>Синтаксис

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*унпаккединпут* 
</dt> <dd>

Данные шейдера для упаковки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Упакованные данные шейдера.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции](format-conversion-functions.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





