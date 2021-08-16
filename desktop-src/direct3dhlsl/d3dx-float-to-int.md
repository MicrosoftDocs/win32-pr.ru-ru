---
title: Функция D3DX_FLOAT_to_INT
description: Преобразует значение FLOAT в тип INT.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- Функция D3DX_FLOAT_to_INT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb76c5c459daaaba4dd7d038b65b9dc34e895f283b66545684ef1f5fb10c95cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516667"
---
# <a name="d3dx_float_to_int-function"></a>\_Функция D3DX float \_ to \_ int

Преобразует значение FLOAT в тип INT.

## <a name="syntax"></a>Синтаксис

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*\_V* 
</dt> <dd>

Значение v.

</dd> <dt>

*\_Масштабирование* 
</dt> <dd>

Значение масштаба.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Преобразованное значение FLOAT

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

 

 





