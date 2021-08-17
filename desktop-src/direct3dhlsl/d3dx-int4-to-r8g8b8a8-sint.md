---
title: Функция D3DX_INT4_to_R8G8B8A8_SINT
description: Упаковывает заданный XMINT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ Синт.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- Функция D3DX_INT4_to_R8G8B8A8_SINT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdeb7a92bff374d7b93d647971afd52746fbb768d9a33ec7c3a5c33b1c493523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515868"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a>D3DX \_ INT4 \_ to \_ R8G8B8A8 \_ Синт

Упаковывает заданный XMINT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ Синт.

## <a name="syntax"></a>Синтаксис

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*унпаккединпут* 
</dt> <dd>

Данные шейдера для упаковки.

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

 

 





