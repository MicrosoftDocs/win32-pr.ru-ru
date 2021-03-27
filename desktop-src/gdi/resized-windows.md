---
description: Система изменяет размер окна при выборе пользователем команд меню «окно», таких как размер и развертывание, или когда приложение вызывает функции, такие как функция SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Измененные размеры окон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898394"
---
# <a name="resized-windows"></a><span data-ttu-id="b54f8-103">Измененные размеры окон</span><span class="sxs-lookup"><span data-stu-id="b54f8-103">Resized Windows</span></span>

<span data-ttu-id="b54f8-104">Система изменяет размер окна при выборе пользователем команд меню «окно», таких как размер и развертывание, или когда приложение вызывает функции, такие как функция [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="b54f8-104">The system changes the size of a window when the user chooses window menu commands, such as Size and Maximize, or when the application calls functions, such as the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function.</span></span> <span data-ttu-id="b54f8-105">При изменении размера окна система предполагает, что содержимое ранее предоставленной части окна не затрагивается и его не нужно перерисовать.</span><span class="sxs-lookup"><span data-stu-id="b54f8-105">When a window changes size, the system assumes that the contents of the previously exposed portion of the window are not affected and need not be redrawn.</span></span> <span data-ttu-id="b54f8-106">Система делает недействительным только недавно открытую часть окна, что экономит время, когда в приложении обрабатывается сообщение о завершении работы [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="b54f8-106">The system invalidates only the newly exposed portion of the window, which saves time when the eventual [**WM\_PAINT**](wm-paint.md) message is processed by the application.</span></span> <span data-ttu-id="b54f8-107">В этом случае **WM \_ Paint** не создается при уменьшении размера окна.</span><span class="sxs-lookup"><span data-stu-id="b54f8-107">In this case, **WM\_PAINT** is not generated when the size of the window is reduced.</span></span>

<span data-ttu-id="b54f8-108">Для некоторых окон любое изменение размера окна сделает содержимое недействительным.</span><span class="sxs-lookup"><span data-stu-id="b54f8-108">For some windows, any change to the size of the window invalidates the contents.</span></span> <span data-ttu-id="b54f8-109">Например, приложение для работы с часами, которое адаптирует грань часов к точному размеру окна, должно перерисовывать часы при каждом изменении размера окна.</span><span class="sxs-lookup"><span data-stu-id="b54f8-109">For example, a clock application that adapts the face of the clock to fit neatly within its window must redraw the clock whenever the window changes size.</span></span> <span data-ttu-id="b54f8-110">Чтобы заставить систему сделать недействительной всю клиентскую область окна при изменении вертикального, горизонтального или вертикального и горизонтального изменения, в приложении необходимо указать \_ стиль CS вредрав или CS \_ хредрав или и то, и другое, при регистрации класса Window.</span><span class="sxs-lookup"><span data-stu-id="b54f8-110">To force the system to invalidate the entire client area of the window when a vertical, horizontal, or both vertical and horizontal change is made, an application must specify the CS\_VREDRAW or CS\_HREDRAW style, or both, when registering the window class.</span></span> <span data-ttu-id="b54f8-111">Любое окно, принадлежащее классу окна, имеющее эти стили, становится недействительным каждый раз, когда пользователь или приложение изменяют размер окна.</span><span class="sxs-lookup"><span data-stu-id="b54f8-111">Any window belonging to a window class having these styles is invalidated each time the user or the application changes the size of the window.</span></span>

 

 
