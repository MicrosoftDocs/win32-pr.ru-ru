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
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987164"
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

*\_3,3* 
</dt> <dd>

Значение v.

</dd> <dt>

*\_Измените* 
</dt> <dd>

Значение масштаба.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Преобразованное значение int.

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

 

 





