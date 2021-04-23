---
description: Определяет типы текстур образца для шейдеров вершин.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Перечисление D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424330"
---
# <a name="d3dsampler_texture_type-enumeration"></a><span data-ttu-id="60e9a-103">\_ \_ Перечисление типов текстур D3DSAMPLER</span><span class="sxs-lookup"><span data-stu-id="60e9a-103">D3DSAMPLER\_TEXTURE\_TYPE enumeration</span></span>

<span data-ttu-id="60e9a-104">Определяет типы текстур образца для шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="60e9a-104">Defines the sampler texture types for vertex shaders.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60e9a-105">Syntax</span></span>


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="60e9a-106">Константы</span><span class="sxs-lookup"><span data-stu-id="60e9a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="60e9a-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="60e9a-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="60e9a-108">Неинициализированное значение.</span><span class="sxs-lookup"><span data-stu-id="60e9a-108">Uninitialized value.</span></span> <span data-ttu-id="60e9a-109">Значение этого элемента равно 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.</span><span class="sxs-lookup"><span data-stu-id="60e9a-109">The value of this element is 0 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="60e9a-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**</span><span class="sxs-lookup"><span data-stu-id="60e9a-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT\_2D**</span></span>
</dt> <dd>

<span data-ttu-id="60e9a-111">Объявление двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="60e9a-111">Declaring a 2D texture.</span></span> <span data-ttu-id="60e9a-112">Значение этого элемента равно 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.</span><span class="sxs-lookup"><span data-stu-id="60e9a-112">The value of this element is 2 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="60e9a-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Куб D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="60e9a-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT\_CUBE**</span></span>
</dt> <dd>

<span data-ttu-id="60e9a-114">Объявление текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="60e9a-114">Declaring a cube texture.</span></span> <span data-ttu-id="60e9a-115">Значение этого элемента равно 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.</span><span class="sxs-lookup"><span data-stu-id="60e9a-115">The value of this element is 3 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="60e9a-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Том D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="60e9a-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="60e9a-117">Объявление текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="60e9a-117">Declaring a volume texture.</span></span> <span data-ttu-id="60e9a-118">Значение этого элемента равно 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.</span><span class="sxs-lookup"><span data-stu-id="60e9a-118">The value of this element is 4 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="60e9a-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="60e9a-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="60e9a-120">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="60e9a-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="60e9a-121">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="60e9a-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="60e9a-122">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="60e9a-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60e9a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="60e9a-123">Requirements</span></span>



| <span data-ttu-id="60e9a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="60e9a-124">Requirement</span></span> | <span data-ttu-id="60e9a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="60e9a-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60e9a-126">Header</span><span class="sxs-lookup"><span data-stu-id="60e9a-126">Header</span></span><br/> | <dl> <span data-ttu-id="60e9a-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e9a-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e9a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60e9a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e9a-129">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="60e9a-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




