---
description: Буферы трафаретов — это методика использования буфера глубины, которую можно обновить при отрисовке геометрии и использовать снова в качестве маски для рисования большей геометрии.
ms.assetid: 0e1ef114-1d49-4beb-9fc2-2cfbbcae7add
title: Теневая версия (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7581f8f7720adf0550beda6ef16b6292178276
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805285"
---
# <a name="shadowing-direct3d-9"></a><span data-ttu-id="2c562-103">Теневая версия (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2c562-103">Shadowing (Direct3D 9)</span></span>

<span data-ttu-id="2c562-104">Буферы трафаретов — это методика использования буфера глубины, которую можно обновить при отрисовке геометрии и использовать снова в качестве маски для рисования большей геометрии.</span><span class="sxs-lookup"><span data-stu-id="2c562-104">Stencil buffers are a depth-buffer technique that can be updated as geometry is rendered, and used again as a mask for drawing more geometry.</span></span> <span data-ttu-id="2c562-105">К общим эффектам относятся зеркала, тени (расширенная методика), разрешения и т. д.</span><span class="sxs-lookup"><span data-stu-id="2c562-105">Common effects include mirrors, shadows (an advanced technique), dissolves, and so on.</span></span> <span data-ttu-id="2c562-106">В [примере шадовволуме](https://msdn.microsoft.com/library/Ee418792(v=VS.85).aspx) используются буферы трафаретов для реализации теней в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="2c562-106">The [ShadowVolume Sample](https://msdn.microsoft.com/library/Ee418792(v=VS.85).aspx) uses stencil buffers to implement real-time shadows.</span></span> <span data-ttu-id="2c562-107">Дополнительные сведения содержатся в [наборе элементов с двумя сторонами (Direct3D 9)](two-sided-stencil.md).</span><span class="sxs-lookup"><span data-stu-id="2c562-107">Additional information is contained in [Two-Sided Stencil (Direct3D 9)](two-sided-stencil.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c562-108">См. также</span><span class="sxs-lookup"><span data-stu-id="2c562-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c562-109">Конвейер пикселей</span><span class="sxs-lookup"><span data-stu-id="2c562-109">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



