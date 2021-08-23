---
title: Функция D3DX_FLOAT2_to_R16G16_FLOAT
description: Упаковывает заданный XMFLOAT2 обратно в формат DXGI \_ \_ R16G16 \_ float.
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- Функция D3DX_FLOAT2_to_R16G16_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f96d9c2652966ef4b35f4c07ec13d1ea5b6f92af641c2e86a1bf4e0b12ca4487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516610"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a>D3DX \_ FLOAT2 \_ to \_ R16G16 \_ float Function

Упаковывает заданный XMFLOAT2 обратно в формат DXGI \_ \_ R16G16 \_ float.

## <a name="syntax"></a>Синтаксис

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
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
| Заголовок<br/> | <dl> <dt>D3DX \_ дксгиформатконверт. inl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции](format-conversion-functions.md)
</dt> <dt>

[Распаковка и \_ формат упаковки для редактирования образа In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





