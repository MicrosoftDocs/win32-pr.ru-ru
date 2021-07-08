---
description: Определяет типы ресурсов.
ms.assetid: 6b360fb1-4a5a-47a2-bef9-d8234770bf0c
title: Перечисление D3DRESOURCETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecb6b0c84f884df6441f3272a585ee3e09928661
ms.sourcegitcommit: bfab92e16614d4fa54b044917358261232bda81a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2021
ms.locfileid: "113489688"
---
# <a name="d3dresourcetype-enumeration"></a><span data-ttu-id="d9f67-103">Перечисление D3DRESOURCETYPE</span><span class="sxs-lookup"><span data-stu-id="d9f67-103">D3DRESOURCETYPE enumeration</span></span>

<span data-ttu-id="d9f67-104">Определяет типы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9f67-104">Defines resource types.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9f67-105">Syntax</span></span>


```C++
typedef enum D3DRESOURCETYPE { 
  D3DRTYPE_SURFACE        = 1,
  D3DRTYPE_VOLUME         = 2,
  D3DRTYPE_TEXTURE        = 3,
  D3DRTYPE_VOLUMETEXTURE  = 4,
  D3DRTYPE_CUBETEXTURE    = 5,
  D3DRTYPE_VERTEXBUFFER   = 6,
  D3DRTYPE_INDEXBUFFER    = 7,
  D3DRTYPE_FORCE_DWORD    = 0x7fffffff
} D3DRESOURCETYPE, *LPD3DRESOURCETYPE;
```



## <a name="constants"></a><span data-ttu-id="d9f67-106">Константы</span><span class="sxs-lookup"><span data-stu-id="d9f67-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d9f67-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**\_Поверхность D3DRTYPE**</span><span class="sxs-lookup"><span data-stu-id="d9f67-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**D3DRTYPE\_SURFACE**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-108">Ресурс Surface.</span><span class="sxs-lookup"><span data-stu-id="d9f67-108">Surface resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9f67-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**\_Том D3DRTYPE**</span><span class="sxs-lookup"><span data-stu-id="d9f67-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**D3DRTYPE\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-110">Ресурс тома.</span><span class="sxs-lookup"><span data-stu-id="d9f67-110">Volume resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9f67-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**\_Текстура D3DRTYPE**</span><span class="sxs-lookup"><span data-stu-id="d9f67-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**D3DRTYPE\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-112">Ресурс текстуры.</span><span class="sxs-lookup"><span data-stu-id="d9f67-112">Texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9f67-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE \_ волуметекстуре**</span><span class="sxs-lookup"><span data-stu-id="d9f67-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE\_VOLUMETEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-114">Ресурс текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="d9f67-114">Volume texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9f67-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE \_ кубетекстуре**</span><span class="sxs-lookup"><span data-stu-id="d9f67-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE\_CUBETEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-116">Ресурс текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="d9f67-116">Cube texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9f67-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE \_ вертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="d9f67-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE\_VERTEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-118">Ресурс буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="d9f67-118">Vertex buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9f67-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE \_ индексбуффер**</span><span class="sxs-lookup"><span data-stu-id="d9f67-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE\_INDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-120">Ресурс буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="d9f67-120">Index buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="d9f67-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d9f67-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d9f67-122">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="d9f67-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d9f67-123">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="d9f67-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d9f67-124">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="d9f67-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9f67-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d9f67-125">Requirements</span></span>



| <span data-ttu-id="d9f67-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d9f67-126">Requirement</span></span> | <span data-ttu-id="d9f67-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d9f67-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f67-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9f67-128">Header</span></span><br/> | <dl> <span data-ttu-id="d9f67-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f67-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f67-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d9f67-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f67-131">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="d9f67-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d9f67-132">**IDirect3DResource9:: GetType**</span><span class="sxs-lookup"><span data-stu-id="d9f67-132">**IDirect3DResource9::GetType**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-gettype)
</dt> </dl>

 

 
