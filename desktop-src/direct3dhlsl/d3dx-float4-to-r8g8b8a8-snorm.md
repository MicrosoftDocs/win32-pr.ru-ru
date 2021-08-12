---
title: Функция D3DX_FLOAT4_to_R8G8B8A8_SNORM
description: Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ снорм.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- Функция D3DX_FLOAT4_to_R8G8B8A8_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0382cc5e7bfc47b8046eec437cbc25cf559c9116b4e6215cce9a3fb8f344f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286732"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a>D3DX \_ FLOAT4 \_ to \_ R8G8B8A8 \_ снорм Function

Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ снорм.

## <a name="syntax"></a>Синтаксис

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
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
| Заголовок<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции](format-conversion-functions.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





