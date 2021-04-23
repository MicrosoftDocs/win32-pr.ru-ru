---
title: Перекрытых
description: Фрагменты преобразуются в Пиксели в буфера кадров.
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL, ПКС
- Конвейер обработки OpenGL, Пиксели
- пикселы OpenGL
- фрамебуфферс, преобразование фрагментов в Пиксели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6660452930683943da780fad3aeb001e531711
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411374"
---
# <a name="pixels"></a><span data-ttu-id="6f38c-107">Перекрытых</span><span class="sxs-lookup"><span data-stu-id="6f38c-107">Pixels</span></span>

<span data-ttu-id="6f38c-108">Фрагменты преобразуются в Пиксели в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="6f38c-108">Fragments are converted to pixels in the framebuffer.</span></span> <span data-ttu-id="6f38c-109">Буфера кадров организован в набор логических буферов, которые представляют собой цвет, глубину, трафарет и буферы накопления.</span><span class="sxs-lookup"><span data-stu-id="6f38c-109">The framebuffer is organized into a set of logical buffers the color, depth, stencil, and accumulation buffers.</span></span> <span data-ttu-id="6f38c-110">Цветовой буфер сам по себе состоит из передних левый, передних прав, заднего левого, заднего право и некоторое количество вспомогательных буферов.</span><span class="sxs-lookup"><span data-stu-id="6f38c-110">The color buffer itself consists of a front left, front right, back left, back right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="6f38c-111">Вы можете выдавать функции для управления этими буферами и напрямую считывать или копировать пиксели из них.</span><span class="sxs-lookup"><span data-stu-id="6f38c-111">You can issue functions to control these buffers, and directly read or copy pixels from them.</span></span> <span data-ttu-id="6f38c-112">(Обратите внимание, что конкретный контекст OpenGL, который вы используете, может не предоставлять все эти буферы.)</span><span class="sxs-lookup"><span data-stu-id="6f38c-112">(Note that the particular OpenGL context you're using may not provide all these buffers.)</span></span>

-   [<span data-ttu-id="6f38c-113">Операции буфера кадров</span><span class="sxs-lookup"><span data-stu-id="6f38c-113">Framebuffer Operations</span></span>](framebuffer-operations.md)
-   [<span data-ttu-id="6f38c-114">Чтение или копирование пикселей</span><span class="sxs-lookup"><span data-stu-id="6f38c-114">Reading or Copying Pixels</span></span>](reading-or-copying-pixels.md)
-   [<span data-ttu-id="6f38c-115">Ссылки на Пиксели</span><span class="sxs-lookup"><span data-stu-id="6f38c-115">Pixels Reference</span></span>](pixels-reference.md)

 

 




