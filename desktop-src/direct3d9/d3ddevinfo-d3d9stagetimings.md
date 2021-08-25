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
ms.openlocfilehash: eb4302b86d31c074f58fd003601557864aee152da9e532771336097f4228ea61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676734"
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

## <a name="remarks"></a>Remarks

Для оптимальной производительности рекомендуется использовать сбалансированную нагрузку.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
