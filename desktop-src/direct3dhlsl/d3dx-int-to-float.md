---
title: Функция D3DX_INT_to_FLOAT
description: Преобразует значение типа INT в тип FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- Функция D3DX_INT_to_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d49320c2b7bfd53b2fa4e0303a7d2e9bf6c22427557ee3827aed31f5915d1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855494"
---
# <a name="d3dx_int_to_float-function"></a>\_Функция D3DX int \_ to \_ float

Преобразует значение типа INT в тип FLOAT.

## <a name="syntax"></a>Синтаксис

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
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

Преобразованное значение int.

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

 

 





