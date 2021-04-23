---
description: Следующие функции используются для создания, изменения или рисования контуров.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Функции пути (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984884"
---
# <a name="path-functions-windows-gdi"></a><span data-ttu-id="5f8ad-103">Функции пути (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="5f8ad-103">Path Functions (Windows GDI)</span></span>

<span data-ttu-id="5f8ad-104">Следующие функции используются для создания, изменения или рисования контуров.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-104">The following functions are used to create, alter, or draw paths.</span></span>



| <span data-ttu-id="5f8ad-105">Функция</span><span class="sxs-lookup"><span data-stu-id="5f8ad-105">Function</span></span>                                       | <span data-ttu-id="5f8ad-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5f8ad-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f8ad-107">**абортпас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-107">**AbortPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | <span data-ttu-id="5f8ad-108">Закрывает и удаляет все пути в указанном контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-108">Closes and discards any paths in the specified device context.</span></span>                                                                                                   |
| [<span data-ttu-id="5f8ad-109">**бегинпас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-109">**BeginPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | <span data-ttu-id="5f8ad-110">Открывает скобку пути в указанном контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-110">Opens a path bracket in the specified device context.</span></span>                                                                                                            |
| [<span data-ttu-id="5f8ad-111">**клосефигуре**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-111">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | <span data-ttu-id="5f8ad-112">Закрывает открытую фигуру в контуре.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-112">Closes an open figure in a path.</span></span>                                                                                                                                 |
| [<span data-ttu-id="5f8ad-113">**ендпас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-113">**EndPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | <span data-ttu-id="5f8ad-114">Закрывает скобку пути и выбирает путь, определенный скобкой, в указанный контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-114">Closes a path bracket and selects the path defined by the bracket into the specified device context.</span></span>                                                             |
| [<span data-ttu-id="5f8ad-115">**филлпас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-115">**FillPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | <span data-ttu-id="5f8ad-116">Закрывает все открытые фигуры в текущем контуре и заполняет внутреннюю часть пути, используя текущую кисть и режим заливки многоугольников.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-116">Closes any open figures in the current path and fills the path's interior by using the current brush and polygon-filling mode.</span></span>                                   |
| [<span data-ttu-id="5f8ad-117">**флаттенпас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-117">**FlattenPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | <span data-ttu-id="5f8ad-118">Преобразует все кривые в пути, выбранном в текущем контексте устройства (DC), преобразуя каждую кривую в последовательность линий.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-118">Transforms any curves in the path that is selected into the current device context (DC), turning each curve into a sequence of lines.</span></span>                            |
| [<span data-ttu-id="5f8ad-119">**жетмитерлимит**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-119">**GetMiterLimit**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | <span data-ttu-id="5f8ad-120">Возвращает предел среза для указанного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-120">Retrieves the miter limit for the specified device context.</span></span>                                                                                                      |
| [<span data-ttu-id="5f8ad-121">**GetPath**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-121">**GetPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | <span data-ttu-id="5f8ad-122">Получает координаты, определяющие конечные точки линий и контрольные точки кривых, найденные по пути, выбранному в заданном контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-122">Retrieves the coordinates defining the endpoints of lines and the control points of curves found in the path that is selected into the specified device context.</span></span> |
| [<span data-ttu-id="5f8ad-123">**пасторегион**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-123">**PathToRegion**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | <span data-ttu-id="5f8ad-124">Создает регион из пути, выбранного в заданном контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-124">Creates a region from the path that is selected into the specified device context.</span></span>                                                                               |
| [<span data-ttu-id="5f8ad-125">**сетмитерлимит**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-125">**SetMiterLimit**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | <span data-ttu-id="5f8ad-126">Задает ограничение длины угловых соединений для указанного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-126">Sets the limit for the length of miter joins for the specified device context.</span></span>                                                                                   |
| [<span data-ttu-id="5f8ad-127">**строкеандфиллпас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-127">**StrokeAndFillPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | <span data-ttu-id="5f8ad-128">Закрывает все открытые фигуры в контуре, обводки контура с помощью текущего пера и заполняет внутреннюю часть с помощью текущей кисти.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-128">Closes any open figures in a path, strokes the outline of the path by using the current pen, and fills its interior by using the current brush.</span></span>                  |
| [<span data-ttu-id="5f8ad-129">**строкепас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-129">**StrokePath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | <span data-ttu-id="5f8ad-130">Отображает указанный путь с помощью текущего пера.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-130">Renders the specified path by using the current pen.</span></span>                                                                                                             |
| [<span data-ttu-id="5f8ad-131">**виденпас**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-131">**WidenPath**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | <span data-ttu-id="5f8ad-132">Переопределяет текущий путь как область, которая будет окрашена, если контур был штриховым с помощью пера, выбранного в данный момент в данном контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-132">Redefines the current path as the area that would be painted if the path were stroked using the pen currently selected into the given device context.</span></span>            |



 

 

 



