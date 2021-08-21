---
title: Функция D3DX_R8G8B8A8_SNORM_to_FLOAT4
description: Распаковать \_ \_ \_ данные шейдера в формате DXGI R8G8B8A8 снорм в XMFLOAT4.
ms.assetid: 2f2b9d5e-f4d0-470a-a4bb-b333d57f03e7
keywords:
- Функция D3DX_R8G8B8A8_SNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c7da0ff2b6cb1bc725ed880cbb75d9ea7313df12a2e170c94dfde1e4efb4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490984"
---
# <a name="d3dx_r8g8b8a8_snorm_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ снорм \_ to \_ FLOAT4 Function

Распаковать \_ \_ \_ данные шейдера в формате DXGI R8G8B8A8 снорм в XMFLOAT4.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(
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

 

 





