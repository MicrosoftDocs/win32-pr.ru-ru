---
description: Windows поддерживает пять графических режимов, позволяющих приложению указать, как смешиваются цвета, где отображаются выходные данные, как будут масштабироваться выходные данные и т. д. Эти режимы, которые хранятся в контроллере домена, описаны в следующей таблице.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Графические режимы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544482"
---
# <a name="graphic-modes"></a><span data-ttu-id="41b1e-104">Графические режимы</span><span class="sxs-lookup"><span data-stu-id="41b1e-104">Graphic Modes</span></span>

<span data-ttu-id="41b1e-105">Windows поддерживает пять графических режимов, позволяющих приложению указать, как смешиваются цвета, где отображаются выходные данные, как будут масштабироваться выходные данные и т. д.</span><span class="sxs-lookup"><span data-stu-id="41b1e-105">Windows supports five graphic modes that allow an application to specify how colors are mixed, where output appears, how the output is scaled, and so on.</span></span> <span data-ttu-id="41b1e-106">Эти режимы, которые хранятся в контроллере домена, описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="41b1e-106">These modes, which are stored in a DC, are described in the following table.</span></span>



| <span data-ttu-id="41b1e-107">Графический режим</span><span class="sxs-lookup"><span data-stu-id="41b1e-107">Graphics mode</span></span> | <span data-ttu-id="41b1e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="41b1e-108">Description</span></span>                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b1e-109">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="41b1e-109">Background</span></span>    | <span data-ttu-id="41b1e-110">Определяет, как цвета фона смешиваются с существующими окнами или экранными цветами для операций с растровыми и текстовыми изображениями.</span><span class="sxs-lookup"><span data-stu-id="41b1e-110">Defines how background colors are mixed with existing window or screen colors for bitmap and text operations.</span></span>              |
| <span data-ttu-id="41b1e-111">Рисование</span><span class="sxs-lookup"><span data-stu-id="41b1e-111">Drawing</span></span>       | <span data-ttu-id="41b1e-112">Определяет, как цвета переднего плана смешиваются с существующими окнами или экранными цветами для операций пером, кисти, точечного рисунка и текста.</span><span class="sxs-lookup"><span data-stu-id="41b1e-112">Defines how foreground colors are mixed with existing window or screen colors for pen, brush, bitmap, and text operations.</span></span> |
| <span data-ttu-id="41b1e-113">Сопоставление</span><span class="sxs-lookup"><span data-stu-id="41b1e-113">Mapping</span></span>       | <span data-ttu-id="41b1e-114">Определяет, каким способом графические выходные данные сопоставлены из логического (или мира) пространства на бумаге окна, экрана или принтера.</span><span class="sxs-lookup"><span data-stu-id="41b1e-114">Defines how graphics output is mapped from logical (or world) space onto the window, screen, or printer paper.</span></span>             |
| <span data-ttu-id="41b1e-115">Многоугольник-заливка</span><span class="sxs-lookup"><span data-stu-id="41b1e-115">Polygon-fill</span></span>  | <span data-ttu-id="41b1e-116">Определяет, как шаблон кисти используется для заполнения внутренней части сложных областей.</span><span class="sxs-lookup"><span data-stu-id="41b1e-116">Defines how the brush pattern is used to fill the interior of complex regions.</span></span>                                             |
| <span data-ttu-id="41b1e-117">Тягивает</span><span class="sxs-lookup"><span data-stu-id="41b1e-117">Stretching</span></span>    | <span data-ttu-id="41b1e-118">Определяет, как цвета точечных рисунков смешиваются с существующими окнами или экранными цветами при сжатии растрового изображения (или при уменьшении масштаба).</span><span class="sxs-lookup"><span data-stu-id="41b1e-118">Defines how bitmap colors are mixed with existing window or screen colors when the bitmap is compressed (or scaled down).</span></span>  |



 

<span data-ttu-id="41b1e-119">Как и при работе с графическими объектами, система инициализирует контроллер домена с графическими режимами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41b1e-119">As it does with graphic objects, the system initializes a DC with default graphic modes.</span></span> <span data-ttu-id="41b1e-120">Приложение может извлекать и исследовать эти режимы по умолчанию, вызывая следующие функции.</span><span class="sxs-lookup"><span data-stu-id="41b1e-120">An application can retrieve and examine these default modes by calling the following functions.</span></span>



| <span data-ttu-id="41b1e-121">Графический режим</span><span class="sxs-lookup"><span data-stu-id="41b1e-121">Graphics mode</span></span> | <span data-ttu-id="41b1e-122">Функция</span><span class="sxs-lookup"><span data-stu-id="41b1e-122">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="41b1e-123">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="41b1e-123">Background</span></span>    | [<span data-ttu-id="41b1e-124">**жетбкмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-124">**GetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| <span data-ttu-id="41b1e-125">Рисование</span><span class="sxs-lookup"><span data-stu-id="41b1e-125">Drawing</span></span>       | [<span data-ttu-id="41b1e-126">**GetROP2**</span><span class="sxs-lookup"><span data-stu-id="41b1e-126">**GetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| <span data-ttu-id="41b1e-127">Сопоставление</span><span class="sxs-lookup"><span data-stu-id="41b1e-127">Mapping</span></span>       | [<span data-ttu-id="41b1e-128">**жетмапмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-128">**GetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| <span data-ttu-id="41b1e-129">Многоугольник-заливка</span><span class="sxs-lookup"><span data-stu-id="41b1e-129">Polygon-fill</span></span>  | [<span data-ttu-id="41b1e-130">**жетполифиллмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-130">**GetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| <span data-ttu-id="41b1e-131">Тягивает</span><span class="sxs-lookup"><span data-stu-id="41b1e-131">Stretching</span></span>    | [<span data-ttu-id="41b1e-132">**жетстретчблтмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-132">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

<span data-ttu-id="41b1e-133">Приложение может изменить режимы по умолчанию, вызвав одну из следующих функций.</span><span class="sxs-lookup"><span data-stu-id="41b1e-133">An application can change the default modes by calling one of the following functions.</span></span>



| <span data-ttu-id="41b1e-134">Графический режим</span><span class="sxs-lookup"><span data-stu-id="41b1e-134">Graphics mode</span></span> | <span data-ttu-id="41b1e-135">Функция</span><span class="sxs-lookup"><span data-stu-id="41b1e-135">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="41b1e-136">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="41b1e-136">Background</span></span>    | [<span data-ttu-id="41b1e-137">**сетбкмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-137">**SetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| <span data-ttu-id="41b1e-138">Рисование</span><span class="sxs-lookup"><span data-stu-id="41b1e-138">Drawing</span></span>       | [<span data-ttu-id="41b1e-139">**SetROP2**</span><span class="sxs-lookup"><span data-stu-id="41b1e-139">**SetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| <span data-ttu-id="41b1e-140">Сопоставление</span><span class="sxs-lookup"><span data-stu-id="41b1e-140">Mapping</span></span>       | [<span data-ttu-id="41b1e-141">**сетмапмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-141">**SetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| <span data-ttu-id="41b1e-142">Многоугольник-заливка</span><span class="sxs-lookup"><span data-stu-id="41b1e-142">Polygon-fill</span></span>  | [<span data-ttu-id="41b1e-143">**сетполифиллмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-143">**SetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| <span data-ttu-id="41b1e-144">Тягивает</span><span class="sxs-lookup"><span data-stu-id="41b1e-144">Stretching</span></span>    | [<span data-ttu-id="41b1e-145">**сетстретчблтмоде**</span><span class="sxs-lookup"><span data-stu-id="41b1e-145">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



