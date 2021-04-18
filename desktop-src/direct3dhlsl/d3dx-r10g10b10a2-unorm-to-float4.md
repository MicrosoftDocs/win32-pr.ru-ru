---
title: Функция D3DX_R10G10B10A2_UNORM_to_FLOAT4
description: Распаковать \_ \_ \_ данные шейдера в формате DXGI R10G10B10A2 UNORM в XMFLOAT4.
ms.assetid: 36efd611-1450-421a-a34f-fd874589de2a
keywords:
- Функция D3DX_R10G10B10A2_UNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c93bd6fb9cce07ee13a873b4fade91bd322824
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987155"
---
# <a name="d3dx_r10g10b10a2_unorm_to_float4-function"></a>D3DX \_ R10G10B10A2 \_ UNORM \_ to \_ FLOAT4 Function

Распаковать \_ \_ \_ данные шейдера в формате DXGI R10G10B10A2 UNORM в XMFLOAT4.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(
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

 

 





