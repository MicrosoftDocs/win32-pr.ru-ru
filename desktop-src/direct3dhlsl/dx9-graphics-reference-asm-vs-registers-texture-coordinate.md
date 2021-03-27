---
title: Регистр текстурных координат (Справочник по HLSL VS)
description: Этот выходной регистр шейдера вершин содержит координаты текстуры на вершину.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134479"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a><span data-ttu-id="0b9f5-103">Регистр текстурных координат (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="0b9f5-103">Texture Coordinate Register (HLSL VS reference)</span></span>

<span data-ttu-id="0b9f5-104">Этот выходной регистр шейдера вершин содержит координаты текстуры на вершину.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-104">This vertex shader output register contains per-vertex texture coordinates.</span></span>

<span data-ttu-id="0b9f5-105">Регистр состоит из свойств, определяющих принцип работы каждой ККМ.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="0b9f5-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="0b9f5-106">Property</span></span>        | <span data-ttu-id="0b9f5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0b9f5-107">Description</span></span>   |
|-----------------|---------------|
| <span data-ttu-id="0b9f5-108">Имя</span><span class="sxs-lookup"><span data-stu-id="0b9f5-108">Name</span></span>            | <span data-ttu-id="0b9f5-109">oT0 - oT7</span><span class="sxs-lookup"><span data-stu-id="0b9f5-109">oT0 - oT7</span></span>     |
| <span data-ttu-id="0b9f5-110">Count</span><span class="sxs-lookup"><span data-stu-id="0b9f5-110">Count</span></span>           | <span data-ttu-id="0b9f5-111">Восемь векторов</span><span class="sxs-lookup"><span data-stu-id="0b9f5-111">Eight vectors</span></span> |
| <span data-ttu-id="0b9f5-112">Разрешения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="0b9f5-112">I/O permissions</span></span> | <span data-ttu-id="0b9f5-113">Только на запись</span><span class="sxs-lookup"><span data-stu-id="0b9f5-113">Write-only</span></span>    |



 

<span data-ttu-id="0b9f5-114">Регистры выходных координат текстуры являются массивом регистров выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-114">The output texture coordinates registers are an array of output data registers.</span></span> <span data-ttu-id="0b9f5-115">Данные регистра просматриваются и используются в качестве координат текстуры на стадиях выборки текстуры для передачи данных в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-115">The register data is iterated and used as texture coordinates by the texture sampling stages to supply data to the pixel shader.</span></span>

<span data-ttu-id="0b9f5-116">При записи в регистр текстурных координат рекомендуется передавать в качестве измерения соответствующей карты текстуры только столько значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-116">When writing to a texture coordinate register, it is recommended that you pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="0b9f5-117">Управление значениями, передаваемыми с помощью модификатора.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-117">Control the values that are passed with a modifier.</span></span> <span data-ttu-id="0b9f5-118">Например, используйте. XY для двухмерной текстурной гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-118">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="0b9f5-119">Флаги конвейера вершинной функции, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4), должны быть равны нулю, если используется программируемый шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-119">The fixed function vertex pipeline flags, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF\_COUNT1, D3DTTFF\_COUNT2, D3DTTFF\_COUNT3, D3DTTFF\_COUNT4), should be set to zero if you are using a programmable vertex shader.</span></span>

<span data-ttu-id="0b9f5-120">Данные вершин объекта предоставляют координаты текстуры ввода.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-120">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="0b9f5-121">Объекты, которые не используют мозаичные текстуры, обычно имеют координаты текстуры в диапазоне \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0b9f5-121">Objects that do not use tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="0b9f5-122">Объекты, использующие мозаичные текстуры, такие как ландшафта, обычно имеют координаты текстуры в диапазоне от \[ -n, + n, \] где n может быть любым числом с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-122">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-n,+n\] where n can be any floating point number.</span></span>

<span data-ttu-id="0b9f5-123">Интерполяция текстурных координат выполняется для данных вершин для растрирования.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-123">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="0b9f5-124">Во время растрирования координаты текстуры интерполируются между вершинами объекта, изменены путем переноса текстур и масштабируются по размеру текстуры (также принимая во внимание режимы адресации текстуры) для создания целочисленного индекса.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-124">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping, and scaled by the texture size (also taking into account texture addressing modes) to produce an integer index.</span></span> <span data-ttu-id="0b9f5-125">Затем индекс используется для поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-125">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="0b9f5-126">Используйте значение Макстекстуререпеат в [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) , чтобы определить, сколько раз можно выполнить мозаичное заполнение текстуры.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-126">Use the MaxTextureRepeat value in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) to determine how many times a texture can be tiled.</span></span>

## <a name="example"></a><span data-ttu-id="0b9f5-127">Например, .</span><span class="sxs-lookup"><span data-stu-id="0b9f5-127">Example</span></span>

<span data-ttu-id="0b9f5-128">Объявите регистр координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-128">Declare the texture coordinate register.</span></span>


```
dcl_texcoord v7
```



<span data-ttu-id="0b9f5-129">Скопируйте координаты текстуры на вершину в выходной регистр.</span><span class="sxs-lookup"><span data-stu-id="0b9f5-129">Copy the per-vertex texture coordinates to the output register.</span></span>


```
mov oT0, v7
```





| <span data-ttu-id="0b9f5-130">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="0b9f5-130">Vertex shader versions</span></span>      | <span data-ttu-id="0b9f5-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="0b9f5-131">1\_1</span></span> | <span data-ttu-id="0b9f5-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0b9f5-132">2\_0</span></span> | <span data-ttu-id="0b9f5-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0b9f5-133">2\_sw</span></span> | <span data-ttu-id="0b9f5-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0b9f5-134">2\_x</span></span> | <span data-ttu-id="0b9f5-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0b9f5-135">3\_0</span></span> | <span data-ttu-id="0b9f5-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0b9f5-136">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="0b9f5-137">Регистр координаты текстуры</span><span class="sxs-lookup"><span data-stu-id="0b9f5-137">Texture Coordinate Register</span></span> | <span data-ttu-id="0b9f5-138">x</span><span class="sxs-lookup"><span data-stu-id="0b9f5-138">x</span></span>    | <span data-ttu-id="0b9f5-139">x</span><span class="sxs-lookup"><span data-stu-id="0b9f5-139">x</span></span>    | <span data-ttu-id="0b9f5-140">x</span><span class="sxs-lookup"><span data-stu-id="0b9f5-140">x</span></span>     | <span data-ttu-id="0b9f5-141">x</span><span class="sxs-lookup"><span data-stu-id="0b9f5-141">x</span></span>    | <span data-ttu-id="0b9f5-142">x</span><span class="sxs-lookup"><span data-stu-id="0b9f5-142">x</span></span>    | <span data-ttu-id="0b9f5-143">x</span><span class="sxs-lookup"><span data-stu-id="0b9f5-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="0b9f5-144">См. также</span><span class="sxs-lookup"><span data-stu-id="0b9f5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b9f5-145">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="0b9f5-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 