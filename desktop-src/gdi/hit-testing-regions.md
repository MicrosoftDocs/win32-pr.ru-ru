---
description: Приложение выполняет проверку нажатия для регионов, чтобы определить координаты текущей позиции курсора.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Регионы проверки попадания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263676"
---
# <a name="hit-testing-regions"></a><span data-ttu-id="b8c39-103">Регионы проверки попадания</span><span class="sxs-lookup"><span data-stu-id="b8c39-103">Hit Testing Regions</span></span>

<span data-ttu-id="b8c39-104">Приложение выполняет проверку нажатия для регионов, чтобы определить координаты текущей позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="b8c39-104">An application performs hit testing on regions to determine the coordinates of the current cursor position.</span></span> <span data-ttu-id="b8c39-105">Затем он передает эти координаты, а также маркер, определяющий регион для функции [**птинрегион**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .</span><span class="sxs-lookup"><span data-stu-id="b8c39-105">Then it passes these coordinates as well as a handle identifying the region to the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span> <span data-ttu-id="b8c39-106">Координаты курсора можно получить, обрабатывая различные сообщения мыши, такие как [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) , [**WM \_ Лбуттонуп**](../inputdev/wm-lbuttonup.md) , [**WM \_ рбуттондовн**](../inputdev/wm-rbuttondown.md) и [**WM \_ рбуттонуп**](../inputdev/wm-rbuttonup.md).</span><span class="sxs-lookup"><span data-stu-id="b8c39-106">The cursor coordinates can be retrieved by processing the various mouse messages, such as [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM\_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) , and [**WM\_RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span></span> <span data-ttu-id="b8c39-107">Возвращаемое значение для Птинрегион указывает, находится ли расположение курсора в заданной области.</span><span class="sxs-lookup"><span data-stu-id="b8c39-107">The return value for PtInRegion indicates whether the cursor position is within the given region.</span></span>

 

 
