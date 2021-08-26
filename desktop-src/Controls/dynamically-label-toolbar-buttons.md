---
title: Динамическое добавление меток для кнопок панели инструментов
description: Можно назначить текст существующей кнопке с помощью \_ сообщения СЕТБУТТОНИНФО ТБ.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063a3b8be8a23dc8cead219c53989a8ff1a40225dc8411f9e8a1b156b6bb55bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877444"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Динамическое добавление меток для кнопок панели инструментов

Можно назначить текст существующей кнопке с помощью сообщения [**\_ сетбуттонинфо ТБ**](tb-setbuttoninfo.md) .

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

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



## <a name="remarks"></a>Remarks

Изменение текста кнопки с помощью [**ТБ \_ сетбуттонинфо**](tb-setbuttoninfo.md) не влияет на строку, назначенную этой кнопке в списке внутренних строк.

При добавлении строки кнопки панели инструментов во внутренний текстовый список невозможно получить индекс этой строки путем вызова [ТБН \_ жетбуттонинфо](tbn-getbuttoninfo.md)— вместо этого следует использовать сообщение о [**\_ кнопке ТБ**](tb-getbutton.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления ToolBar](using-toolbar-controls.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




