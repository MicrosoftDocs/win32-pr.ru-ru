---
description: Процент времени обработки данных шейдера.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: Структура D3DDEVINFO_D3D9STAGETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674687"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a>\_Структура D3D9STAGETIMINGS D3DDEVINFO

Процент времени обработки данных шейдера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a>Члены

<dl> <dt>

**меморипроцессингперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени, затраченного на доступ к памяти в шейдере.

</dd> <dt>

**компутатионпроцессингперцент**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Процент времени обработки (перемещение данных по регистрам или выполнение математических операций).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для оптимальной производительности рекомендуется использовать сбалансированную нагрузку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
