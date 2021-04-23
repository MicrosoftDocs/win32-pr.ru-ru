---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, фрагменты
- Конвейер обработки OpenGL, фрагменты
- фрагменты OpenGL
- фрамебуфферс, фрагменты, изменяющие Пиксели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672099"
---
# <a name="fragments"></a><span data-ttu-id="4fc0a-107">Fragments</span><span class="sxs-lookup"><span data-stu-id="4fc0a-107">Fragments</span></span>

<span data-ttu-id="4fc0a-108">Фрагмент, созданный путем растрирования, изменяет соответствующий пиксель в буфера кадров только в том случае, если он проходит следующие тесты:</span><span class="sxs-lookup"><span data-stu-id="4fc0a-108">A fragment produced by rasterization modifies the corresponding pixel in the framebuffer only if it passes the following tests:</span></span>

-   [<span data-ttu-id="4fc0a-109">Тестирование владения пикселями</span><span class="sxs-lookup"><span data-stu-id="4fc0a-109">Pixel ownership test</span></span>](pixel-ownership-test.md)
-   [<span data-ttu-id="4fc0a-110">Ножницное тестирование</span><span class="sxs-lookup"><span data-stu-id="4fc0a-110">Scissor test</span></span>](scissor-test.md)
-   [<span data-ttu-id="4fc0a-111">Альфа-тест</span><span class="sxs-lookup"><span data-stu-id="4fc0a-111">Alpha test</span></span>](alpha-test.md)
-   [<span data-ttu-id="4fc0a-112">Тест набора элементов</span><span class="sxs-lookup"><span data-stu-id="4fc0a-112">Stencil test</span></span>](stencil-test.md)
-   [<span data-ttu-id="4fc0a-113">Тест буфера глубины</span><span class="sxs-lookup"><span data-stu-id="4fc0a-113">Depth-buffer test</span></span>](depth-buffer-test.md)

<span data-ttu-id="4fc0a-114">При передаче данные фрагмента могут заменить существующие значения буфера кадров или объединить его с существующими данными в буфера кадров в зависимости от состояния определенных режимов.</span><span class="sxs-lookup"><span data-stu-id="4fc0a-114">If it passes, the fragment's data can replace the existing framebuffer values, or you can combine it with existing data in the framebuffer, depending on the state of certain modes.</span></span> <span data-ttu-id="4fc0a-115">Фрагмент можно объединить с данными в буфера кадров, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4fc0a-115">You can combine the fragment with data in the framebuffer by:</span></span>

-   [<span data-ttu-id="4fc0a-116">Смешения</span><span class="sxs-lookup"><span data-stu-id="4fc0a-116">Blending</span></span>](blending.md)
-   [<span data-ttu-id="4fc0a-117">Сглаживания</span><span class="sxs-lookup"><span data-stu-id="4fc0a-117">Dithering</span></span>](dithering.md)
-   [<span data-ttu-id="4fc0a-118">Логические операции</span><span class="sxs-lookup"><span data-stu-id="4fc0a-118">Logical operations</span></span>](logical-operations.md)

 

 




