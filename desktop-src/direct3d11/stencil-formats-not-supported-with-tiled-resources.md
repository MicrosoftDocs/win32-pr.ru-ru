---
title: Форматы трафаретов не поддерживаются для мозаичных ресурсов
description: Форматы, содержащие набор элементов, не поддерживаются для мозаичных ресурсов.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067253"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a><span data-ttu-id="a2c2f-103">Форматы трафаретов не поддерживаются для мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2c2f-103">Stencil formats not supported with tiled resources</span></span>

<span data-ttu-id="a2c2f-104">Форматы, содержащие набор элементов, не поддерживаются для мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2c2f-104">Formats that contain stencil aren't supported with tiled resources.</span></span>

<span data-ttu-id="a2c2f-105">Форматы, содержащие набор элементов, включают в себя \_ Формат DXGI \_ D24 \_ UNORM \_ S8 \_ uint (и связанные форматы в семействе R24G8) и \_ Формат DXGI \_ d32 \_ float \_ S8X24 \_ uint (и связанные форматы в семействе R32G8X24).</span><span class="sxs-lookup"><span data-stu-id="a2c2f-105">Formats that contain stencil include DXGI\_FORMAT\_D24\_UNORM\_S8\_UINT (and related formats in the R24G8 family) and DXGI\_FORMAT\_D32\_FLOAT\_S8X24\_UINT (and related formats in the R32G8X24 family).</span></span>

<span data-ttu-id="a2c2f-106">Некоторые реализации хранят данные о глубине и трафарете в отдельных распределениях, другие хранят их вместе.</span><span class="sxs-lookup"><span data-stu-id="a2c2f-106">Some implementations store depth and stencil in separate allocations while others store them together.</span></span> <span data-ttu-id="a2c2f-107">Управление плитками для этих двух схем будет отличаться, в одном API-интерфейсе нельзя объединить или рационализировать эти различия.</span><span class="sxs-lookup"><span data-stu-id="a2c2f-107">Tile management for the two schemes would have to be different, and no single API can abstract or rationalize the differences.</span></span> <span data-ttu-id="a2c2f-108">Мы рекомендуем в будущем оборудовании поддерживать независимые поверхности глубины и трафарета, каждую с независимой разбивкой по плиткам.</span><span class="sxs-lookup"><span data-stu-id="a2c2f-108">We recommend for future hardware to support independent depth and stencil surfaces, each independently tiled.</span></span> <span data-ttu-id="a2c2f-109">32. Глубина глубины 128x128 плитки, а 8 элементов 256x256 — плитки.</span><span class="sxs-lookup"><span data-stu-id="a2c2f-109">32 bit depth would have 128x128 tiles, and 8 bit stencil would have 256x256 tiles.</span></span> <span data-ttu-id="a2c2f-110">Таким образом приложения будут иметь дело с рассогласованием формы плиток между буферами глубины и трафарета.</span><span class="sxs-lookup"><span data-stu-id="a2c2f-110">Therefore, applications would have to live with tile shape misalignment between depth and stencil.</span></span> <span data-ttu-id="a2c2f-111">Однако та же проблема уже существует с различными форматами целевой поверхности прорисовки.</span><span class="sxs-lookup"><span data-stu-id="a2c2f-111">But the same problem exists with different render target surface formats already.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2c2f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a2c2f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2c2f-113">Мозаичная обработка ресурсов и совместное использование устройств</span><span class="sxs-lookup"><span data-stu-id="a2c2f-113">Tiled resource cross process and device sharing</span></span>](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




