---
description: Описывает тип событий, которые могут быть разделены контроллером анимации.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: Перечисление D3DXEVENT_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: a7e3dec14876f784bbb4055c483f22552bef80e034798f902196c7b65ff3aa45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804095"
---
# <a name="d3dxevent_type-enumeration"></a>\_Перечисление типов D3DXEVENT

Описывает тип событий, которые могут быть разделены контроллером анимации.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT \_ траккспид**
</dt> <dd>

Скорость записи.

</dd> <dt>

<span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT \_ тракквеигхт**
</dt> <dd>

Вес трекинга.

</dd> <dt>

<span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT \_ траккпоситион**
</dt> <dd>

Расположение Track.

</dd> <dt>

<span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT \_ траккенабле**
</dt> <dd>

Включить флаг.

</dd> <dt>

<span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT \_ приоритибленд**
</dt> <dd>

Значение приоритета смешения.

</dd> <dt>

<span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




