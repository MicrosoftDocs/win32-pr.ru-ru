---
description: Вы можете раздать пользователю возможность рисовать линии с помощью мыши, вырисуя процедуру окна при обработке сообщения WM \_ MOUSEMOVE.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Рисование с помощью мыши
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080502"
---
# <a name="drawing-with-the-mouse"></a><span data-ttu-id="48199-103">Рисование с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="48199-103">Drawing with the Mouse</span></span>

<span data-ttu-id="48199-104">Вы можете раздать пользователю возможность рисовать линии с помощью мыши, вырисуя процедуру окна при обработке сообщения [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="48199-104">You can permit the user to draw lines with the mouse by having your window procedure draw while processing the [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) message.</span></span> <span data-ttu-id="48199-105">Система отправляет сообщение **WM \_ MOUSEMOVE** в оконную процедуру каждый раз, когда пользователь перемещает курсор в пределах окна.</span><span class="sxs-lookup"><span data-stu-id="48199-105">The system sends the **WM\_MOUSEMOVE** message to the window procedure whenever the user moves the cursor within the window.</span></span> <span data-ttu-id="48199-106">Для рисования линий процедура окна может получить контекст устройства отображения и нарисовать линию в окне между положением текущего и предыдущего курсора.</span><span class="sxs-lookup"><span data-stu-id="48199-106">To draw lines, the window procedure can retrieve a display device context and draw a line in the window between the current and previous cursor positions.</span></span>

<span data-ttu-id="48199-107">В следующем примере процедура окна подготавливается для рисования, когда пользователь нажимает и удерживает левую кнопку мыши (отправляя сообщение [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) ).</span><span class="sxs-lookup"><span data-stu-id="48199-107">In the following example, the window procedure prepares for drawing when the user presses and holds the left mouse button (sending the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message).</span></span> <span data-ttu-id="48199-108">По мере того, как пользователь перемещает курсор в пределах окна, процедура окна получает ряд сообщений [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="48199-108">As the user moves the cursor within the window, the window procedure receives a series of [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages.</span></span> <span data-ttu-id="48199-109">Для каждого сообщения процедура окна рисует линию, соединяющую предыдущую и текущую позицией.</span><span class="sxs-lookup"><span data-stu-id="48199-109">For each message, the window procedure draws a line connecting the previous position and the current position.</span></span> <span data-ttu-id="48199-110">Для рисования линии процедура использует [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) для получения контекста устройства отображения; После завершения рисования и перед возвратом из сообщения процедура использует функцию [**релеаседк**](/windows/desktop/api/Winuser/nf-winuser-releasedc) для освобождения контекста устройства отображения.</span><span class="sxs-lookup"><span data-stu-id="48199-110">To draw the line, the procedure uses [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) to retrieve a display device context; then, as soon as drawing is complete and before returning from the message, the procedure uses the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context.</span></span> <span data-ttu-id="48199-111">Как только пользователь отпускает кнопку мыши, процедура окна очищает флаг, а рисование останавливается (при этом отправляется сообщение [**WM \_ лбуттонуп**](../inputdev/wm-lbuttonup.md) ).</span><span class="sxs-lookup"><span data-stu-id="48199-111">As soon as the user releases the mouse button, the window procedure clears the flag, and the drawing stops (which sends the [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) message).</span></span>


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



<span data-ttu-id="48199-112">Приложение, которое позволяет рисовать, как в этом примере, обычно записывает либо точки, либо строки, чтобы строки можно было перерисовать при каждом обновлении окна.</span><span class="sxs-lookup"><span data-stu-id="48199-112">An application that enables drawing, as in this example, typically records either the points or lines so that the lines can be redrawn whenever the window is updated.</span></span> <span data-ttu-id="48199-113">Графические приложения часто используют контекст устройства памяти и связанный точечный рисунок для хранения линий, рисуемых с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="48199-113">Drawing applications often use a memory device context and an associated bitmap to store lines that were drawn by using a mouse.</span></span>

 

 
