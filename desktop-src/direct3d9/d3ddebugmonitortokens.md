---
description: Определяет маркеры монитора отладки.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Перечисление D3DDEBUGMONITORTOKENS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ed64939714c3ee69fb30e56afe23e52e780405287c898e138ee86822f1c5e0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989074"
---
# <a name="d3ddebugmonitortokens-enumeration"></a>Перечисление D3DDEBUGMONITORTOKENS

Определяет маркеры монитора отладки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**\_Включить D3DDMT**
</dt> <dd>

Включите монитор отладки.

</dd> <dt>

<span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**\_Отключение D3DDMT**
</dt> <dd>

Отключите монитор отладки.

</dd> <dt>

<span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Значения в этом перечислимом типе используются в \_ состоянии рендеринга D3DRS дебугмонитортокен и относятся только к отладочным сборкам.

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

 

 
