---
title: Обработка уведомления DTN_FORMATQUERY
description: В этом разделе показано, как обработать уведомление о формате запроса, отправляемое элементом управления "Выбор даты и времени" (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988021"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Обработка \_ уведомления ДТН форматкуери

В этом разделе показано, как обработать уведомление о формате запроса, отправляемое элементом управления "Выбор даты и времени" (DTP).

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Элемент управления DTP отправляет код уведомления [ДТН \_ форматкуери](dtn-formatquery.md) , чтобы запросить сведения о максимально возможном размере поля обратного вызова в элементе управления. Приложение должно выполнить обработку этого сообщения, чтобы убедиться, что все поля отображаются правильно.

Следующий пример кода C++ представляет собой определяемую приложением функцию, которая обрабатывает код уведомления [ДТН \_ форматкуери](dtn-formatquery.md) , вычисляя ширину самой широкой строки для данного поля обратного вызова.

**Предупреждение системы безопасности:** Неправильное использование **лстркмп** может привести к нарушению безопасности приложения. Например, перед вызовом **лстркмп** в следующем примере кода следует убедиться, что две строки завершаются нулем. Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: Microsoft Windows Controls](sec-comctls.md) .



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование элементов управления "Выбор даты и времени"](using-date-and-time-picker.md)
</dt> <dt>

[Справочник по элементу выбора даты и времени](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Выбор даты и времени](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




