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
# <a name="adding-palette-message-handlers"></a>Добавление обработчиков сообщений палитры

В следующем примере показаны простые обработчики сообщений для сообщений [**WM \_ Палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) и [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) . В примере используется функция [**дравдибреализе**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) для обработки сообщения **WM \_ куериневпалетте** .

Приложение должно реагировать на сообщение [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) путем непроверки окна назначения, чтобы позволить функции [**дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) перерисовывать изображение. Чтобы реализовать палитру, необходимо ответить на сообщение [**WM \_ палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) с помощью функции [**дравдибреализе**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) .


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Дравдиб](using-drawdib.md)
</dt> </dl>

 

 