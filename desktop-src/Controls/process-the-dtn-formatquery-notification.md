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
# <a name="how-to-process-the-dtn_formatquery-notification"></a><span data-ttu-id="f2b37-103">Обработка \_ уведомления ДТН форматкуери</span><span class="sxs-lookup"><span data-stu-id="f2b37-103">How to Process the DTN\_FORMATQUERY Notification</span></span>

<span data-ttu-id="f2b37-104">В этом разделе показано, как обработать уведомление о формате запроса, отправляемое элементом управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="f2b37-104">This topic demonstrates how to process a Format Query notification that is sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f2b37-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="f2b37-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f2b37-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="f2b37-106">Technologies</span></span>

-   [<span data-ttu-id="f2b37-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="f2b37-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f2b37-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f2b37-108">Prerequisites</span></span>

-   <span data-ttu-id="f2b37-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="f2b37-109">C/C++</span></span>
-   <span data-ttu-id="f2b37-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="f2b37-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f2b37-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f2b37-111">Instructions</span></span>


<span data-ttu-id="f2b37-112">Элемент управления DTP отправляет код уведомления [ДТН \_ форматкуери](dtn-formatquery.md) , чтобы запросить сведения о максимально возможном размере поля обратного вызова в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="f2b37-112">A DTP control sends a [DTN\_FORMATQUERY](dtn-formatquery.md) notification code to request information about the maximum possible size of a callback field within the control.</span></span> <span data-ttu-id="f2b37-113">Приложение должно выполнить обработку этого сообщения, чтобы убедиться, что все поля отображаются правильно.</span><span class="sxs-lookup"><span data-stu-id="f2b37-113">Your application must handle this message to ensure that all fields are displayed properly.</span></span>

<span data-ttu-id="f2b37-114">Следующий пример кода C++ представляет собой определяемую приложением функцию, которая обрабатывает код уведомления [ДТН \_ форматкуери](dtn-formatquery.md) , вычисляя ширину самой широкой строки для данного поля обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f2b37-114">The following C++ code example is an application-defined function that processes the [DTN\_FORMATQUERY](dtn-formatquery.md) notification code by calculating the width of the widest possible string for a given callback field.</span></span>

<span data-ttu-id="f2b37-115">**Предупреждение системы безопасности:** Неправильное использование **лстркмп** может привести к нарушению безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="f2b37-115">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="f2b37-116">Например, перед вызовом **лстркмп** в следующем примере кода следует убедиться, что две строки завершаются нулем.</span><span class="sxs-lookup"><span data-stu-id="f2b37-116">For example, before calling **lstrcmp** in the following code example you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="f2b37-117">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: Microsoft Windows Controls](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b37-117">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="f2b37-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f2b37-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b37-119">Использование элементов управления "Выбор даты и времени"</span><span class="sxs-lookup"><span data-stu-id="f2b37-119">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="f2b37-120">Справочник по элементу выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="f2b37-120">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f2b37-121">Выбор даты и времени</span><span class="sxs-lookup"><span data-stu-id="f2b37-121">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




