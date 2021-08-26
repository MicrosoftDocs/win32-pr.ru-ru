---
title: Перечисление D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Перечисление D3DX11_CHANNEL_FLAG Direct3D 11
- Указатель перечисления LPD3DX11_CHANNEL_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f8142d34235a151638e1043928521666f2d1751319ee785d22b92004a14421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028314"
---
# <a name="d3dx11_channel_flag-enumeration"></a>\_ \_ Перечисление флагов канала D3DX11

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 

Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**\_Канал D3DX11 \_ красный**
</dt> <dd>

Указывает, что следует использовать красный канал.

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**\_Канал D3DX11 \_ синий**
</dt> <dd>

Указывает, что должен использоваться синий канал.

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**\_Зеленый канал \_ D3DX11**
</dt> <dd>

Указывает, что должен использоваться зеленый канал.

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**\_Альфа-канал D3DX11 \_**
</dt> <dd>

Указывает, что следует использовать альфа-канал.

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_ \_ Освещенность канала D3DX11**
</dt> <dd>

Указывает, что следует использовать луминацесие красного, зеленого и синего каналов.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





