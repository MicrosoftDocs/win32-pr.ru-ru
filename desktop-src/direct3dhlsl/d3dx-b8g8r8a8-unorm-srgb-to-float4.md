---
title: Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
description: Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4. | Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620823a572b7eb23f05bdda83866aae982f326dfb70ca6856309abc9d96f05b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516600"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 Function

Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции](format-conversion-functions.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





