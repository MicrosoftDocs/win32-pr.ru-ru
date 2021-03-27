---
title: Функция D3DX_FLOAT2_to_R16G16_SNORM
description: Упаковывает заданный XMFLOAT2 обратно в формат DXGI \_ \_ R16G16 \_ снорм.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- Функция D3DX_FLOAT2_to_R16G16_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000396"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a>D3DX \_ FLOAT2 \_ to \_ R16G16 \_ снорм Function

Упаковывает заданный XMFLOAT2 обратно в формат DXGI \_ \_ R16G16 \_ снорм.

## <a name="syntax"></a>Синтаксис

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*унпаккединпут* 
</dt> <dd>

Распакованные данные шейдера.

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

 

 





