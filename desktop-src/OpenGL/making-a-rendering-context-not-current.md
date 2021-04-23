---
title: Неактуальный контекст подготовки к просмотру
description: Чтобы отсоединить контекст подготовки к просмотру от потока, сделайте его неактуальным. Это можно сделать, вызвав функцию Вглмакекуррент с параметрами, для которых задано значение NULL. Ниже приведен пример этой простой задачи.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL в Windows, контексты отрисовки
- Контексты отрисовки OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329512"
---
# <a name="making-a-rendering-context-not-current"></a><span data-ttu-id="aaab5-107">Неактуальный контекст подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="aaab5-107">Making a Rendering Context Not Current</span></span>

<span data-ttu-id="aaab5-108">Чтобы отсоединить контекст подготовки к просмотру от потока, сделайте его неактуальным.</span><span class="sxs-lookup"><span data-stu-id="aaab5-108">To detach a rendering context from a thread, make it not current.</span></span> <span data-ttu-id="aaab5-109">Это можно сделать, вызвав функцию [**вглмакекуррент**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) с параметрами, для которых задано **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="aaab5-109">You can do this by calling the [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) function with the parameters set to **NULL**.</span></span> <span data-ttu-id="aaab5-110">Ниже приведен пример этой простой задачи.</span><span class="sxs-lookup"><span data-stu-id="aaab5-110">The following is a sample of this simple task.</span></span>

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




