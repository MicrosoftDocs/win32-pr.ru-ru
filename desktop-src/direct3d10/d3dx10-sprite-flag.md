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
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720947"
---
# <a name="d3dx10_sprite_flag-enumeration"></a><span data-ttu-id="86ea7-104">\_ \_ Перечисление ФЛАГов СПРАЙТа D3DX10</span><span class="sxs-lookup"><span data-stu-id="86ea7-104">D3DX10\_SPRITE\_FLAG enumeration</span></span>

<span data-ttu-id="86ea7-105">Флаги спрайтов, которые указывают API рисования спрайтов, как вести себя.</span><span class="sxs-lookup"><span data-stu-id="86ea7-105">Sprite flags that tell the sprite drawing API how to behave.</span></span> <span data-ttu-id="86ea7-106">Они передаются в [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).</span><span class="sxs-lookup"><span data-stu-id="86ea7-106">These are passed into [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86ea7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86ea7-107">Syntax</span></span>


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a><span data-ttu-id="86ea7-108">Константы</span><span class="sxs-lookup"><span data-stu-id="86ea7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="86ea7-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Текстура D3DX10ной сортировки спрайтов \_ \_**</span><span class="sxs-lookup"><span data-stu-id="86ea7-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10\_SPRITE\_SORT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="86ea7-110">Отсортируйте спрайты по текстуре перед отрисовкой, чтобы при наличии нескольких спрайтов с той же текстурой, в которой все эти спрайты будут подготавливаться к просмотру одновременно, тем самым улучшая производительность.</span><span class="sxs-lookup"><span data-stu-id="86ea7-110">Sort the sprites by texture before rendering so that when there are many sprites with the same texture that texture all of those sprites will be rendered at the same time, thereby improving performance.</span></span>

</dd> <dt>

<span data-ttu-id="86ea7-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10ная \_ Сортировка спрайта \_ \_ \_ \_ на \_ передний план**</span><span class="sxs-lookup"><span data-stu-id="86ea7-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_BACK\_TO\_FRONT**</span></span>
</dt> <dd>

<span data-ttu-id="86ea7-112">Отсортируйте спрайты с обратно на передний план, чтобы они были первыми выведены из камеры.</span><span class="sxs-lookup"><span data-stu-id="86ea7-112">Sort the sprites from back to front to that those farther away from the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="86ea7-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**\_ \_ Глубина сортировки D3DX10 для спрайта \_ \_ спереди \_ на \_ задний план**</span><span class="sxs-lookup"><span data-stu-id="86ea7-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_FRONT\_TO\_BACK**</span></span>
</dt> <dd>

<span data-ttu-id="86ea7-114">Отсортируйте спрайты от начала до конца, чтобы они ближе отрисованы в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="86ea7-114">Sort the sprites from front to back so that those closer to the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="86ea7-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ \_ состояние сохранения спрайта \_**</span><span class="sxs-lookup"><span data-stu-id="86ea7-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10\_SPRITE\_SAVE\_STATE**</span></span>
</dt> <dd>

<span data-ttu-id="86ea7-116">Сохраняет состояние, чтобы при вызове [**ID3DX10Sprite:: end**](id3dx10sprite-end.md) состояние восстанавливается до вызова [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="86ea7-116">Saves the state so that when [**ID3DX10Sprite::End**](id3dx10sprite-end.md) is called, it will restore the state to the way it was before [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) was called.</span></span>

</dd> <dt>

<span data-ttu-id="86ea7-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**Текстуры ADDREF D3DX10 для \_ спрайтов \_ \_**</span><span class="sxs-lookup"><span data-stu-id="86ea7-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10\_SPRITE\_ADDREF\_TEXTURES**</span></span>
</dt> <dd>

<span data-ttu-id="86ea7-118">Вызывает AddRef для всех текстур, когда они передаются в [**ID3DX10Sprite::D равспритесбуфферед**](id3dx10sprite-drawspritesbuffered.md).</span><span class="sxs-lookup"><span data-stu-id="86ea7-118">Calls AddRef on all of the textures when they are passed into [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86ea7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86ea7-119">Remarks</span></span>

<span data-ttu-id="86ea7-120">После выполнения обратной сортировки с начала и до заднего плана автоматически выполняется дополнительная сортировка по текстуре.</span><span class="sxs-lookup"><span data-stu-id="86ea7-120">After a front-to-back or back-to-front sort is done, it will automatically do a secondary sort by texture.</span></span> <span data-ttu-id="86ea7-121">Это полезно при наличии множества спрайтов с одинаковой текстурой на одной плоскости, например при рисовании пользовательского интерфейса в игре.</span><span class="sxs-lookup"><span data-stu-id="86ea7-121">This is helpful for when there are many sprites with the same texture all on the same plane, such as when drawing the user interface in a game.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ea7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="86ea7-122">Requirements</span></span>



| <span data-ttu-id="86ea7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="86ea7-123">Requirement</span></span> | <span data-ttu-id="86ea7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="86ea7-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86ea7-125">Header</span><span class="sxs-lookup"><span data-stu-id="86ea7-125">Header</span></span><br/> | <dl> <span data-ttu-id="86ea7-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="86ea7-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ea7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86ea7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ea7-128">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="86ea7-128">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




