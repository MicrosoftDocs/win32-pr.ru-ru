---
description: 'Флаги спрайтов, которые указывают API рисования спрайтов, как вести себя. Они передаются в ID3DX10Sprite:: Begin.'
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: Перечисление D3DX10_SPRITE_FLAG (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 53b2c7965beaeb2976e88d38f5af90d546f644b6d4879964c23b2166cd51b19b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634944"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>\_ \_ Перечисление ФЛАГов СПРАЙТа D3DX10

Флаги спрайтов, которые указывают API рисования спрайтов, как вести себя. Они передаются в [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Текстура D3DX10ной сортировки спрайтов \_ \_**
</dt> <dd>

Отсортируйте спрайты по текстуре перед отрисовкой, чтобы при наличии нескольких спрайтов с той же текстурой, в которой все эти спрайты будут подготавливаться к просмотру одновременно, тем самым улучшая производительность.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10ная \_ Сортировка спрайта \_ \_ \_ \_ на \_ передний план**
</dt> <dd>

Отсортируйте спрайты с обратно на передний план, чтобы они были первыми выведены из камеры.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**\_ \_ Глубина сортировки D3DX10 для спрайта \_ \_ спереди \_ на \_ задний план**
</dt> <dd>

Отсортируйте спрайты от начала до конца, чтобы они ближе отрисованы в первую очередь.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ \_ состояние сохранения спрайта \_**
</dt> <dd>

Сохраняет состояние, чтобы при вызове [**ID3DX10Sprite:: end**](id3dx10sprite-end.md) состояние восстанавливается до вызова [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) .

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**Текстуры ADDREF D3DX10 для \_ спрайтов \_ \_**
</dt> <dd>

Вызывает AddRef для всех текстур, когда они передаются в [**ID3DX10Sprite::D равспритесбуфферед**](id3dx10sprite-drawspritesbuffered.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

После выполнения обратной сортировки с начала и до заднего плана автоматически выполняется дополнительная сортировка по текстуре. Это полезно при наличии множества спрайтов с одинаковой текстурой на одной плоскости, например при рисовании пользовательского интерфейса в игре.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




