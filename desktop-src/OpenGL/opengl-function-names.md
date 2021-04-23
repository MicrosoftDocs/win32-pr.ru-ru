---
title: Имена функций OpenGL
description: Многие функции OpenGL — это разновидности друг друга, которые отличаются главными типами данных их аргументов.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, имена функций
- имена функций OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776142"
---
# <a name="opengl-function-names"></a><span data-ttu-id="fd222-105">Имена функций OpenGL</span><span class="sxs-lookup"><span data-stu-id="fd222-105">OpenGL Function Names</span></span>

<span data-ttu-id="fd222-106">Многие функции OpenGL — это разновидности друг друга, которые отличаются главными типами данных их аргументов.</span><span class="sxs-lookup"><span data-stu-id="fd222-106">Many OpenGL functions are variations of each other, differing mostly in the data types of their arguments.</span></span> <span data-ttu-id="fd222-107">Некоторые функции имеют разное число связанных аргументов и могут ли эти аргументы быть заданы в качестве вектора или должны быть указаны отдельно в списке.</span><span class="sxs-lookup"><span data-stu-id="fd222-107">Some functions differ in the number of related arguments and whether those arguments can be specified as a vector or must be specified separately in a list.</span></span> <span data-ttu-id="fd222-108">Например, при использовании функции **glVertex2f** необходимо указать координаты x и y как 32-разрядные числа с плавающей запятой. При использовании **glVertex3sv** необходимо предоставить массив из трех коротких (16-разрядных) целочисленных значений для x, y и z.</span><span class="sxs-lookup"><span data-stu-id="fd222-108">For example, if you use the **glVertex2f** function, you need to supply x- and y-coordinates as 32-bit floating-point numbers; with **glVertex3sv**, you must supply an array of three short (16-bit) integer values for x, y, and z.</span></span> <span data-ttu-id="fd222-109">В следующих разделах используется только базовое имя функции.</span><span class="sxs-lookup"><span data-stu-id="fd222-109">Only the base name of the function is used in the topics that follow.</span></span> <span data-ttu-id="fd222-110">Звездочка означает, что фактическое имя функции может быть больше, чем показано.</span><span class="sxs-lookup"><span data-stu-id="fd222-110">An asterisk indicates that there may be more to the actual function name than is shown.</span></span> <span data-ttu-id="fd222-111">Например, [глвертекс \*](glvertex-functions.md) означает все варианты функции, которую вы используете для указания вершин: **glVertex2d**, **glVertex2f**, **glVertex2i** и т. д.</span><span class="sxs-lookup"><span data-stu-id="fd222-111">For example, [glVertex\*](glvertex-functions.md) stands for all the variations of the function you use to specify vertices: **glVertex2d**, **glVertex2f**, **glVertex2i**, and so on.</span></span>

<span data-ttu-id="fd222-112">Результат функции OpenGL может изменяться в зависимости от того, включены ли определенные режимы.</span><span class="sxs-lookup"><span data-stu-id="fd222-112">The effect of an OpenGL function can vary depending on whether certain modes are enabled.</span></span> <span data-ttu-id="fd222-113">Например, необходимо включить освещение, если функции, связанные с освещением, должны создавать объект с надлежащим светом.</span><span class="sxs-lookup"><span data-stu-id="fd222-113">For example, you need to enable lighting if the lighting-related functions are to produce a properly lit object.</span></span> <span data-ttu-id="fd222-114">Чтобы включить определенный режим, используйте функцию [**гленабле**](glenable.md) и укажите соответствующую константу для указания режима (например, « \_ освещение»).</span><span class="sxs-lookup"><span data-stu-id="fd222-114">To enable a particular mode, use the [**glEnable**](glenable.md) function and supply the appropriate constant to identify the mode (for example, GL\_LIGHTING).</span></span> <span data-ttu-id="fd222-115">Чтобы отключить режим, используйте [**глдисабле**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="fd222-115">To disable a mode, use [**glDisable**](gldisable.md).</span></span> <span data-ttu-id="fd222-116">Полный список режимов, которые можно включить, см. в разделе **гленабле** .</span><span class="sxs-lookup"><span data-stu-id="fd222-116">See **glEnable** for a complete list of the modes that can be enabled.</span></span>

 

 




