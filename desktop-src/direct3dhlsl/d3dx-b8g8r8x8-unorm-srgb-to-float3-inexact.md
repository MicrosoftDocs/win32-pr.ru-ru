---
title: Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
description: Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT3. | Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f696381402d8ad42c92310029631e66b457e3b211d22d8f9de3dd98c1f1312ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986874"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 \_ Точная функция

Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT3.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
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

Эта функция использует инструкции шейдера, которые не имеют достаточно высокой точности для получения точного ответа. Альтернативная функция [**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) использует таблицу подстановки, хранящуюся в шейдере, чтобы дать точное преобразование sRGB для преобразования с плавающей запятой.

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

 

 





