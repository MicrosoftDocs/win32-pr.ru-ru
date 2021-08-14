---
description: Для просмотра доступных шрифтов можно использовать диалоговое окно Общие шрифты.
ms.assetid: 317ea311-0592-432a-87b5-58296de003aa
title: Создание логического шрифта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb491a1af055963053e8b0247ecaa212547a750a7bd0a35db0ae983695a2420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887474"
---
# <a name="creating-a-logical-font"></a>Создание логического шрифта

Для просмотра доступных шрифтов можно использовать диалоговое **окно Общие шрифты** . Диалоговое окно **ChooseFont** отображается после того, как приложение инициализирует элементы структуры [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) и вызывает функцию [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . После того как пользователь выберет один из доступных шрифтов и нажмет кнопку **ОК** , функция **ChooseFont** Инициализирует структуру [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) с соответствующими данными. Приложение может затем вызвать функцию [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) и создать логический шрифт на основе запроса пользователя. В следующем примере показано, как это сделать.


```C++
HFONT FAR PASCAL MyCreateFont( void ) 
{ 
    CHOOSEFONT cf; 
    LOGFONT lf; 
    HFONT hfont; 
 
    // Initialize members of the CHOOSEFONT structure.  
 
    cf.lStructSize = sizeof(CHOOSEFONT); 
    cf.hwndOwner = (HWND)NULL; 
    cf.hDC = (HDC)NULL; 
    cf.lpLogFont = &lf; 
    cf.iPointSize = 0; 
    cf.Flags = CF_SCREENFONTS; 
    cf.rgbColors = RGB(0,0,0); 
    cf.lCustData = 0L; 
    cf.lpfnHook = (LPCFHOOKPROC)NULL; 
    cf.lpTemplateName = (LPSTR)NULL; 
    cf.hInstance = (HINSTANCE) NULL; 
    cf.lpszStyle = (LPSTR)NULL; 
    cf.nFontType = SCREEN_FONTTYPE; 
    cf.nSizeMin = 0; 
    cf.nSizeMax = 0; 
 
    // Display the CHOOSEFONT common-dialog box.  
 
    ChooseFont(&cf); 
 
    // Create a logical font based on the user's  
    // selection and return a handle identifying  
    // that font.  
 
    hfont = CreateFontIndirect(cf.lpLogFont); 
    return (hfont); 
} 
```



 

 
