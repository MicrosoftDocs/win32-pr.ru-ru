---
title: Функция D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
description: Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- Функция D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f61e484675b94e1089436ce0b3bd564b3103a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355770"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a>D3DX \_ FLOAT4 \_ в \_ R8G8B8A8 \_ UNORM \_ sRGB

Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.

## <a name="syntax"></a>Синтаксис

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
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

 

 





