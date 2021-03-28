---
title: Функция D3DX_R16G16_FLOAT_to_FLOAT2
description: Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- Функция D3DX_R16G16_FLOAT_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fb721e59a63415f98216b6e3f81a92e7598f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157239"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a>D3DX \_ R16G16 \_ с плавающей запятой \_ в \_ FLOAT2 функцию

Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT2.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
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

 

 





