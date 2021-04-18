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
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986882"
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

## <a name="remarks"></a>Примечания

Эта функция не имеет достаточно большой точности для получения точного ответа. Альтернативная функция [**D3DX \_ sRGB \_ to \_ float**](d3dx-srgb-to-float.md) использует таблицу уточняющих запросов для точного преобразования sRGB в float.

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

 

 





