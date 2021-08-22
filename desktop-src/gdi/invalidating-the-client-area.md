---
description: Система не является единственным источником \_ сообщений WM Paint. Функция Инвалидатерект или Инвалидатергн может косвенно создавать \_ сообщения WM Paint для окон. Эти функции отмечают всю клиентскую область как недопустимую (которую необходимо перерисовать) или ее часть.
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Идет недействительность клиентской области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94a3a5b4e6903c549331788f9e81947dca44e7a699bb1a633bce46525585b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558664"
---
# <a name="invalidating-the-client-area"></a>Идет недействительность клиентской области

Система не является единственным источником сообщений [**WM \_ Paint**](wm-paint.md) . Функция [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) или [**инвалидатергн**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) может косвенно создавать сообщения **WM \_ Paint** для окон. Эти функции отмечают всю клиентскую область как недопустимую (которую необходимо перерисовать) или ее часть.

В следующем примере оконная процедура делает всю клиентскую область недействительной при обработке сообщений [**WM \_ char**](../inputdev/wm-char.md) . Это позволяет пользователю изменить рисунок, введя число и просмотрев результаты. Эти результаты отображаются, как только в очереди сообщений приложения отсутствуют другие сообщения.


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



В этом примере аргумент **null** , используемый в [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , указывает всю клиентскую область. Аргумент **true** приводит к удалению фона. Если вы не хотите, чтобы приложение ожидало, чтобы в очереди сообщений приложения не было других сообщений, используйте функцию [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) , чтобы принудительно отправить сообщение [**WM \_ Paint**](wm-paint.md) . Если в клиентской области имеется какая-либо недопустимая часть, **упдатевиндов** отправляет сообщение **WM \_ Paint** для указанного окна непосредственно в процедуру окна.

 

 
