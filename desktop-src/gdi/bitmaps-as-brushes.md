---
description: Ряд функций использует выбранную кисть в контексте устройства для выполнения операций точечного рисунка.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Растровые изображения как кисти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263694"
---
# <a name="bitmaps-as-brushes"></a><span data-ttu-id="8a820-103">Растровые изображения как кисти</span><span class="sxs-lookup"><span data-stu-id="8a820-103">Bitmaps as Brushes</span></span>

<span data-ttu-id="8a820-104">Ряд функций использует выбранную кисть в контексте устройства для выполнения операций точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="8a820-104">A number of functions use the brush currently selected into a device context to perform bitmap operations.</span></span> <span data-ttu-id="8a820-105">Например, функция [**патблт**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) реплицирует кисть в прямоугольной области внутри окна, а функция [**флудфилл**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) реплицирует кисть внутри области окна, ограниченного указанным цветом (в отличие от **патблт**, **флудфилл** заполняет непрямоугольные фигуры).</span><span class="sxs-lookup"><span data-stu-id="8a820-105">For example, the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function replicates the brush in a rectangular region within a window, and the [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush inside an area in a window bounded by the specified color (unlike **PatBlt**, **FloodFill** does fill nonrectangular shapes).</span></span>

<span data-ttu-id="8a820-106">Функция [**флудфилл**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) реплицирует кисть в пределах региона, ограниченного указанным цветом.</span><span class="sxs-lookup"><span data-stu-id="8a820-106">The [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush within a region bounded by a specified color.</span></span> <span data-ttu-id="8a820-107">Однако, в отличие от функции [**патблт**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , **флудфилл** не объединяет данные цвета кисти с цветовыми данными для пикселов на дисплее; Он просто задает цвет всех пикселов внутри области, отображаемой цветом кисти, выбранной в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="8a820-107">However, unlike the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function, **FloodFill** does not combine the color data for the brush with the color data for the pixels on the display; it simply sets the color of all pixels within the enclosed region on the display to the color of the brush that is currently selected into the device context.</span></span>

 

 



