---
title: Библиотека служебной программы OpenGL
description: Библиотека служебной программы OpenGL
ms.assetid: 54a7cdce-b38d-416a-a59d-827b6fb76b47
keywords:
- OpenGL, служебная программа OpenGL (GLU)
- Служебная программа OpenGL (GLU)
- GLU библиотека OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d40d4a6fa51354204ee37bfc43e9217b742b882
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888383"
---
# <a name="opengl-utility-library"></a><span data-ttu-id="58523-106">Библиотека служебной программы OpenGL</span><span class="sxs-lookup"><span data-stu-id="58523-106">OpenGL Utility Library</span></span>

<span data-ttu-id="58523-107">Библиотека служебной программы OpenGL (GLU) содержит несколько групп функций, дополняющих основной интерфейс OpenGL, обеспечивая поддержку дополнительных функций.</span><span class="sxs-lookup"><span data-stu-id="58523-107">The OpenGL Utility (GLU) library contains several groups of functions that complement the core OpenGL interface by providing support for auxiliary features.</span></span> <span data-ttu-id="58523-108">Эти служебные функции используют основные функции OpenGL, поэтому любая реализация OpenGL гарантирует поддержку служебных функций.</span><span class="sxs-lookup"><span data-stu-id="58523-108">These utility functions make use of core OpenGL functions, so any OpenGL implementation is guaranteed to support the utility functions.</span></span>

> [!Note]  
> <span data-ttu-id="58523-109">Префикс для функций библиотеки служебной программы — «Glu», а не «GL».</span><span class="sxs-lookup"><span data-stu-id="58523-109">The prefix for Utility library functions is "glu" rather than "gl."</span></span>

 

<span data-ttu-id="58523-110">Многие из этих функций описаны в предыдущих разделах документации по по мере возникновения таких разделов.</span><span class="sxs-lookup"><span data-stu-id="58523-110">Many of these functions are described in preceding sections of the documenation as their topics arise.</span></span> <span data-ttu-id="58523-111">Эти функции перечислены здесь для полноты.</span><span class="sxs-lookup"><span data-stu-id="58523-111">These functions are listed here for completeness.</span></span> <span data-ttu-id="58523-112">GLU функции, которые не обсуждаются в предыдущих разделах, описаны здесь.</span><span class="sxs-lookup"><span data-stu-id="58523-112">GLU functions that aren't discussed in preceding sections are described here.</span></span> <span data-ttu-id="58523-113">Более подробное описание этих функций см. в *справочном руководстве по OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="58523-113">For more detailed descriptions of these functions, see the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="58523-114">В этом разделе группируются связанные функции GLU следующим образом:</span><span class="sxs-lookup"><span data-stu-id="58523-114">This section groups related GLU functions, as follows:</span></span>

-   [<span data-ttu-id="58523-115">Инициализации</span><span class="sxs-lookup"><span data-stu-id="58523-115">Initializing</span></span>](initializing.md)
-   [<span data-ttu-id="58523-116">Обработка изображений для использования в текстурировании</span><span class="sxs-lookup"><span data-stu-id="58523-116">Manipulating Images for Use in Texturing</span></span>](manipulating-images-for-use-in-texturing.md)
-   [<span data-ttu-id="58523-117">Преобразование координат</span><span class="sxs-lookup"><span data-stu-id="58523-117">Transforming Coordinates</span></span>](transforming-coordinates.md)
-   [<span data-ttu-id="58523-118">Тесселяция многоугольников</span><span class="sxs-lookup"><span data-stu-id="58523-118">Tessellating Polygons</span></span>](tessellating-polygons.md)
-   [<span data-ttu-id="58523-119">Использование функций обратного вызова</span><span class="sxs-lookup"><span data-stu-id="58523-119">Using Callback Functions</span></span>](using-callback-functions.md)
-   [<span data-ttu-id="58523-120">Использование объектов тесселяции</span><span class="sxs-lookup"><span data-stu-id="58523-120">Using Tessellation Objects</span></span>](using-tessellation-objects.md)
-   [<span data-ttu-id="58523-121">Указание обратных вызовов</span><span class="sxs-lookup"><span data-stu-id="58523-121">Specifying Callbacks</span></span>](specifying-callbacks.md)
-   [<span data-ttu-id="58523-122">Указание многоугольника для тесселяции</span><span class="sxs-lookup"><span data-stu-id="58523-122">Specifying the Polygon to Be Tessellated</span></span>](specifying-the-polygon-to-be-tessellated.md)
-   [<span data-ttu-id="58523-123">Отрисовка простых поверхностей</span><span class="sxs-lookup"><span data-stu-id="58523-123">Rendering Simple Surfaces</span></span>](rendering-simple-surfaces.md)
-   [<span data-ttu-id="58523-124">Использование кривых и поверхностей НУРБС</span><span class="sxs-lookup"><span data-stu-id="58523-124">Using NURBS Curves and Surfaces</span></span>](using-nurbs-curves-and-surfaces.md)
-   [<span data-ttu-id="58523-125">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="58523-125">Handling Errors</span></span>](handling-errors.md)

 

 




