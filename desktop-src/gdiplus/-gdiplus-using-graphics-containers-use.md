---
description: Графический объект предоставляет такие методы, как DrawLine, DrawImage и DrawString для отображения векторных изображений, растровых изображений и текста.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Использование графических контейнеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985113"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="2a099-103">Использование графических контейнеров</span><span class="sxs-lookup"><span data-stu-id="2a099-103">Using Graphics Containers</span></span>

<span data-ttu-id="2a099-104">[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект предоставляет такие методы, как [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))и [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) для отображения векторных изображений, растровых изображений и текста.</span><span class="sxs-lookup"><span data-stu-id="2a099-104">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides methods such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="2a099-105">Объект **Graphics** также имеет несколько свойств, влияющих на качество и ориентацию рисуемых элементов.</span><span class="sxs-lookup"><span data-stu-id="2a099-105">A **Graphics** object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="2a099-106">Например, свойство «режим сглаживания» определяет, применяется ли сглаживание к линиям и кривым, а свойство «мировое преобразование» влияет на расположение и поворот рисуемых элементов.</span><span class="sxs-lookup"><span data-stu-id="2a099-106">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>

<span data-ttu-id="2a099-107">[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект часто связывается с конкретным устройством вывода.</span><span class="sxs-lookup"><span data-stu-id="2a099-107">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object is often associated with a particular display device.</span></span> <span data-ttu-id="2a099-108">При использовании **графического** объекта для рисования в окне **графический** объект также связывается с этим конкретным окном.</span><span class="sxs-lookup"><span data-stu-id="2a099-108">When you use a **Graphics** object to draw in a window, the **Graphics** object is also associated with that particular window.</span></span>

<span data-ttu-id="2a099-109">Объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) можно рассматривать как контейнер, так как он содержит набор свойств, влияющих на прорисовку, и связан с информацией, относящейся к конкретному устройству.</span><span class="sxs-lookup"><span data-stu-id="2a099-109">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be thought of as a container because it holds a set of properties that influence drawing, and it is linked to device-specific information.</span></span> <span data-ttu-id="2a099-110">Вы можете создать дополнительный контейнер в существующем объекте **Graphics** , вызвав метод [бегинконтаинер](/previous-versions//ms535731(v=vs.85)) этого **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="2a099-110">You can create a secondary container within an existing **Graphics** object by calling the [BeginContainer](/previous-versions//ms535731(v=vs.85)) method of that **Graphics** object.</span></span>

<span data-ttu-id="2a099-111">В следующих разделах более подробно рассматриваются [**графические**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекты и вложенные контейнеры.</span><span class="sxs-lookup"><span data-stu-id="2a099-111">The following topics cover [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) objects and nested containers in more detail:</span></span>

-   [<span data-ttu-id="2a099-112">Состояние графического объекта</span><span class="sxs-lookup"><span data-stu-id="2a099-112">The State of a Graphics Object</span></span>](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [<span data-ttu-id="2a099-113">Вложенные графические контейнеры</span><span class="sxs-lookup"><span data-stu-id="2a099-113">Nested Graphics Containers</span></span>](-gdiplus-nested-graphics-containers-use.md)

 

 
