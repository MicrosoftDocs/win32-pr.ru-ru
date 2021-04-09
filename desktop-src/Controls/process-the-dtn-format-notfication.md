---
title: Обработка уведомления DTN_FORMAT
description: В этом разделе показано, как обработать уведомление формата, отправленное элементом управления "Выбор даты и времени" (DTP).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103891245"
---
# <a name="how-to-process-the-dtn_format-notification"></a><span data-ttu-id="0e10f-103">Обработка \_ уведомления формата ДТН</span><span class="sxs-lookup"><span data-stu-id="0e10f-103">How to Process the DTN\_FORMAT Notification</span></span>

<span data-ttu-id="0e10f-104">В этом разделе показано, как обработать уведомление формата, отправленное элементом управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="0e10f-104">This topic demonstrates how to process a format notification sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0e10f-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="0e10f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0e10f-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="0e10f-106">Technologies</span></span>

-   [<span data-ttu-id="0e10f-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="0e10f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0e10f-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="0e10f-108">Prerequisites</span></span>

-   <span data-ttu-id="0e10f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="0e10f-109">C/C++</span></span>
-   <span data-ttu-id="0e10f-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="0e10f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0e10f-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="0e10f-111">Instructions</span></span>


<span data-ttu-id="0e10f-112">Элемент управления DTP отправляет уведомление [ \_ формата ДТН](dtn-format.md) для запроса текста, который будет отображаться в поле обратного вызова элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0e10f-112">A DTP control sends the [DTN\_FORMAT](dtn-format.md) notification to request text that will be displayed in a callback field of the control.</span></span> <span data-ttu-id="0e10f-113">Приложение должно справиться с этим уведомлением, чтобы элемент управления DTP отображал информацию, которая не поддерживает встроенную поддержку.</span><span class="sxs-lookup"><span data-stu-id="0e10f-113">Your application must handle this notification to enable the DTP control to display information that it does not natively support.</span></span>

<span data-ttu-id="0e10f-114">Следующий пример кода C++ — определяемая приложением функция (**доформат**), которая обрабатывает коды [уведомлений \_ формата ДТН](dtn-format.md) , предоставляя текстовую строку для поля обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0e10f-114">The following C++ code example is an application-defined function (**DoFormat**) that processes [DTN\_FORMAT](dtn-format.md) notification codes by providing a text string for a callback field.</span></span> <span data-ttu-id="0e10f-115">Приложение вызывает определяемую приложением **жетдайнум** функцию, чтобы запросить номер дня, который будет использоваться в строке обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0e10f-115">The application calls the **GetDayNum** application-defined function to request the day number to be used in the callback string.</span></span>


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



<span data-ttu-id="0e10f-116">**Определяемая приложением функция Жетдайнум**</span><span class="sxs-lookup"><span data-stu-id="0e10f-116">**The GetDayNum application-defined function**</span></span>

<span data-ttu-id="0e10f-117">Определяемая приложением пример функции **доформат** вызывает следующую определяемую приложением **жетдайнум** функцию для запроса номера дня на основе текущей даты.</span><span class="sxs-lookup"><span data-stu-id="0e10f-117">The application-defined sample function **DoFormat** calls the following **GetDayNum** application-defined function to request the day number based on the current date.</span></span> <span data-ttu-id="0e10f-118">**Жетдайнум** возвращает значение **типа int** , представляющее текущий день года, от 0 до 366.</span><span class="sxs-lookup"><span data-stu-id="0e10f-118">**GetDayNum** returns an **INT** value that represents the current day of the year, from 0 to 366.</span></span> <span data-ttu-id="0e10f-119">Эта функция вызывает другую определяемую приложением функцию **ислеапир** во время обработки.</span><span class="sxs-lookup"><span data-stu-id="0e10f-119">This function calls another application-defined function, **IsLeapYr**, during processing.</span></span>


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



<span data-ttu-id="0e10f-120">**Определяемая приложением функция Ислеапир**</span><span class="sxs-lookup"><span data-stu-id="0e10f-120">**The IsLeapYr application-defined function**</span></span>

<span data-ttu-id="0e10f-121">Определяемая приложением функция **жетдайнум** вызывает функцию **ислеапир** , чтобы определить, является ли текущий год високосным годом.</span><span class="sxs-lookup"><span data-stu-id="0e10f-121">The application-defined function **GetDayNum** calls the **IsLeapYr** function to determine whether the current year is a leap year.</span></span> <span data-ttu-id="0e10f-122">**Ислеапир** возвращает **логическое** значение, равное **true** , если это високосный год, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0e10f-122">**IsLeapYr** returns a **BOOL** value that is **TRUE** if it is a leap year and **FALSE** otherwise.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0e10f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0e10f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e10f-124">Использование элементов управления "Выбор даты и времени"</span><span class="sxs-lookup"><span data-stu-id="0e10f-124">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="0e10f-125">Справочник по элементу выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="0e10f-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0e10f-126">Выбор даты и времени</span><span class="sxs-lookup"><span data-stu-id="0e10f-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




