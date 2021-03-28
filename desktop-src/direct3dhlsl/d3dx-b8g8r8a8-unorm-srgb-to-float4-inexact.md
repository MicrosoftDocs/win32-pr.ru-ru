---
title: Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4. | Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c813c74569dbd23d17fbe93b6b34f3e39f86bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998303"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ Точная функция

Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4.

## <a name="syntax"></a>Синтаксис

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

## <a name="remarks"></a>Примечания

Эта функция использует инструкции шейдера, которые не имеют достаточно высокой точности для получения точного ответа. Альтернативная функция [**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) использует таблицу подстановки, хранящуюся в шейдере, чтобы дать точное преобразование sRGB для преобразования с плавающей запятой.

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

 

 





