---
title: Обработка уведомления DTN_FORMATQUERY
description: В этом разделе показано, как обработать уведомление о формате запроса, отправляемое элементом управления "Выбор даты и времени" (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c148332c36711e68b7c3b773fdb47acef202c5fd2a67f5620319f06c7fbc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696944"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Обработка \_ уведомления ДТН форматкуери

В этом разделе показано, как обработать уведомление о формате запроса, отправляемое элементом управления "Выбор даты и времени" (DTP).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Элемент управления DTP отправляет код уведомления [ДТН \_ форматкуери](dtn-formatquery.md) , чтобы запросить сведения о максимально возможном размере поля обратного вызова в элементе управления. Приложение должно выполнить обработку этого сообщения, чтобы убедиться, что все поля отображаются правильно.

Следующий пример кода C++ представляет собой определяемую приложением функцию, которая обрабатывает код уведомления [ДТН \_ форматкуери](dtn-formatquery.md) , вычисляя ширину самой широкой строки для данного поля обратного вызова.

**Предупреждение системы безопасности:** Неправильное использование **лстркмп** может привести к нарушению безопасности приложения. Например, перед вызовом **лстркмп** в следующем примере кода следует убедиться, что две строки завершаются нулем. перед продолжением следует ознакомиться с [вопросами безопасности: элементы управления Microsoft Windows](sec-comctls.md) .



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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления "Выбор даты и времени"](using-date-and-time-picker.md)
</dt> <dt>

[Справочник по элементу выбора даты и времени](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Выбор даты и времени](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




