---
title: Функция D3DX_SRGB_to_FLOAT_inexact
description: Преобразует значение SRGB в FLOAT. | Функция D3DX_SRGB_to_FLOAT_inexact
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- Функция D3DX_SRGB_to_FLOAT_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9dd841e022da85d609c203f57288af62a6c99ecc9f56079982308a095285f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515695"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX \_ sRGB \_ для \_ \_ неточной функции

Преобразует значение SRGB в FLOAT.

## <a name="syntax"></a>Синтаксис

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Val* 
</dt> <dd>

Значение SRGB для преобразования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Преобразованное значение SRGB.

## <a name="remarks"></a>Remarks

Эта функция не имеет достаточно большой точности для получения точного ответа. Альтернативная функция [**D3DX \_ sRGB \_ to \_ float**](d3dx-srgb-to-float.md) использует таблицу уточняющих запросов для точного преобразования sRGB в float.

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

 

 





