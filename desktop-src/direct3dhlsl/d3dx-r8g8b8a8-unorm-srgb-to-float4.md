---
title: Функция D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
description: Распаковка формата DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4. | Функция D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
ms.assetid: 67ad1768-aeb9-4c01-ae3e-0cd79476a459
keywords:
- Функция D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e373ccb8035b19da7c44ee05a07dd0351ca8f48d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986849"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 Function

Распаковка формата DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(
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
| Header<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции](format-conversion-functions.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





