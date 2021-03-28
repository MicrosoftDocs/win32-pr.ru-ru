---
description: Чтобы ответить на сообщение WM \_ Paint, используйте код, подобный приведенному ниже.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Рисование на контроллере домена, охватывающем несколько экранов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5b1b85c8aab20b7ef2415c1d67188ecab7728c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544439"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a><span data-ttu-id="b85f8-103">Рисование на контроллере домена, охватывающем несколько экранов</span><span class="sxs-lookup"><span data-stu-id="b85f8-103">Painting on a DC That Spans Multiple Displays</span></span>

<span data-ttu-id="b85f8-104">Чтобы ответить на сообщение **WM \_ Paint** , используйте код, подобный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="b85f8-104">To respond to a **WM\_PAINT** message, use code like the following.</span></span>


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



<span data-ttu-id="b85f8-105">Чтобы закрасить верхнюю половину окна, используйте код, подобный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="b85f8-105">To paint the top half of a window, use code like the following.</span></span>


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



<span data-ttu-id="b85f8-106">Чтобы оптимально закрасить весь виртуальный экран для каждого монитора, используйте код, подобный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="b85f8-106">To paint the entire virtual screen optimally for each monitor, use code like the following.</span></span>


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



