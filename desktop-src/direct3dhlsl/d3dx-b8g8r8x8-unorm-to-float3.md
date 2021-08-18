---
title: Функция D3DX_B8G8R8X8_UNORM_to_FLOAT3
description: Распаковать \_ \_ \_ данные шейдера в формате DXGI B8G8R8X8 UNORM в XMFLOAT3.
ms.assetid: 0987d71a-89a4-4751-9f32-08e2490204d2
keywords:
- Функция D3DX_B8G8R8X8_UNORM_to_FLOAT3 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac787be8dc856c9f4748b7d2934000c5e4271141284dbb36e45cc1309f111a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793819"
---
# <a name="d3dx_b8g8r8x8_unorm_to_float3-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ to \_ FLOAT3 Function

Распаковать \_ \_ \_ данные шейдера в формате DXGI B8G8R8X8 UNORM в XMFLOAT3.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(
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

 

 





