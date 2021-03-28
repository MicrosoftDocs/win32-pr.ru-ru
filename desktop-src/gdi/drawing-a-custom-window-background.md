---
description: Вы можете нарисовать собственный фон окна, не нарисуя его.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Рисование пользовательского фона окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984985"
---
# <a name="drawing-a-custom-window-background"></a>Рисование пользовательского фона окна

Вы можете нарисовать собственный фон окна, не нарисуя его. Большинство приложений задают дескриптор кисти или значение системного цвета для кисти фона класса при регистрации класса окна; для рисования фона система использует кисть или цвет. Однако если задать для кисти фона класса **значение NULL**, система отправляет сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) в вашу оконную процедуру каждый раз, когда необходимо прорисовка фона окна, позволяя рисовать пользовательский фон.

В следующем примере процедура Window рисует большой шаблон шахматной доски, который точно соответствует в окне. Процедура заполняет клиентскую область белой кистью, а затем Рисует прямоугольники 13 20 на 20 с помощью серой кисти. Контекст устройства отображения, используемый при рисовании фона, задается в параметре *wParam* сообщения.


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



Если приложение рисует собственное окно с минимальным объемом, система также отправляет сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) в процедуру окна, чтобы нарисовать фон для сворачивания окна. Ту же методику, которую использует [**WM \_ Paint**](wm-paint.md) , можно использовать, чтобы определить, является ли окно сведенным, то есть вызвать функцию « [**Icon**](/windows/win32/api/winuser/nf-winuser-isiconic) » и проверить возвращаемое значение **true**.

 

 
