---
title: Использование объектов тесселяции
description: При описании и тесселяции сложного многоугольника требуются связанные данные, такие как вершины, грани и функции обратного вызова.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Служебная программа OpenGL (GLU), объекты тесселяции
- GLU (служебная программа OpenGL), объекты тесселяции
- объекты тесселяции OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329195"
---
# <a name="using-tessellation-objects"></a><span data-ttu-id="b6bc7-106">Использование объектов тесселяции</span><span class="sxs-lookup"><span data-stu-id="b6bc7-106">Using Tessellation Objects</span></span>

<span data-ttu-id="b6bc7-107">При описании и тесселяции сложного многоугольника требуются связанные данные, такие как вершины, грани и функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-107">As a complex polygon is being described and tessellated, it requires associated data, such as the vertices, edges, and callback functions.</span></span> <span data-ttu-id="b6bc7-108">Все эти данные связаны с одним объектом тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-108">All this data is tied to a single tessellation object.</span></span> <span data-ttu-id="b6bc7-109">Для тесселяции многоугольника сначала используется функция [**глуневтесс**](glunewtess.md) , которая создает новый объект тесселяции и возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-109">To tessellate a polygon, you first use the [**gluNewTess**](glunewtess.md) function which creates a new tessellation object and returns a pointer to it.</span></span> <span data-ttu-id="b6bc7-110">Если функция завершается ошибкой, возвращается пустой указатель.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-110">A null pointer is returned if the function fails.</span></span>

<span data-ttu-id="b6bc7-111">Если объект тесселяции больше не нужен, его можно удалить и освободить всю связанную память с помощью [**глуделететесс**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="b6bc7-111">If you no longer need a tessellation object, you can delete it and free all associated memory with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="b6bc7-112">Можно повторно использовать один объект тесселяции для всех тесселяций.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-112">You can reuse a single tessellation object for all your tessellations.</span></span> <span data-ttu-id="b6bc7-113">Этот объект необходим только потому, что библиотечным функциям может потребоваться делать собственные тесселяции, и они должны иметь возможность сделать это, не мешая тесселяции, выполняемой программой.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-113">This object is required only because library functions may need to do their own tessellations, and they should be able to do so without interfering with any tessellation that your program is performing.</span></span> <span data-ttu-id="b6bc7-114">Несколько объектов тесселяции также полезны, если требуется использовать разные наборы обратных вызовов для различных тесселяций.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-114">Multiple tessellation objects are also useful if you want to use different sets of callbacks for different tessellations.</span></span> <span data-ttu-id="b6bc7-115">Однако обычно выделяется один объект тесселяции и используется для всех тесселяций.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-115">Typically, however, you allocate a single tessellation object and use it for all the tessellations.</span></span> <span data-ttu-id="b6bc7-116">Не нужно освобождать его, так как в нем используется небольшой объем памяти.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-116">There's no real need to free it, because it uses a small amount of memory.</span></span> <span data-ttu-id="b6bc7-117">С другой стороны, при написании библиотечной функции, использующей тесселяцию GLU, будьте внимательны, чтобы освободить все создаваемые объекты тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b6bc7-117">On the other hand, if you're writing a library function that uses GLU tessellation, be careful to free any tessellation objects you create.</span></span>

 

 




