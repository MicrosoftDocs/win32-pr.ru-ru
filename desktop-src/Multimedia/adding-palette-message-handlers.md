---
title: Добавление обработчиков сообщений палитры
description: Добавление обработчиков сообщений палитры
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- Дравдиб, палитры
- Функция Дравдибреализе
- Функция Дравдибдрав
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412924"
---
# <a name="adding-palette-message-handlers"></a><span data-ttu-id="00b9e-106">Добавление обработчиков сообщений палитры</span><span class="sxs-lookup"><span data-stu-id="00b9e-106">Adding Palette Message Handlers</span></span>

<span data-ttu-id="00b9e-107">В следующем примере показаны простые обработчики сообщений для сообщений [**WM \_ Палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) и [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="00b9e-107">The following example illustrates simple message handlers for the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages.</span></span> <span data-ttu-id="00b9e-108">В примере используется функция [**дравдибреализе**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) для обработки сообщения **WM \_ куериневпалетте** .</span><span class="sxs-lookup"><span data-stu-id="00b9e-108">The example uses the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to process the **WM\_QUERYNEWPALETTE** message.</span></span>

<span data-ttu-id="00b9e-109">Приложение должно реагировать на сообщение [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) путем непроверки окна назначения, чтобы позволить функции [**дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) перерисовывать изображение.</span><span class="sxs-lookup"><span data-stu-id="00b9e-109">Your application should respond to the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message by invalidating the destination window to let the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function redraw an image.</span></span> <span data-ttu-id="00b9e-110">Чтобы реализовать палитру, необходимо ответить на сообщение [**WM \_ палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) с помощью функции [**дравдибреализе**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) .</span><span class="sxs-lookup"><span data-stu-id="00b9e-110">You should respond to the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) message by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to realize the palette.</span></span>


```C++
case WM_PALETTECHANGED: 
    if ((HWND)wParam == hwnd) 
        break; 
case WM_QUERYNEWPALETTE: 
    hdc = GetDC(hwnd); 
    f = DrawDibRealize(hdd, hdc, FALSE) > 0; 
    ReleaseDC(hwnd, hdc); 
    if (f) 
        InvalidateRect(hwnd, NULL, TRUE); 
    break; 

```



## <a name="related-topics"></a><span data-ttu-id="00b9e-111">См. также</span><span class="sxs-lookup"><span data-stu-id="00b9e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b9e-112">Использование Дравдиб</span><span class="sxs-lookup"><span data-stu-id="00b9e-112">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 