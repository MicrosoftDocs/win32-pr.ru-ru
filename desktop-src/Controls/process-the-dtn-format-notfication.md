---
title: Обработка уведомления DTN_FORMAT
description: В этом разделе показано, как обработать уведомление формата, отправленное элементом управления "Выбор даты и времени" (DTP).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d1234dbd9d09159335539309deec86e2d3e1e05547d933cd18f16b9d7162d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829915"
---
# <a name="how-to-process-the-dtn_format-notification"></a>Обработка \_ уведомления формата ДТН

В этом разделе показано, как обработать уведомление формата, отправленное элементом управления "Выбор даты и времени" (DTP).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Обязательные условия

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции


Элемент управления DTP отправляет уведомление [ \_ формата ДТН](dtn-format.md) для запроса текста, который будет отображаться в поле обратного вызова элемента управления. Приложение должно справиться с этим уведомлением, чтобы элемент управления DTP отображал информацию, которая не поддерживает встроенную поддержку.

Следующий пример кода C++ — определяемая приложением функция (**доформат**), которая обрабатывает коды [уведомлений \_ формата ДТН](dtn-format.md) , предоставляя текстовую строку для поля обратного вызова. Приложение вызывает определяемую приложением **жетдайнум** функцию, чтобы запросить номер дня, который будет использоваться в строке обратного вызова.


```C++
//  DoFormat processes DTN_FORMAT to provide the text for a callback
//  field in a DTP control. In this example, the callback field
//  contains a value for the day of year. The function calls the 
//  application-defined function GetDayNum (below) to retrieve
//  the correct value. StringCchPrintf truncates the formatted string if
//  the entire string will not fit into the destination buffer. 

void WINAPI DoFormat(HWND hwndDP, LPNMDATETIMEFORMAT lpDTFormat)
{
HRESULT hr = StringCchPrintf(lpDTFormat->szDisplay,
                sizeof(lpDTFormat->szDisplay)/sizeof(lpDTFormat->szDisplay[0]),
                L"%d",GetDayNum(&lpDTFormat->st));
if(SUCCEEDED(hr))
 {
   // Insert code here to handle the case when the function succeeds.      
 }
else
 {
   // Insert code here to handle the case when the function fails or the string 
   // is truncated.
 }
}
```



**Определяемая приложением функция Жетдайнум**

Определяемая приложением пример функции **доформат** вызывает следующую определяемую приложением **жетдайнум** функцию для запроса номера дня на основе текущей даты. **Жетдайнум** возвращает значение **типа int** , представляющее текущий день года, от 0 до 366. Эта функция вызывает другую определяемую приложением функцию **ислеапир** во время обработки.


```C++
//  GetDayNum is an application-defined function that retrieves the 
//  correct day of year value based on the contents of a given 
//  SYSTEMTIME structure. This function calls the IsLeapYr function to 
//  check if the current year is a leap year. The function returns an 
//  integer value that represents the day of year.

int WINAPI GetDayNum(SYSTEMTIME *st)
{
    int iNormYearAccum[ ] = {31,59,90,120,151,181,
                            212,243,273,304,334,365};
    int iLeapYearAccum[ ] = {31,60,91,121,152,182,
                            213,244,274,305,335,366};
    int iDayNum;

    if(IsLeapYr(st->wYear))
        iDayNum=iLeapYearAccum[st->wMonth-2]+st->wDay;
    else
        iDayNum=iNormYearAccum[st->wMonth-2]+st->wDay;

    return (iDayNum);
}        
```



**Определяемая приложением функция Ислеапир**

Определяемая приложением функция **жетдайнум** вызывает функцию **ислеапир** , чтобы определить, является ли текущий год високосным годом. **Ислеапир** возвращает **логическое** значение, равное **true** , если это високосный год, и **false** в противном случае.


```C++
//  IsLeapYr determines if a given year value is a leap year. The
//  function returns TRUE if the current year is a leap year, and 
//  FALSE otherwise.

BOOL WINAPI IsLeapYr(int iYear)
{
    BOOL fLeapYr = FALSE;

    // If the year is evenly divisible by 4 and not by 100, but is 
    // divisible by 400, it is a leap year.
    if ((!(iYear % 4))             // each even fourth year
            && ((iYear % 100)      // not each even 100 year
            || (!(iYear % 400))))  // but each even 400 year
        fLeapYr = TRUE;

    return (fLeapYr);
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

 

 




