---
title: Пример текстуры тома DDS
description: Для текстуры тома используйте ДДСКАПС \_ Complex, DDSCAPS2 \_ том, ддсд \_ Depth, flags, Set и двдепс. Текстура тома — это расширение стандартной текстуры для Direct3D 9; текстуру тома можно определить с помощью или без MIP-карты.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710089"
---
# <a name="dds-volume-texture-example"></a><span data-ttu-id="40b29-104">Пример текстуры тома DDS</span><span class="sxs-lookup"><span data-stu-id="40b29-104">DDS Volume Texture Example</span></span>

<span data-ttu-id="40b29-105">Для текстуры тома используйте ДДСКАПС \_ Complex, DDSCAPS2 \_ том, ддсд \_ Depth, flags, Set и двдепс.</span><span class="sxs-lookup"><span data-stu-id="40b29-105">For a volume texture, use the DDSCAPS\_COMPLEX, DDSCAPS2\_VOLUME, DDSD\_DEPTH, flags and set and dwDepth.</span></span> <span data-ttu-id="40b29-106">Текстура тома — это расширение стандартной текстуры для Direct3D 9; текстуру тома можно определить с помощью или без MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="40b29-106">A volume texture is an extension of a standard texture for Direct3D 9; a volume texture is can be defined with or without mipmaps.</span></span>

<span data-ttu-id="40b29-107">Для томов без MIP-карты каждый срез глубины записывается в файл по порядку.</span><span class="sxs-lookup"><span data-stu-id="40b29-107">For volumes without mipmaps, each depth slice is written to the file in order.</span></span> <span data-ttu-id="40b29-108">Если включены MIP-карты, все срезы глубины для данного уровня mipmap записываются вместе, при этом каждый уровень содержит половину столько срезов, сколько на предыдущем уровне, как минимум 1.</span><span class="sxs-lookup"><span data-stu-id="40b29-108">If mipmaps are included, all depth slices for a given mipmap level are written together, with each level containing half as many slices as the previous level with a minimum of 1.</span></span>

<span data-ttu-id="40b29-109">Например, Схема тома 64-by-64-на-4 с использованием формата пикселей R8G8B8 (3 байта на пиксель) со всеми уровнями mipmap будет содержать следующее:</span><span class="sxs-lookup"><span data-stu-id="40b29-109">For example, a 64-by-64-by-4 volume map using a pixel format of R8G8B8 (3 bytes per pixel) with all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="40b29-110">Компоненты DDS</span><span class="sxs-lookup"><span data-stu-id="40b29-110">DDS Components</span></span>                      | <span data-ttu-id="40b29-111">\# Байт</span><span class="sxs-lookup"><span data-stu-id="40b29-111">\# Bytes</span></span>    |
|-------------------------------------|-------------|
| <span data-ttu-id="40b29-112">заголовок</span><span class="sxs-lookup"><span data-stu-id="40b29-112">header</span></span>                              | <span data-ttu-id="40b29-113">128 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-113">128 bytes</span></span>   |
| <span data-ttu-id="40b29-114">64-by-64 срез 1 из 4 основного образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-114">64-by-64 slice 1 of 4 main image.</span></span>   | <span data-ttu-id="40b29-115">12288 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-115">12288 bytes</span></span> |
| <span data-ttu-id="40b29-116">64-by-64 срез 2 из 4 основного образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-116">64-by-64 slice 2 of 4 main image.</span></span>   | <span data-ttu-id="40b29-117">12288 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-117">12288 bytes</span></span> |
| <span data-ttu-id="40b29-118">64-by-64 срез 3 из 4 основного образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-118">64-by-64 slice 3 of 4 main image.</span></span>   | <span data-ttu-id="40b29-119">12288 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-119">12288 bytes</span></span> |
| <span data-ttu-id="40b29-120">64-by-64 срез 4 из 4 основного образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-120">64-by-64 slice 4 of 4 main image.</span></span>   | <span data-ttu-id="40b29-121">12288 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-121">12288 bytes</span></span> |
| <span data-ttu-id="40b29-122">32-by-32 срез 1 из 2 mipmapного образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-122">32-by-32 slice 1 of 2 mipmap image.</span></span> | <span data-ttu-id="40b29-123">3072 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-123">3072 bytes</span></span>  |
| <span data-ttu-id="40b29-124">32-by-32 срез 2 из 2 mipmap образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-124">32-by-32 slice 2 of 2 mipmap image.</span></span> | <span data-ttu-id="40b29-125">3072 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-125">3072 bytes</span></span>  |
| <span data-ttu-id="40b29-126">16 на 16 срез 1 из 1 mipmap изображения.</span><span class="sxs-lookup"><span data-stu-id="40b29-126">16-by-16 slice 1 of 1 mipmap image.</span></span> | <span data-ttu-id="40b29-127">768 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-127">768 bytes</span></span>   |
| <span data-ttu-id="40b29-128">8 на 8 срез 1 из 1 mipmap изображения.</span><span class="sxs-lookup"><span data-stu-id="40b29-128">8-by-8 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="40b29-129">192 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-129">192 bytes</span></span>   |
| <span data-ttu-id="40b29-130">4-по 4 срез 1 из 1 mipmap образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-130">4-by-4 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="40b29-131">48 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-131">48 bytes</span></span>    |
| <span data-ttu-id="40b29-132">2-by-2 срез 1 из 1 mipmapного образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-132">2-by-2 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="40b29-133">12 байт</span><span class="sxs-lookup"><span data-stu-id="40b29-133">12 bytes</span></span>    |
| <span data-ttu-id="40b29-134">1-by-1 срез 1 из 1 mipmap образа.</span><span class="sxs-lookup"><span data-stu-id="40b29-134">1-by-1 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="40b29-135">3 байта</span><span class="sxs-lookup"><span data-stu-id="40b29-135">3 bytes</span></span>     |



 

<span data-ttu-id="40b29-136">Обратите внимание, что минимальный уровень mipmap составляет всего 3 байта, поскольку биткаунт имеет значение 24, а на этом уровне нет дополнительного сжатия.</span><span class="sxs-lookup"><span data-stu-id="40b29-136">Note that the smallest mipmap level is only 3 bytes because the bitcount is 24 and there is no added compression at this level.</span></span>

<span data-ttu-id="40b29-137">Поддержка текстур томов была добавлена в DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="40b29-137">Support for volume textures was added in DirectX 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b29-138">См. также</span><span class="sxs-lookup"><span data-stu-id="40b29-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b29-139">Руководством по программированию для DDS</span><span class="sxs-lookup"><span data-stu-id="40b29-139">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




