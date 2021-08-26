---
title: Создание всплывающей подсказки для прямоугольной области
description: В следующем примере показано, как создать стандартный элемент управления ToolTip для всей клиентской области окна.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9be19be187e8c09b3aeb618e1c3518c7c15ca66816cbbb751abe43aa0b9172a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920702"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Создание всплывающей подсказки для прямоугольной области

В следующем примере показано, как создать стандартный элемент управления ToolTip для всей клиентской области окна.

На следующем рисунке показана подсказка, которая отображается, когда указатель мыши находится в окне клиента диалогового окна. Маркер диалогового окна был передан функции, показанной в предыдущем примере.

![снимок экрана: диалоговое окно; указатель мыши находится в окне клиента, и всплывающая подсказка отображается](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Создать подсказку для прямоугольной области

В следующем примере показано, как создать стандартный элемент управления ToolTip для всей клиентской области окна.


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




