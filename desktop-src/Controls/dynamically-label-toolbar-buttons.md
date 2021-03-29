---
title: Динамическое добавление меток для кнопок панели инструментов
description: Можно назначить текст существующей кнопке с помощью \_ сообщения СЕТБУТТОНИНФО ТБ.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104487376"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Динамическое добавление меток для кнопок панели инструментов

Можно назначить текст существующей кнопке с помощью сообщения [**\_ сетбуттонинфо ТБ**](tb-setbuttoninfo.md) .

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции

### <a name="dynamically-label-a-toolbar-button"></a>Динамическое добавление метки для кнопки панели инструментов

В следующем примере показано, как изменить текст третьей кнопки в предыдущих примерах с **Save** на **Сохранить как**.


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a>Комментарии

Изменение текста кнопки с помощью [**ТБ \_ сетбуттонинфо**](tb-setbuttoninfo.md) не влияет на строку, назначенную этой кнопке в списке внутренних строк.

При добавлении строки кнопки панели инструментов во внутренний текстовый список невозможно получить индекс этой строки путем вызова [ТБН \_ жетбуттонинфо](tbn-getbuttoninfo.md)— вместо этого следует использовать сообщение о [**\_ кнопке ТБ**](tb-getbutton.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




