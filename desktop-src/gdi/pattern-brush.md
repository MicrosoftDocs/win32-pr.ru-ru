---
description: Шаблон (или пользовательская) кисть создается из определяемого приложением точечного рисунка или аппаратно-независимого точечного рисунка (DIB). Следующие прямоугольники были окрашены с использованием различных узорных кистей.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Узорная кисть
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987920"
---
# <a name="pattern-brush"></a><span data-ttu-id="bfb61-104">Узорная кисть</span><span class="sxs-lookup"><span data-stu-id="bfb61-104">Pattern Brush</span></span>

<span data-ttu-id="bfb61-105">Шаблон (или пользовательская) кисть создается из определяемого приложением точечного рисунка или аппаратно-независимого точечного рисунка (DIB).</span><span class="sxs-lookup"><span data-stu-id="bfb61-105">A pattern (or custom) brush is created from an application-defined bitmap or device-independent bitmap (DIB).</span></span> <span data-ttu-id="bfb61-106">Следующие прямоугольники были окрашены с использованием различных узорных кистей.</span><span class="sxs-lookup"><span data-stu-id="bfb61-106">The following rectangles were painted by using different pattern brushes.</span></span>

![Иллюстрация, в которой показаны три поля, каждый из которых заполняется другим шаблоном](images/csbru-05.png)

<span data-ttu-id="bfb61-108">Чтобы создать логическую кисть-шаблон, приложение должно сначала создать точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="bfb61-108">To create a logical pattern brush, an application must first create a bitmap.</span></span> <span data-ttu-id="bfb61-109">После создания точечного рисунка приложение может создать логическую узорную кисть, вызвав функцию [**креатепаттернбруш**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) или [**креатедибпаттернбрушпт**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , указав дескриптор, определяющий точечный рисунок (или DIB).</span><span class="sxs-lookup"><span data-stu-id="bfb61-109">After creating the bitmap, the application can create the logical pattern brush by calling the [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) or [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) function, supplying a handle that identifies the bitmap (or DIB).</span></span> <span data-ttu-id="bfb61-110">Кисти, показанные на предыдущем рисунке, были созданы из монохромных растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="bfb61-110">The brushes that appear in the preceding illustration were created from monochrome bitmaps.</span></span> <span data-ttu-id="bfb61-111">Описание точечных рисунков, рисунков DIB и функций, которые их создают, см. в разделе [точечные рисунки](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="bfb61-111">For a description of bitmaps, DIBs, and the functions that create them, see [Bitmaps](bitmaps.md).</span></span>

 

 



