---
title: Функция D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Распаковка формата DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4. | Функция D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- Функция D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede0d10bd8c90514771fa6520eb41e0bd555a3d969b230bb2932665ec0c81796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727349"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ Точная функция

Распаковка формата DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

## <a name="remarks"></a>Remarks

Эта функция использует инструкции шейдера, которые не имеют достаточно высокой точности для получения точного ответа. Альтернативная функция [**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) использует таблицу подстановки, хранящуюся в шейдере, чтобы дать точное преобразование sRGB для преобразования с плавающей запятой.

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

 

 





