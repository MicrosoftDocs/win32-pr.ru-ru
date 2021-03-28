---
title: Текстуры
description: В этом разделе описываются текстуры, используемые в Direct3D 11, и ссылки на документацию на основе задач для распространенных сценариев.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258731"
---
# <a name="textures"></a><span data-ttu-id="4b6b3-103">Текстуры</span><span class="sxs-lookup"><span data-stu-id="4b6b3-103">Textures</span></span>

<span data-ttu-id="4b6b3-104">Текстура хранит сведения о шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-104">A texture stores texel information.</span></span> <span data-ttu-id="4b6b3-105">В этом разделе описываются текстуры, используемые в Direct3D 11, и ссылки на документацию на основе задач для распространенных сценариев.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-105">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4b6b3-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="4b6b3-106">In this section</span></span>



| <span data-ttu-id="4b6b3-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="4b6b3-107">Topic</span></span>                                                                                                    | <span data-ttu-id="4b6b3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4b6b3-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b6b3-109">Общие сведения о текстурах в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4b6b3-109">Introduction To Textures in Direct3D 11</span></span>](overviews-direct3d-11-resources-textures-intro.md)<br/> | <span data-ttu-id="4b6b3-110">Текстурный ресурс — это структурированный набор данных, предназначенный для хранения текселей.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-110">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="4b6b3-111">Тексель представляет собой наименьший элемент текстуры, который может использоваться конвейером для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-111">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="4b6b3-112">В отличие от буферов текстуры можно фильтровать по дискретизаторам текстур во время их считывания блоками шейдера.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-112">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="4b6b3-113">Тип текстуры влияет на способ ее фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-113">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="4b6b3-114">Каждый шаг текселя содержит от 1 до 4 компонентов, расположенных в одном из форматов DXGI, определенных \_ перечислением в формате DXGI.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-114">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span><br/> |
| [<span data-ttu-id="4b6b3-115">Сжатие блоков текстуры в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4b6b3-115">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)<br/>      | <span data-ttu-id="4b6b3-116">В Direct3D 11 расширена поддержка сжатия блоков для текстур и теперь она включает алгоритмы BC6H и BC7.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-116">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="4b6b3-117">BC6H поддерживает исходные данные цвета из высокодинамичного диапазона, а BC7 обеспечивает качество сжатия выше среднего с меньшим количеством артефактов для стандартных исходных данных RGB.</span><span class="sxs-lookup"><span data-stu-id="4b6b3-117">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span><br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="4b6b3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="4b6b3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b6b3-119">Как создать текстуру</span><span class="sxs-lookup"><span data-stu-id="4b6b3-119">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[<span data-ttu-id="4b6b3-120">Как программно инициализировать текстуру</span><span class="sxs-lookup"><span data-stu-id="4b6b3-120">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[<span data-ttu-id="4b6b3-121">Как инициализировать текстуру из файла</span><span class="sxs-lookup"><span data-stu-id="4b6b3-121">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[<span data-ttu-id="4b6b3-122">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="4b6b3-122">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





