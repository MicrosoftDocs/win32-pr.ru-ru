---
title: Расширение функций OpenGL
description: Библиотека OpenGL поддерживает несколько реализаций своих функций.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL в Windows, функции расширения
- функции расширения OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986738"
---
# <a name="extending-opengl-functions"></a><span data-ttu-id="41921-105">Расширение функций OpenGL</span><span class="sxs-lookup"><span data-stu-id="41921-105">Extending OpenGL Functions</span></span>

<span data-ttu-id="41921-106">Библиотека OpenGL поддерживает несколько реализаций своих функций.</span><span class="sxs-lookup"><span data-stu-id="41921-106">The OpenGL library supports multiple implementations of its functions.</span></span> <span data-ttu-id="41921-107">Функции расширения, поддерживаемые в одном контексте отрисовки, не обязательно поддерживаются в другом контексте отрисовки.</span><span class="sxs-lookup"><span data-stu-id="41921-107">Extension functions supported in one rendering context aren't necessarily supported in a different rendering context.</span></span> <span data-ttu-id="41921-108">Для данного контекста отрисовки в приложении, использующем функции расширения, используйте только адреса функций, возвращенные функцией [**вглжетпрокаддресс**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="41921-108">For a given rendering context in an application using extension functions, use only the function addresses returned by the [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) function.</span></span>

 

 




