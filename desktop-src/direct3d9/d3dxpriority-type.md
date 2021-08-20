---
description: Определяет тип приоритета, которому назначена анимация анимации.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: Перечисление D3DXPRIORITY_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: e7ea5b7447b896c6b582280216af4d6c05cc540286ad31a2bfb337975fe6c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524853"
---
# <a name="d3dxpriority_type-enumeration"></a>\_Перечисление типов D3DXPRIORITY

Определяет тип приоритета, которому назначена анимация анимации.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ низкий**
</dt> <dd>

Отслеживание должно смешиваться со всеми дорожками с низким приоритетом, прежде чем смешивание с низким приоритетом будет смешиваться с высоким приоритетом.

</dd> <dt>

<span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ высокий**
</dt> <dd>

Отслеживание следует смешивать со всеми высокоприоритетными дорожками, прежде чем смешивание с высоким приоритетом будет смешиваться с низким приоритетом.

</dd> <dt>

<span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Курсы с одинаковым приоритетом смешиваются друг с другом, а два результирующих значения смешиваются с использованием коэффициента смешения приоритетов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




