---
description: Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Перечисление D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 4b29cbb958b2aa8af02000fc62d4d3a848c2efba585bd927674c9ceca9d65d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634964"
---
# <a name="d3dx10_channel_flag-enumeration"></a>\_ \_ Перечисление флагов канала D3DX10

Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**\_Канал D3DX10 \_ красный**
</dt> <dd>

Указывает, что следует использовать красный канал.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**\_Канал D3DX10 \_ синий**
</dt> <dd>

Указывает, что должен использоваться синий канал.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Зеленый канал \_ D3DX10**
</dt> <dd>

Указывает, что должен использоваться зеленый канал.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**\_Альфа-канал D3DX10 \_**
</dt> <dd>

Указывает, что следует использовать альфа-канал.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_ \_ Освещенность канала D3DX10**
</dt> <dd>

Указывает, что следует использовать луминацесие красного, зеленого и синего каналов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




