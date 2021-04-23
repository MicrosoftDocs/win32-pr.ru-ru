---
description: Текстуры — это очень мощное средство для обеспечения реалистичности созданных на компьютере трехмерных изображений. Direct3D поддерживает широкий набор функций для работы с текстурами, предоставляя разработчикам удобный доступ к дополнительным методам обработки текстур.
ms.assetid: 48dcbc86-631e-4bc7-b809-b0e4a0a9ae8e
title: Текстуры Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afebd7217b36ad5f740616e198963314a1d2aca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139286"
---
# <a name="direct3d-textures-direct3d-9"></a><span data-ttu-id="b1698-104">Текстуры Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-104">Direct3D Textures (Direct3D 9)</span></span>

<span data-ttu-id="b1698-105">Текстуры — это очень мощное средство для обеспечения реалистичности созданных на компьютере трехмерных изображений.</span><span class="sxs-lookup"><span data-stu-id="b1698-105">Textures are a powerful tool in creating realism in computer-generated 3D images.</span></span> <span data-ttu-id="b1698-106">Direct3D поддерживает широкий набор функций для работы с текстурами, предоставляя разработчикам удобный доступ к дополнительным методам обработки текстур.</span><span class="sxs-lookup"><span data-stu-id="b1698-106">Direct3D supports an extensive texturing feature set, providing developers with easy access to advanced texturing techniques.</span></span>

<span data-ttu-id="b1698-107">В этом разделе вы узнаете, как приступить к работе с текстурами.</span><span class="sxs-lookup"><span data-stu-id="b1698-107">This section will get you started using textures.</span></span>

-   [<span data-ttu-id="b1698-108">Основные понятия текстурирования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-108">Basic Texturing Concepts (Direct3D 9)</span></span>](basic-texturing-concepts.md)
-   [<span data-ttu-id="b1698-109">Координаты текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-109">Texture Coordinates (Direct3D 9)</span></span>](texture-coordinates.md)
-   [<span data-ttu-id="b1698-110">Фильтрация текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-110">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
-   [<span data-ttu-id="b1698-111">Ресурсы текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-111">Texture Resources (Direct3D 9)</span></span>](texture-resources.md)
-   [<span data-ttu-id="b1698-112">Перенос текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-112">Texture Wrapping (Direct3D 9)</span></span>](texture-wrapping.md)
-   [<span data-ttu-id="b1698-113">Смешение текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-113">Texture Blending (Direct3D 9)</span></span>](texture-blending.md)

<span data-ttu-id="b1698-114">Эти разделы содержат более подробные сведения о дополнительных функциях текстурирования.</span><span class="sxs-lookup"><span data-stu-id="b1698-114">These topics will go into more detail about additional texturing functionality.</span></span>

-   [<span data-ttu-id="b1698-115">Автоматическое создание MIP-карты (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-115">Automatic Generation of Mipmaps (Direct3D 9)</span></span>](automatic-generation-of-mipmaps.md)
-   [<span data-ttu-id="b1698-116">Автоматическое управление текстурами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-116">Automatic Texture Management (Direct3D 9)</span></span>](automatic-texture-management.md)
-   [<span data-ttu-id="b1698-117">Сжатые ресурсы текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-117">Compressed Texture Resources (Direct3D 9)</span></span>](compressed-texture-resources.md)
-   [<span data-ttu-id="b1698-118">Рекомендации по оборудованию для текстурирования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-118">Hardware Considerations for Texturing (Direct3D 9)</span></span>](hardware-considerations-for-texturing.md)
-   [<span data-ttu-id="b1698-119">Ресурсы текстуры тома (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1698-119">Volume Texture Resources (Direct3D 9)</span></span>](volume-texture-resources.md)

<span data-ttu-id="b1698-120">Для повышения производительности рассмотрите возможность использования динамических текстур.</span><span class="sxs-lookup"><span data-stu-id="b1698-120">For improved performance, consider using dynamic textures.</span></span> <span data-ttu-id="b1698-121">Динамические текстуры можно блокировать, производить в них запись и разблокировать для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="b1698-121">A dynamic texture can be locked, written to, and unlocked each frame.</span></span> <span data-ttu-id="b1698-122">См. раздел [Использование динамических текстур](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="b1698-122">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1698-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b1698-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1698-124">Начало работы</span><span class="sxs-lookup"><span data-stu-id="b1698-124">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



