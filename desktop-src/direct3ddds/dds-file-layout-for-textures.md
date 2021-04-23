---
title: Пример текстуры DDS
description: Для несжатой текстуры используйте \_ Флаги ддсд тон и ддпф \_ RGB. для сжатой текстуры используйте \_ Флаги ДДСД линеарсизе и ддпф \_ FourCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710090"
---
# <a name="dds-texture-example"></a><span data-ttu-id="88c85-103">Пример текстуры DDS</span><span class="sxs-lookup"><span data-stu-id="88c85-103">DDS Texture Example</span></span>

<span data-ttu-id="88c85-104">Для несжатой текстуры используйте \_ Флаги ддсд тон и ддпф \_ RGB. для сжатой текстуры используйте \_ Флаги ДДСД линеарсизе и ддпф \_ FourCC.</span><span class="sxs-lookup"><span data-stu-id="88c85-104">For an uncompressed texture, use the DDSD\_PITCH and DDPF\_RGB flags; for a compressed texture, use the DDSD\_LINEARSIZE and DDPF\_FOURCC flags.</span></span> <span data-ttu-id="88c85-105">Для текстуры мипмаппед используйте \_ также сложные флаги ддсд MIPMAPCOUNT, ддскапс mipmap и ддскапс, а также составной \_ \_ элемент Count mipmap.</span><span class="sxs-lookup"><span data-stu-id="88c85-105">For a mipmapped texture, use the DDSD\_MIPMAPCOUNT, DDSCAPS\_MIPMAP, and DDSCAPS\_COMPLEX flags also as well as the mipmap count member.</span></span> <span data-ttu-id="88c85-106">Если создаются MIP-карты, обычно записываются все уровни вниз до 1 – 1.</span><span class="sxs-lookup"><span data-stu-id="88c85-106">If mipmaps are generated, all levels down to 1-by-1 are usually written.</span></span>

<span data-ttu-id="88c85-107">Для сжатой текстуры размер каждого изображения уровня mipmap обычно составляет один четвертый размер предыдущего, с минимальным размером в 8 (DXT1) или 16 (DXT2-5) байт (для квадратных текстур).</span><span class="sxs-lookup"><span data-stu-id="88c85-107">For a compressed texture, the size of each mipmap level image is typically one-fourth the size of the previous, with a minimum of 8 (DXT1) or 16 (DXT2-5) bytes (for square textures).</span></span> <span data-ttu-id="88c85-108">Используйте следующую формулу, чтобы вычислить размер каждого уровня для текстуры, отличной от квадратной.</span><span class="sxs-lookup"><span data-stu-id="88c85-108">Use the following formula to calculate the size of each level for a non-square texture:</span></span>


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



<span data-ttu-id="88c85-109">В этой таблице перечислены объемы пространства, занимаемого каждым слоем для текстуры R8G8B8 с 256 по 256, без использования сжатия.</span><span class="sxs-lookup"><span data-stu-id="88c85-109">This table lists the amount of space taken up by each layer for a 256-by-256 R8G8B8 texture, without using compression.</span></span>



| <span data-ttu-id="88c85-110">Компоненты DDS</span><span class="sxs-lookup"><span data-stu-id="88c85-110">DDS Components</span></span>          | <span data-ttu-id="88c85-111">\# Байт</span><span class="sxs-lookup"><span data-stu-id="88c85-111">\# Bytes</span></span> |
|-------------------------|----------|
| <span data-ttu-id="88c85-112">заголовок</span><span class="sxs-lookup"><span data-stu-id="88c85-112">header</span></span>                  | <span data-ttu-id="88c85-113">128</span><span class="sxs-lookup"><span data-stu-id="88c85-113">128</span></span>      |
| <span data-ttu-id="88c85-114">основной образ 256-by-256</span><span class="sxs-lookup"><span data-stu-id="88c85-114">256-by-256 main image</span></span>   | <span data-ttu-id="88c85-115">196608</span><span class="sxs-lookup"><span data-stu-id="88c85-115">196608</span></span>   |
| <span data-ttu-id="88c85-116">изображение mipmap с 128 по 128</span><span class="sxs-lookup"><span data-stu-id="88c85-116">128-by-128 mipmap image</span></span> | <span data-ttu-id="88c85-117">49152</span><span class="sxs-lookup"><span data-stu-id="88c85-117">49152</span></span>    |
| <span data-ttu-id="88c85-118">изображение mipmap с 64 по 64</span><span class="sxs-lookup"><span data-stu-id="88c85-118">64-by-64 mipmap image</span></span>   | <span data-ttu-id="88c85-119">12288</span><span class="sxs-lookup"><span data-stu-id="88c85-119">12288</span></span>    |
| <span data-ttu-id="88c85-120">изображение mipmap с 32 по 32</span><span class="sxs-lookup"><span data-stu-id="88c85-120">32-by-32 mipmap image</span></span>   | <span data-ttu-id="88c85-121">3072</span><span class="sxs-lookup"><span data-stu-id="88c85-121">3072</span></span>     |
| <span data-ttu-id="88c85-122">изображение размером 16 на 16 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-122">16-by-16 mipmap image</span></span>   | <span data-ttu-id="88c85-123">768</span><span class="sxs-lookup"><span data-stu-id="88c85-123">768</span></span>      |
| <span data-ttu-id="88c85-124">изображение с 8 по 8 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-124">8-by-8 mipmap image</span></span>     | <span data-ttu-id="88c85-125">192</span><span class="sxs-lookup"><span data-stu-id="88c85-125">192</span></span>      |
| <span data-ttu-id="88c85-126">изображение с 4 по 4 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-126">4-by-4 mipmap image</span></span>     | <span data-ttu-id="88c85-127">48</span><span class="sxs-lookup"><span data-stu-id="88c85-127">48</span></span>       |
| <span data-ttu-id="88c85-128">изображение с 2 по 2 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-128">2-by-2 mipmap image</span></span>     | <span data-ttu-id="88c85-129">12</span><span class="sxs-lookup"><span data-stu-id="88c85-129">12</span></span>       |
| <span data-ttu-id="88c85-130">изображение с 1 по 1 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-130">1-by-1 mipmap image</span></span>     | <span data-ttu-id="88c85-131">3</span><span class="sxs-lookup"><span data-stu-id="88c85-131">3</span></span>        |



 

<span data-ttu-id="88c85-132">В этой таблице перечислены объемы пространства, занимаемого каждым слоем для той же текстуры с помощью сжатия (DXT1).</span><span class="sxs-lookup"><span data-stu-id="88c85-132">This table lists the amount of space taken up by each layer for the same texture using compression (DXT1).</span></span>



| <span data-ttu-id="88c85-133">Компоненты DDS</span><span class="sxs-lookup"><span data-stu-id="88c85-133">DDS Components</span></span>         | <span data-ttu-id="88c85-134">\# Байт</span><span class="sxs-lookup"><span data-stu-id="88c85-134">\# Bytes</span></span> |
|------------------------|----------|
| <span data-ttu-id="88c85-135">заголовок</span><span class="sxs-lookup"><span data-stu-id="88c85-135">header</span></span>                 | <span data-ttu-id="88c85-136">128</span><span class="sxs-lookup"><span data-stu-id="88c85-136">128</span></span>      |
| <span data-ttu-id="88c85-137">основной образ 256-by-64</span><span class="sxs-lookup"><span data-stu-id="88c85-137">256-by-64 main image</span></span>   | <span data-ttu-id="88c85-138">8192</span><span class="sxs-lookup"><span data-stu-id="88c85-138">8192</span></span>     |
| <span data-ttu-id="88c85-139">изображение mipmap с 128 по 32</span><span class="sxs-lookup"><span data-stu-id="88c85-139">128-by-32 mipmap image</span></span> | <span data-ttu-id="88c85-140">2048</span><span class="sxs-lookup"><span data-stu-id="88c85-140">2048</span></span>     |
| <span data-ttu-id="88c85-141">изображение mipmap с 64 по 16</span><span class="sxs-lookup"><span data-stu-id="88c85-141">64-by-16 mipmap image</span></span>  | <span data-ttu-id="88c85-142">512</span><span class="sxs-lookup"><span data-stu-id="88c85-142">512</span></span>      |
| <span data-ttu-id="88c85-143">образ mipmap с 32 по 8</span><span class="sxs-lookup"><span data-stu-id="88c85-143">32-by-8 mipmap image</span></span>   | <span data-ttu-id="88c85-144">128</span><span class="sxs-lookup"><span data-stu-id="88c85-144">128</span></span>      |
| <span data-ttu-id="88c85-145">изображение с 16 по 4 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-145">16-by-4 mipmap image</span></span>   | <span data-ttu-id="88c85-146">32</span><span class="sxs-lookup"><span data-stu-id="88c85-146">32</span></span>       |
| <span data-ttu-id="88c85-147">изображение с 8 по 2 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-147">8-by-2 mipmap image</span></span>    | <span data-ttu-id="88c85-148">16</span><span class="sxs-lookup"><span data-stu-id="88c85-148">16</span></span>       |
| <span data-ttu-id="88c85-149">изображение с 4 по 1 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-149">4-by-1 mipmap image</span></span>    | <span data-ttu-id="88c85-150">8</span><span class="sxs-lookup"><span data-stu-id="88c85-150">8</span></span>        |
| <span data-ttu-id="88c85-151">изображение с 2 по 1 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-151">2-by-1 mipmap image</span></span>    | <span data-ttu-id="88c85-152">8</span><span class="sxs-lookup"><span data-stu-id="88c85-152">8</span></span>        |
| <span data-ttu-id="88c85-153">изображение с 1 по 1 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-153">1-by-1 mipmap image</span></span>    | <span data-ttu-id="88c85-154">8</span><span class="sxs-lookup"><span data-stu-id="88c85-154">8</span></span>        |



 

<span data-ttu-id="88c85-155">В этой таблице перечислены объемы пространства, занимаемого каждым слоем для одной текстуры с помощью формата сжатия DXGI (в данном случае BC3 \_ UNORM), поэтому требуется расширенный заголовок:</span><span class="sxs-lookup"><span data-stu-id="88c85-155">This table lists the amount of space taken up by each layer for the same texture using a DXGI compression format (in this case BC3\_UNORM) that therefore requires the extended header:</span></span>



| <span data-ttu-id="88c85-156">Компоненты DDS</span><span class="sxs-lookup"><span data-stu-id="88c85-156">DDS Components</span></span>                                                | <span data-ttu-id="88c85-157">\# Байт</span><span class="sxs-lookup"><span data-stu-id="88c85-157">\# Bytes</span></span> |
|---------------------------------------------------------------|----------|
| <span data-ttu-id="88c85-158">заголовок (FourCC имеет значение "СОДЕРЖИМЫМ DX10")</span><span class="sxs-lookup"><span data-stu-id="88c85-158">header (FourCC set to "DX10")</span></span>                                 | <span data-ttu-id="88c85-159">128</span><span class="sxs-lookup"><span data-stu-id="88c85-159">128</span></span>      |
| <span data-ttu-id="88c85-160">расширенный заголовок (для формата DXGI задан \_ Формат DXGI \_ BC3 \_ UNORM)</span><span class="sxs-lookup"><span data-stu-id="88c85-160">extended header (DXGI format set to DXGI\_FORMAT\_BC3\_UNORM)</span></span> | <span data-ttu-id="88c85-161">20</span><span class="sxs-lookup"><span data-stu-id="88c85-161">20</span></span>       |
| <span data-ttu-id="88c85-162">основной образ 256-by-64</span><span class="sxs-lookup"><span data-stu-id="88c85-162">256-by-64 main image</span></span>                                          | <span data-ttu-id="88c85-163">16384</span><span class="sxs-lookup"><span data-stu-id="88c85-163">16384</span></span>    |
| <span data-ttu-id="88c85-164">изображение mipmap с 128 по 32</span><span class="sxs-lookup"><span data-stu-id="88c85-164">128-by-32 mipmap image</span></span>                                        | <span data-ttu-id="88c85-165">4096</span><span class="sxs-lookup"><span data-stu-id="88c85-165">4096</span></span>     |
| <span data-ttu-id="88c85-166">изображение mipmap с 64 по 16</span><span class="sxs-lookup"><span data-stu-id="88c85-166">64-by-16 mipmap image</span></span>                                         | <span data-ttu-id="88c85-167">1024</span><span class="sxs-lookup"><span data-stu-id="88c85-167">1024</span></span>     |
| <span data-ttu-id="88c85-168">образ mipmap с 32 по 8</span><span class="sxs-lookup"><span data-stu-id="88c85-168">32-by-8 mipmap image</span></span>                                          | <span data-ttu-id="88c85-169">256</span><span class="sxs-lookup"><span data-stu-id="88c85-169">256</span></span>      |
| <span data-ttu-id="88c85-170">изображение с 16 по 4 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-170">16-by-4 mipmap image</span></span>                                          | <span data-ttu-id="88c85-171">64</span><span class="sxs-lookup"><span data-stu-id="88c85-171">64</span></span>       |
| <span data-ttu-id="88c85-172">изображение с 8 по 2 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-172">8-by-2 mipmap image</span></span>                                           | <span data-ttu-id="88c85-173">32</span><span class="sxs-lookup"><span data-stu-id="88c85-173">32</span></span>       |
| <span data-ttu-id="88c85-174">изображение с 4 по 1 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-174">4-by-1 mipmap image</span></span>                                           | <span data-ttu-id="88c85-175">16</span><span class="sxs-lookup"><span data-stu-id="88c85-175">16</span></span>       |
| <span data-ttu-id="88c85-176">изображение с 2 по 1 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-176">2-by-1 mipmap image</span></span>                                           | <span data-ttu-id="88c85-177">16</span><span class="sxs-lookup"><span data-stu-id="88c85-177">16</span></span>       |
| <span data-ttu-id="88c85-178">изображение с 1 по 1 mipmap</span><span class="sxs-lookup"><span data-stu-id="88c85-178">1-by-1 mipmap image</span></span>                                           | <span data-ttu-id="88c85-179">16</span><span class="sxs-lookup"><span data-stu-id="88c85-179">16</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="88c85-180">См. также</span><span class="sxs-lookup"><span data-stu-id="88c85-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c85-181">Руководством по программированию для DDS</span><span class="sxs-lookup"><span data-stu-id="88c85-181">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




