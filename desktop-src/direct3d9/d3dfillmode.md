---
description: Определяет константы, описывающие режим заполнения.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Перечисление D3DFILLMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e92d91c13718462487eb3dac07ba1d5fc61a2d428bf610dd9575b080d375676d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857454"
---
# <a name="d3dfillmode-enumeration"></a>Перечисление D3DFILLMODE

Определяет константы, описывающие режим заполнения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**\_Точка D3DFILL**
</dt> <dd>

Точки заполнения.

</dd> <dt>

<span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**\_Каркасная схема D3DFILL**
</dt> <dd>

Заполнить каркасы.

</dd> <dt>

<span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_**
</dt> <dd>

Заливка сплошным.

</dd> <dt>

<span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значения в этом перечислимом типе используются \_ состоянием визуализации D3DRS филлмоде.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
