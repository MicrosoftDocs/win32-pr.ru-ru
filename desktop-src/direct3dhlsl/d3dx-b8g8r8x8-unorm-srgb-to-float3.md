---
title: Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
description: Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT3. | Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5f638d827a7b6ebf3543b3cde212fd56b0ace41ffb69bf4b7f79b56c28dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793860"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 Function

Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT3.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*паккединпут* 
</dt> <dd>

Упакованные данные шейдера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Распакованные данные шейдера.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции](format-conversion-functions.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





