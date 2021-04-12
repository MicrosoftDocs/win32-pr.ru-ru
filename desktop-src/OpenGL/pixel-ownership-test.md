---
title: Тестирование владения пикселями
description: Проверка владения пикселом определяет, владеет ли текущий контекст OpenGL пикселом в буфера кадров, соответствующим определенному фрагменту.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Конвейер обработки OpenGL, проверка владения пикселями
- Проверка владения пиксельным OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330592"
---
# <a name="pixel-ownership-test"></a><span data-ttu-id="7edcc-105">Тестирование владения пикселями</span><span class="sxs-lookup"><span data-stu-id="7edcc-105">Pixel Ownership Test</span></span>

<span data-ttu-id="7edcc-106">Проверка владения пикселом определяет, владеет ли текущий контекст OpenGL пикселом в буфера кадров, соответствующим определенному фрагменту.</span><span class="sxs-lookup"><span data-stu-id="7edcc-106">The pixel ownership test determines whether the current OpenGL context owns the pixel in the framebuffer corresponding to a particular fragment.</span></span> <span data-ttu-id="7edcc-107">Если это так, фрагмент переходит к следующему тесту.</span><span class="sxs-lookup"><span data-stu-id="7edcc-107">If so, the fragment proceeds to the next test.</span></span> <span data-ttu-id="7edcc-108">В противном случае система Window определяет, отбрасывается ли фрагмент или выполняются ли дальнейшие операции с этим фрагментом.</span><span class="sxs-lookup"><span data-stu-id="7edcc-108">If not, the window system determines whether the fragment is discarded or whether any further fragment operations will be performed with that fragment.</span></span> <span data-ttu-id="7edcc-109">В этом тесте окно системы управляет поведением, например, если окно OpenGL скрыто.</span><span class="sxs-lookup"><span data-stu-id="7edcc-109">With this test, the window system controls behavior when, for example, an OpenGL window is obscured.</span></span>

 

 




