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
# <a name="drawing-with-the-mouse"></a>Рисование с помощью мыши

Вы можете раздать пользователю возможность рисовать линии с помощью мыши, вырисуя процедуру окна при обработке сообщения [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) . Система отправляет сообщение **WM \_ MOUSEMOVE** в оконную процедуру каждый раз, когда пользователь перемещает курсор в пределах окна. Для рисования линий процедура окна может получить контекст устройства отображения и нарисовать линию в окне между положением текущего и предыдущего курсора.

В следующем примере процедура окна подготавливается для рисования, когда пользователь нажимает и удерживает левую кнопку мыши (отправляя сообщение [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) ). По мере того, как пользователь перемещает курсор в пределах окна, процедура окна получает ряд сообщений [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) . Для каждого сообщения процедура окна рисует линию, соединяющую предыдущую и текущую позицией. Для рисования линии процедура использует [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) для получения контекста устройства отображения; После завершения рисования и перед возвратом из сообщения процедура использует функцию [**релеаседк**](/windows/desktop/api/Winuser/nf-winuser-releasedc) для освобождения контекста устройства отображения. Как только пользователь отпускает кнопку мыши, процедура окна очищает флаг, а рисование останавливается (при этом отправляется сообщение [**WM \_ лбуттонуп**](../inputdev/wm-lbuttonup.md) ).


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



Приложение, которое позволяет рисовать, как в этом примере, обычно записывает либо точки, либо строки, чтобы строки можно было перерисовать при каждом обновлении окна. Графические приложения часто используют контекст устройства памяти и связанный точечный рисунок для хранения линий, рисуемых с помощью мыши.

 

 
