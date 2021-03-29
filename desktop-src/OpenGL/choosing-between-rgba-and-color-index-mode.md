---
title: Выбор между RGBA и режимом Color-Index
description: Как правило, для приложений OpenGL следует использовать режим RGBA; Он обеспечивает большую гибкость, чем режим индексов цвета для таких эффектов, как заливка, освещение, сопоставление цветов, туман, сглаживание и смешение.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL в Windows, режим RGBA
- OpenGL в Windows, режим индексирования цветов
- Режим RGBA OpenGL
- режим индексирования цветов OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775959"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a><span data-ttu-id="ca385-107">Выбор между RGBA и режимом Color-Index</span><span class="sxs-lookup"><span data-stu-id="ca385-107">Choosing Between RGBA and Color-Index Mode</span></span>

<span data-ttu-id="ca385-108">Как правило, для приложений OpenGL следует использовать режим RGBA; Он обеспечивает большую гибкость, чем режим индексов цвета для таких эффектов, как заливка, освещение, сопоставление цветов, туман, сглаживание и смешение.</span><span class="sxs-lookup"><span data-stu-id="ca385-108">In general, use the RGBA mode for your OpenGL applications; it provides more flexibility than the color-index mode for effects such as shading, lighting, color mapping, fog, antialiasing, and blending.</span></span>

<span data-ttu-id="ca385-109">Рассмотрите возможность использования режима индексов цветов в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="ca385-109">Consider using the color-index mode in the following cases:</span></span>

-   <span data-ttu-id="ca385-110">Если доступно ограниченное число битпланес; режим индексирования цветов может формировать менее грубую заливку по сравнению с режимом RGBA.</span><span class="sxs-lookup"><span data-stu-id="ca385-110">If you have a limited number of bitplanes available; the color-index mode can produce less-coarse shading than the RGBA mode.</span></span>
-   <span data-ttu-id="ca385-111">Если вы не беспокоитесь об использовании "реальных" цветов; Например, использование нескольких цветов в карте топографик для обозначения относительных прав.</span><span class="sxs-lookup"><span data-stu-id="ca385-111">If you are not concerned about using "real" colors; for example, using several colors in a topographic map to designate relative elevations.</span></span>
-   <span data-ttu-id="ca385-112">При переносе существующего приложения, в котором используется режим индексирования цветов, существенно.</span><span class="sxs-lookup"><span data-stu-id="ca385-112">When you're porting an existing application that uses color-index mode extensively.</span></span>
-   <span data-ttu-id="ca385-113">Если вы хотите использовать в приложении анимацию и эффекты цветовой схемы.</span><span class="sxs-lookup"><span data-stu-id="ca385-113">When you want to use color-map animation and effects in your application.</span></span> <span data-ttu-id="ca385-114">(Это невозможно на устройствах с true цветами.)</span><span class="sxs-lookup"><span data-stu-id="ca385-114">(This is not possible on true-color devices.)</span></span>

 

 




